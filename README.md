<!DOCTYPE html>
<html>
<head>
  <title>KP Govt Salary Calculator</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>/* آپ پہلے والا CSS رکھ سکتے ہیں */</style>
</head>
<body>
  <h2>KP Govt Salary Calculator</h2>
  <h3>10% Adhoc on running basic pay and 15% DRA on Initial basic pay of 2017</h3>
  <label for="basic">Enter Running Basic Pay:</label>
  <input type="number" id="basic" placeholder="e.g. 45070" />
  <label for="scale">Select BPS Scale:</label>
  <select id="scale"><option value="">-- Select Scale --</option></select>
  <button onclick="calculate()">Calculate Allowances</button>
  <div id="result"></div>
  <script>
    const initial2017Basic = {1:9130,2:9310,3:9610,4:9900,5:10260,6:10620,7:10990,8:11380,9:11770,10:12160,11:12570,12:13320,13:14260,14:15180,15:16120,16:18910,17:30370,18:38350,19:59210};
    const dropdown=document.getElementById("scale");
    for(let i=1;i<=19;i++){let o=document.createElement("option");o.value=i;o.text="BPS-"+i;dropdown.appendChild(o);}
    function calculate(){
      const b=parseFloat(document.getElementById("basic").value),
            s=document.getElementById("scale").value;
      if(!b||!s){alert("Enter basic and select scale");return;}
      const adh=b*0.1, dra=const disparity = initial2017Basic[scale] * 0.30; tot=adh+dra;
      document.getElementById("result").innerHTML=`
        <strong>10% Adhoc Relief:</strong> Rs. ${adh.toFixed(2)}<br>
        <strong>15% Disparity Allowance:</strong> Rs. ${dra.toFixed(2)}<br><hr>
        <strong>Total Increase:</strong> Rs. ${tot.toFixed(2)}`;
    }
  </script>
  <footer>Developed by Zain ul Abideen</footer>
</body>
</html>
