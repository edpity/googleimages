function getFiles() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet();
  var range = sheet.getRange("A1:A1")
  cell = range.getCell(1,1);
  var input = cell.getValue();
  var folder = DriveApp.getFolderById(input);
  var page = sheet.getActiveSheet();

  var headings = [["File Name", "File Direct URL", "File Size", "File Owner"]];
  page.getRange("A1:D").clear();
  page.getRange("A1:D1").setValues(headings);
  
  var files = folder.getFiles();
  var i=1;
  while(files.hasNext()) {
    var file = files.next();
    if(sheet.getId() == file.getId()){ 
      continue; 
    }
    page.getRange(i+1, 1, 1, 4).setValues([[file.getName(), "https://drive.google.com/uc?id=" + file.getId(), (file.getSize()/1048576).toFixed(2) + " MiB", file.getOwner()]]);
    i++;
  }
}
