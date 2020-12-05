
       
       supp("suppRow1","row1","sommrow1");
       supp("suppRow2","row2","sommrow2");
       supp("suppRow3","row3","sommrow3");
       function supp(objName,rowN,som){
        document.getElementById(objName).addEventListener("click", function (evnt) { 
            var tot = parseFloat(document.getElementById("total").firstChild.data);
            var somme = parseFloat(document.getElementById(som).firstChild.data);
            document.getElementById("total").firstChild.data=tot-somme;  
            document.getElementById(rowN).remove(); 
        });
       } 
    
       calculePlus("calcrow1","quarow1","sommrow1");
       calculePlus("calcrow2","quarow2","sommrow2");
       calculePlus("calcrow3","quarow3","sommrow3");
       function calculePlus(objName,b,c){ 
        document.getElementById(objName).addEventListener("click", function (evnt){ 
            var res = parseFloat(document.getElementById(b).firstChild.data)+1;
            var somme = parseFloat(document.getElementById(c).firstChild.data)+250;
            document.getElementById(b).firstChild.data=res;
            document.getElementById(c).firstChild.data=somme; 
            var tot = parseFloat(document.getElementById("total").firstChild.data);
            document.getElementById("total").firstChild.data=tot+250; 
        })};


        calculeMoins("calcMoinrow1","quarow1","sommrow1");
        calculeMoins("calcMoinrow2","quarow2","sommrow2");
        calculeMoins("calcMoinrow3","quarow3","sommrow3");
        function calculeMoins(objName,b,c){ 
         document.getElementById(objName).addEventListener("click", function (evnt){ 
             var res = parseFloat(document.getElementById(b).firstChild.data)-1;
             var somme = parseFloat(document.getElementById(c).firstChild.data)-250;
             if(res < 0){
                document.getElementById(b).firstChild.data=0;
             }else{
                document.getElementById(b).firstChild.data=res;
             }

             if(somme < 0){
                document.getElementById(c).firstChild.data=0; 
             }else{
                document.getElementById(c).firstChild.data=somme; 
                var tot = parseFloat(document.getElementById("total").firstChild.data);
                document.getElementById("total").firstChild.data=tot-250; 
             }  
         })};
 
var x = document.getElementById("image");
x.addEventListener("click",changer(x));
function changer(x)
 {
     if (x.style.color=="red")
         return x.style.color=="black";
         else
         x.style.color=="red";
 }
       
