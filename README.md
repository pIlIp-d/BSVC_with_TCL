# BSVC_with_TCL
Fix for running BSVC with TCL interpreter

Download and uncompress [BSVC](https://services.informatik.hs-mannheim.de/%7Eihme/lectures/RUR_Files/bsvc-bin.7z)

   * edit 'your_path/bsvc-bin/BSVC/bin/UI/bscv.tk'
     * add `package require Tk` as first line

Download and Install [ActiveTCL](https://www.heise.de/download/product/activetcl-37562/download)

  * open cmd and run `tclsh 'your_path/bsvc-bin/BSVC/bin/UI/bscv.tk'`

### Optional start script 
  create new file `bsvc.bat`
    
    @echo off
    cmd /c start /min "tclsh" "your_path\bsvc-bin\BSVC\bin\UI\bsvc.tk"
    exit
