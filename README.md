<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profit and Loss Calculator</title>
    <style>
      body{
        background-color: black;
        text-decoration: antiquewhite;
        font-family: verdana;

      }
      .plcalculator{
        text-decoration: antiquewhite;
        text-align: center;
        background-color: rgb(12, 206, 206);
        width: 500px;
        margin-left: auto;
        margin-right: auto;
        padding: 10px;
      }
    </style>
</head>
<body>

    <div class="plcalculator">
        <h1>Profit and Loss Calculator</h1>
        <p>Cost Price(CP) :   
             <input type="number" id="cost_price" ></p>
             <p>Selling Price(SP) :
                <input type="number" id="selling_price">
             </p>
             <input type="button" value="Calculate" onclick="Calculate()">
             
                <p> profit_loss: <span id="profit_loss"></span></p>
                <p> profit_loss_percentage:<span id="profit_loss_percentage"></span></p>
                <p> Result:<span id="message"></span></p>
             
    </div>
  <script>
  function Calculate()
{
    let CP=document.getElementById('cost_price').value;
    let SP=document.getElementById('selling_price').value;
    let profit_loss= document.getElementById('profit_loss');
    let percentage= document.getElementById('profit_loss_percentage');
    let Result=document.getElementById('message');
  
    
    profit_loss.innerHTML="";
    percentage.innerHTML="";
    Result.innerHTML="";

if(SP>CP)
{
  let profit=SP-CP;
  let profit_percent=((profit/CP)*100);
  profit_loss.innerHTML="profit :" + profit;
  percentage.innerHTML="profit percentage :"+ profit_percent;
   Result.innerHTML="Profit Profit";
 
}
else if(SP<CP)
{
   let loss=CP-SP;
   let loss_percent=((loss/CP)*100);
  profit_loss.innerHTML="loss :"+ loss;
  percentage.innerHTML="loss percentage :" + loss_percent;
   Result.innerHTML="Loss Loss";
  
} 
else
  {
   Result.innerHTML="no profit no loss";
    
  }
  
}

</script>
  </body>
</html>
