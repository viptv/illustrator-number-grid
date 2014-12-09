if (app.selection[0] != null) {

	var myDoc = app.activeDocument,
		selectedArt = myDoc.selection[0],
		dupNumber = 365, // set duplicates
		horOffset = 83.38,  // set offset
		verOffset = 83.37,  // set  offset
		
		i = 0;
		x=0;
        c=0;
    ilo = 365;
   
	for (i;i < dupNumber; i++){
        selectedArt.contents = 365-i;
        
        x ++;
        myDuplicate = selectedArt.duplicate();
		myDuplicate.position = [selectedArt.position[0] + horOffset * (x + 1), selectedArt.position[1] + verOffset* (c + 1)];
        
        if(x == 11){
       // myDuplicate.position = [selectedArt.position[0], selectedArt.position[1]];
        c++;
x=0;
        }
      
		}

	} 
else {
	alert("zaznacz cos.");
	}
