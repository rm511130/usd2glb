# usd2glb

`./blender -b -P usd2glb.py -- -i <sample.usd> -o <output-directory> -s <sample.glb>`

```
        -b = background or headless
        -P = Python
usd2glb.py = Python Script
        -- = subsequent parameters are inputs for the Python code
        -i = input USD file name and location
        -o = optional output directory where all USD subcomponents will be saved as GLB files 
        -s = optional file name and location of single GLB file conversion from USD file
```

- Python Script for converting [USD files](https://graphics.pixar.com/usd/release/usdfaq.html) into [GLB format](https://en.wikipedia.org/wiki/GlTF)

   1. Converts a single USD file into a single GLB
   2. Converts all subcomponents of a USD file into GLBs

## Requirements: <a name="requirements"></a>
   - [Blender 3.3 or later](https://www.blender.org/download/) installed on your machine
   - Download [`usd2glb.py`](https://drive.google.com/file/d/1KN-noZbOH_hVfCcQgaQo7IAW4CgXGKbs/view?usp=sharing)
   - Download [`PZ2.usd`](https://drive.google.com/file/d/1fJyewo1JMThtBwSZkCKmwBoyg-MuD1mp/view?usp=sharing). It's a sample `usd` file.
   - Windows OS (access to [PowerShell ISE](https://learn.microsoft.com/en-us/powershell/scripting/learn/ps101/01-getting-started?view=powershell-7.2#where-do-i-find-powershell)) or MacOS (access to [Terminal](https://support.apple.com/guide/terminal/open-or-quit-terminal-apd5265185d-f365-44cb-8b09-71a064a42125/mac))
   
_Note: The Python Code will be executed as headless / background service_

## How to execute: <a name="how-to"></a>

### a. Windows PowerShell Example:

```
cd "C:\Program Files\Blender Foundation\Blender 3.3"
mkdir ~\Downloads\output
.\blender.exe -b -P "C:\Users\Ralph\Downloads\usd2glb.py" -- -i "C:\\Users\\Ralph\\Downloads\\PZ2.usd" -o "C:\\Users\Ralph\\Downloads\\output" -s "C:\\Users\\Ralph\\Downloads\\output\\PZ2.glb"
```

### Notes:
       - Directories referred to in "-i", "-o" and "-s" must already exist
       - Note the need for double backslashes when passing parameters to the Python code
       - Please substitute my \Users\Ralph directory with yours

<details>
<summary>
    Example of Logs - Windows Machine
</summary>
  
```
Blender 3.3.1 (hash b292cfe5a936 built 2022-10-05 00:49:25)
Read prefs: C:\Users\Ralph\AppData\Roaming\Blender Foundation\Blender\3.3\config\userpref.blend
USD import of 'C:\Users\Ralph\Downloads\PZ2.usd' took 13.0 ms
18:24:18 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_001
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_002
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_003
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_004
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_005
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.015670299530029297 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.0 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_001
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.0 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_002
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.01564788818359375 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_003
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.0 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_004
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.0 s

18:24:19 | INFO: Draco mesh compression is available, use library at C:\Program Files\Blender Foundation\Blender 3.3\3.3\python\lib\site-packages\extern_draco.dll
18:24:19 | INFO: Starting glTF 2.0 export
18:24:19 | INFO: Extracting primitive: OBJ_from_SE_PZ2_005
18:24:19 | INFO: Primitives created: 1
18:24:19 | INFO: Finished glTF 2.0 export in 0.0 s


Blender quit
```

</details>


### b. MacOS Terminal Example:

```
cd /Applications/Blender.app/Contents/MacOS
mkdir -p ~/Downloads/output
./blender -b -P ~/Downloads/usd2glb.py -- -i ~/Downloads/PZ2.usd -o ~/Downloads/output -s ~/Downloads/output/PZ2.glb
```

<details>
<summary>
    Example of Logs - MacOS Machine
</summary>
  
```
Blender 3.3.1 (hash b292cfe5a936 built 2022-10-04 23:43:02)
USD import of '/Users/rmeira/Downloads/PZ2.usd' took 68.2 ms
18:37:45 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_001
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_002
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_003
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_004
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_005
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.019634008407592773 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.003885984420776367 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_001
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.003175020217895508 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_002
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.004430055618286133 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_003
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.0035169124603271484 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_004
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.00404810905456543 s
18:37:46 | INFO: Draco mesh compression is available, use library at /Applications/Blender.app/Contents/Resources/3.3/python/lib/python3.10/site-packages/libextern_draco.dylib
18:37:46 | INFO: Starting glTF 2.0 export
18:37:46 | INFO: Extracting primitive: OBJ_from_SE_PZ2_005
18:37:46 | INFO: Primitives created: 1
18:37:46 | INFO: Finished glTF 2.0 export in 0.0036890506744384766 s
Blender quit
```

</details>

### Where:
```
-b = background or headless

-P = Python

Python Script = ~/Downloads/usd2glb.py 

-- = subsequent parameters are inputs for the Python code

-i = input USD file name and location
     Example of USD file name and location = ~/Downloads/PZ2.usd

-o = optional output directory where all USD subcomponents will be saved as GLB files
     Example of output directory: ~/Downloads/output

-s = optional file name and location of single GLB file conversion from USD file
     Example of Single GLB file name and location: ~/Downloads/output/PZ2.glb
```

### Notes:
       - Directories referred to in "-i", "-o" and "-s" must already exist
       - `~` corresponds to your home directory under which is found the `Downloads` directory
       
### Results

- Check under the `output` directory created under your default `Downloads` folder
- You should see a 3D Model of a Puzzle `PZ2.glb` and six Puzzle Pieces in GLB format
