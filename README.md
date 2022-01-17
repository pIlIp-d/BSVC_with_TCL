# BSVC_with_TCL
Fix for running BSVC with TCL interpreter (Windows)

Download and uncompress [BSVC](https://services.informatik.hs-mannheim.de/%7Eihme/lectures/RUR_Files/bsvc-bin.7z)

   * edit `your_path/bsvc-bin/BSVC/bin/UI/bscv.tk`
     * change `set install_dir {C:\Programme\BSVC\bin}` to your_path
     * add `package require Tk` as first line

Download and Install [ActiveTCL](https://www.heise.de/download/product/activetcl-37562/download)

  * open cmd and run `tclsh 'your_path/bsvc-bin/BSVC/bin/UI/bscv.tk'`

### assemble .asm files
 > your bsvc-bin directory contains `68kasm.exe`<br>
 > open cmd and navigate into bsvc-bin<br>
 > assemble your .h68 with `68kasm.exe -l 'Path_to_.asm'`


### Optional start script 
  create new file `bsvc.bat`
    
        @echo off
        cmd /c start /min "tclsh" "your_path\bsvc-bin\BSVC\bin\UI\bsvc.tk"
        exit
    
 if tclsh isn't automatically linked for execution, manually select programm `search_for_your_own_path/tclsh.exe`
