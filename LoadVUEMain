var order = new Array;
var sumTotal = 0;
//cost for each group of items
var itemGroupPrices = new Map();

//adds item to order
var askHowMany = function(item, price) {
  if (!Number.isInteger(parseInt(num))) {
    console.log(parseInt(num));
    return;
  }
  num = parseInt(num);
  if (itemGroupPrices.size == 0 || !itemGroupPrices.has(item))
    itemGroupPrices.set(item, num*price);
  else
    itemGroupPrices.set(item, itemGroupPrices.get(item) + num*price);

  sumTotal = sumTotal + num*price;
  for (var i = 0; i < num; i++) {
    var str = item.toString();
    order.push(str);
  }
  console.log("order: " + order);
  console.log(itemGroupPrices.get(item)/price + "x " + item + ": " + itemGroupPrices.get(item));
  console.log("sum total: " + sumTotal);
}

var updateList = function(id, item, price) {
  var quantity = document.getElementById(id).value;
  var num = parseInt(quantity);
  console.log(num);
  if (itemGroupPrices.size == 0 || !itemGroupPrices.has(item))
    itemGroupPrices.set(item, num*price);
  else
    itemGroupPrices.set(item, itemGroupPrices.get(item) + num*price);
  for (var i = 0; i < order.length; i++) {
    if (order[i] == item) {
      order.splice(i, 1);
      i--;
      itemGroupPrices.set(item, itemGroupPrices.get(item) - price);
    }
  }
  if (isNaN(itemGroupPrices.get(item))) {
    itemGroupPrices.set(item, 0);
  }
  sumTotal = sumTotal + num*price;
  for (var i = 0; i < num; i++) {
    order.push(item);
  }
  console.log("order: " + order);
  console.log(itemGroupPrices.get(item)/price + "x " + item + ": " + itemGroupPrices.get(item) + "\n");
  console.log("sum total: " + sumTotal);
}

var printItemGroupPrices = function() {
  var itemPrices = "";
  for (let [item, price] of  itemGroupPrices) {
    itemPrices += itemGroupPrices.get(item) + "x " + item + ": " + itemGroupPrices.get(item) + "<br></br>";
  }
  return itemPrices;
}


$(function(){
  jQuery(document).ready(function() {
    $("#analoginterfaces").hide();
    $("#digitalinterfaces").hide();
    $("#under10klbs").hide();
    $("#over10klbs").hide();
  });
  //dropdowns
  $("#loadcellssval").change(function(event){
    $("#loadcells").replaceWith("<input id='loadcells' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("loadcellssval").value + ">");
    updateList("loadcells", "loadcells", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>" );
  });
  $("#weightscaleval").change(function(event){
    $("#weightscale").replaceWith("<input id='weightscale' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("weightscaleval").value + ">");
    updateList("weightscale", "weightscale", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#impactsensorsval").change(function(event){
    $("#impactsensors").replaceWith("<input id='impactsensors' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("impactsensorsval").value + ">");
    updateList("impactsensors", "impactsensors", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#torquesensorsval").change(function(event){
    $("#torquesensors").replaceWith("<input id='torquesensors' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("torquesensorsval").value + ">");
    updateList("torquesensors", "torquesensors", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#displacementsensorsval").change(function(event){
    $("#displacementsensors").replaceWith("<input id='displacementsensors' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("displacementsensorsval").value + ">");
    updateList("displacementsensors", "displacementsensors", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#pressuresensorsval").change(function(event){
    $("#pressuresensors").replaceWith("<input id='pressuresensors' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("pressuresensorsval").value + ">");
    updateList("pressuresensors", "pressuresensors", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#levelsensorsval").change(function(event){
    $("#levelsensors").replaceWith("<input id='levelsensors' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("levelsensorsval").value + ">");
    updateList("levelsensors", "levelsensors", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#loadvueliteval").change(function(event){
    console.log(document.getElementById("loadvueliteval").value);
    $("#loadvuelite").replaceWith("<input id='loadvuelite' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("loadvueliteval").value + ">");
    updateList("loadvuelite", "loadvuelite", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#loadvueproval").change(function(event){
    $("#loadvuepro").replaceWith("<input id='loadvuepro' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("loadvueproval").value + ">");
    updateList("loadvuepro", "loadvuepro", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#sensorvueval").change(function(event){
    $("#sensorvue").replaceWith("<input id='sensorvue' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("sensorvueval").value + ">");
    updateList("sensorvue", "sensorvue", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#controlvueval").change(function(event){
    $("#controlvue").replaceWith("<input id='controlvue' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("controlvueval").value + ">");
    updateList("controlvue", "controlvue", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#ncounterval").change(function(event){
    $("#ncounter").replaceWith("<input id='ncounter' class='input is-small' type='Quantity' placeholder='Quantity' value=" +
            document.getElementById("ncounterval").value + ">");
    updateList("ncounter", "ncounter", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });

  $("#loadcells").keyup(function(event){
    $("loadcells").css("background-color", "pink");
    updateList("loadcells", "loadcells", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#weightscale").keyup(function(event){
    updateList("weightscale", "weightscale", 1);
    $("#order").replaceWith("<div id='order'class='tile box'>"+ printItemGroupPrices() +" </div>");
  });
  $("#impactsensors").keyup(function(event){
    updateList("impactsensors", "impactsensors", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#torquesensors").keyup(function(event){
    updateList("torquesensors", "torquesensors", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#displacementsensors").keyup(function(event){
    updateList("displacementsensors", "displacementsensors", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div>")
  });
  $("#pressuresensors").keyup(function(event){
    updateList("pressuresensors", "pressuresensors", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>")
  });
  $("#levelsensors").keyup(function(event){
    updateList("levelsensors", "levelsensors", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>")
  });

  $("#loadvuelite").keyup(function(event){
    updateList("loadvuelite", "loadvuelite", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>")
  });
  $("#loadvuepro").keyup(function(event){
    updateList("loadvuepro", "loadvuepro", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>");
  });
  $("#sensorvue").keyup(function(event){
    updateList("sensorvue", "sensorvue", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>");
  });
  $("#controlvue").keyup(function(event){
    updateList("controlvue", "controlvue", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>");
  });
  $("#ncounter").keyup(function(event){
    updateList("ncounter", "ncounter", 1);
    $("#order").replaceWith("<div id='order' class='tile box'>"+ printItemGroupPrices() +" </div><br>");
  });

  //interface dropdowns
  $("#analoginter").click(function( event ) {
    $("#analoginterfaces").show();
    $("#digitalinterfaces").hide();
  });

  $("#digitalinter").click(function( event ) {
    $("#digitalinterfaces").show();
    $("#analoginterfaces").hide();
  });

  //calibration dropdowns
  $("#under10k").click(function( event ) {
    $("#under10klbs").show();
    $("#over10klbs").hide();
  });

  $("#over10k").click(function( event ) {
    $("#under10klbs").hide();
    $("#over10klbs").show();
  });

});
