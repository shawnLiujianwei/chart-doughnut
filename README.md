chart-doughnut
==============

This is chart-doughnut with overlay 

var doughnutData = [
				{
					value: 26,
					color: "#46BFBD",
					highlight: "#5AD3D1",
					label: "Green"
				},
				{
					value: 6,
					color: "#F7464A",
					highlight: "#FF5A5E",
					label: "Red"
				},
				{
					value: 6,
					color: "#949FB1",
					highlight: "#A8B3C5",
					label: "Grey"
				}

			];

			window.onload = function() {
				var ctx = document.getElementById("chart-area");
				var options = {
					//Boolean - Whether we should show a stroke on each segment
					segmentShowStroke: true,
					//String - The colour of each segment stroke
					segmentStrokeColor: "#fff",
					//Number - The width of each segment stroke
					segmentStrokeWidth: 2,
					//Number - The percentage of the chart that we cut out of the middle
					percentageInnerCutout: 92, // This is 0 for Pie charts
					animateRotate: true,
					"innerText": {
						"font": "15px Arial",
						"text": [
							{
								"content": "Text 1",
								"position": {
									"x": 32,
									"y": 70
								}

							}, {
								"content": "Text 2",
								"position": {
									"x": 57,
									"y": 100
								}
							}
						]
					}


				};
				//var t = new Chart(ctx);
				window.myDoughnut = new ChartWithOverlay(ctx, doughnutData, options);
			};

