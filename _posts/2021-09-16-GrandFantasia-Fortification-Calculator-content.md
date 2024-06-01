---
layout: post
title: "GrandFantasia Fortification Calculator"
date: 2021-09-16
---

<html lang="en">
  <style>
    table, th, TD,TR {
      border: 1px solid black;
    }
    </style>
<head>

      <p>Fortification calculator for GrandFantasia </p>
      <label for="">Type weapon attack:</label>
      <input type="text"  id="attk"><input type="button" value="calculate" onclick="forticalc()">
      <div id="fortitable">

      </div>


<script>
  function forticalc(){
    var attk=parseInt(document.getElementById('attk').value)
    if(typeof attk =='number')
    {
      let rates=[3,6,9,12,15,18,21,24,27,31,35,39,45,51,61,67,73,83,88,98];
       var fortitime=1
      var table =document.createElement("table")
      res=document.getElementById('fortitable')
	  res.innerHTML=""
      res.appendChild(table)
       for(x=0;x<rates.length;x++)
      {
        
        var TR=document.createElement("TR")
        TD1=document.createElement('TD')
        fortnbr1=document.createTextNode('+ '+fortitime.toString()+'= ')
        TR.appendChild(TD1.appendChild(fortnbr1))
        fortnbr2=document.createTextNode((rates[x]*0.01)*attk)
        TD2=document.createElement('TD')
        TR.appendChild(TD2.appendChild(fortnbr2))
        table.appendChild(TR)
        fortitime++
      }

    }

  }
</script>

