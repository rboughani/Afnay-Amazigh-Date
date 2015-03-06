/**
 * Developed by Rafik Boughani, To automatic detect current day using Amazigh calendar
 * Email : rafikmias@yahoo.fr
 *
 * helpful to use in your web pages.
 */
 
 /*
  * Initialization
  */
 var laDate = new Date();
 
 var amazighYear = laDate.getFullYear()+950;
 var amazighDay = laDate.getDate()-11;
 var amazighMonth; 

 //Amazigh Month and Day names
 var aggur = ["ⵢⴻⵏⵏⴰⵢⴻⵔ","ⴼⵓⵔⴰⵔ","ⵎⴰⵖⵔⴻⵙ","ⴱⵔⵉⵔ","ⵎⴰⵢⵓ","ⵢⵓⵏⵢⵓ","ⵢⵓⵍⵢⵓ","ⵖⵓⵛⵜ","ⵛⵜⴻⵎⴱⴻⵔ","ⵟⵓⴱⴻⵔ","ⵡⴻⵎⴱⴻⵔ","ⵊⴻⵎⴱⴻⵔ"];
 var ussan = ["ⴰⵔⵉⵎ","ⴰⵔⴰⵎ","ⴰⵀⴰⴷ","ⴰⵎⵀⴰⴷ","ⴻⵎ","ⵙⴻⴷ","ⴰⵛⴻⵔ"];
 var weekly = ["lundi","mardi","marcredi","jeudi","vendredi","samedi","dimanche"];
	
 if (amazighDay<0) {
	amazighMonth = laDate.getMonth()-1;
	// Number of Days in the current Amazigh month
	var amdanWussanWaggur = Date.getDaysInMonth(laDate.getFullYear, amazighMonth);
	// calculate the current day
	amazighDay = ( amdanWussanWaggur - (11 - laDate.getDate()));
 }else{
	amazighMonth = laDate.getMonth();
 }
 
 function AmazighDate() {
	
	this.getYear = function () {
		return amazighYear;
	}
	
	this.getStringDay = function () {
		return ussan[laDate.getDay()-1];
	}
	
	this.getDay = function () {
		return amazighDay;
	}
	
	this.getMonth = function () {
		return amazighMonth;
	}
	
	this.getMonthByName = function () {
		return aggur[amazighMonth];
	}
	
	this.afnayDate = function ($format) {
		
		switch ($format) {
			case "jj/mm/aaaa": $("#amazighDate").text(this.getDay()+"/"+(this.getMonth()+1)+"/"+this.getYear());
							   return this.getDay()+"/"+(this.getMonth()+1)+"/"+this.getYear();
							   break;
			case "jjMM,aaaa" : 
							   $("#amazighDate").text(this.getDay()+" deg "+this.getMonthByName()+", "+this.getYear());
							   return this.getDay()+" deg "+this.getMonthByName()+", "+this.getYear();
							   break;
			default: 		   $("#amazighDate").text(this.getStringDay()+" "+this.getDay()+" "+ this.getMonthByName() +" "+this.getYear());
							   return this.getStringDay()+" "+this.getDay()+" "+ this.getMonthByName() +" "+this.getYear();
							   break;
		}
		
	}
 }
