# -TestTable-arrSelectFields-arrWhereFields
Dim $arrWhereFields[1]=["Firstname = 'Dave'"] $arrRecords = _GetRecords("TestTable",$arrSelectFields,$arrWhereFields) _ArrayDisplay($arrRecords) ;Capture Tables and Colums $tables = _GetTablesAndColumns(1)   ;Param causes display if SYSTEM tables.  Default (no param) hides these tables _ArrayDisplay($tables)   ;Display Tables For $x = 1 to UBound($tables)-1   ;Display Table Columns     _ArrayDisplay($tables[$x][1],"Table Name: " &amp; $tables[$x][0]) Next  ;Add Column to Table _AddColumn("TestTable","Field2","VARCHAR(10)")  ;Drop Column from Table _DropColumn("TestTable","Field2")  ;Drop Table _DropTable("TestTable")
