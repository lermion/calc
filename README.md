# calc

var cell = 10;
		var row = 10;
		function calc(){
			/* Создайте в элементе div таблицу с помощью методов DOM */
			var d = document.getElementById("d");
			d.innerHTML = "";
			var start = new Date();
			var t = d.appendChild(document.createElement("table"));
			var tb = t.appendChild(document.createElement("tbody"));
			for(var i = 1; i <= row; i++){
				var tr = tb.appendChild(document.createElement("tr"));
				for(var j = 1; j <= cell; j++){
					var td = tr.appendChild(document.createElement("td"));
					td.appendChild(document.createTextNode(i * j));
				}
			}
			var end = new Date();
			console.log((end - start) + " ms");
		}
