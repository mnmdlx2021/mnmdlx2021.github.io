#日常问题：
##1. javascript
###1.1 DW 根据某个规则 打开不同的表单？
	function openUrl(){
	var DW_NATURE= getGridFieldValue(rowData,'NATURE'); 
	if(DW_NATURE==null){ DW_NATURE= ''}
		var khlx = DW_NATURE;
		var DW_BINDID = getGridFieldValue(rowData, 'BINDID');
	if (DW_BINDID == null) {
		DW_BINDID = ''
	}
		var openState=1;
		var uid = $("input[name=uid]").val(); 	 
		if (khlx == '自然人' && khlx != null && khlx != '' && DW_BINDID != null && 
		DW_BINDID != ''){ 
		var url = "./w?sid=" + $("#sid").val() + 
		"&cmd=CLIENT_BPM_FORM_MAIN_PAGE_OPEN&processInstId=" + DW_BINDID + 
		"&openState="+openState+"&taskInstId=0&formDefId=4216160c-906c-4c23-
		a785-526cacc331dc";
		window.open(url);
	} else if (khlx=='机构'  && khlx != null && khlx != '' && DW_BINDID != null && 
	DW_BINDID != '') {
		} 
	}
### 1.2 
