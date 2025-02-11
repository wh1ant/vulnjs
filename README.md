- [Chrome](#Chrome)
	- [Chrome_V8_RCE](#Chrome_V8_RCE)
	- [Chrome_V8_cage_escape(V8_SBX)](#Chrome_V8_cage_escape(V8_SBX))
	- [Chrome_Renderer_RCE](#Chrome_Renderer_RCE)
	- [Chrome_SBX](#Chrome_SBX)
- [Safari](#Safari)
	- [Safari_JavaScriptCore_RCE](#Safari_JavaScriptCore_RCE)
	- [Safari_SBX](#Safari_SBX)
- [Firefox](#Firefox)
	- [Firefox_JS_RCE](#Firefox_JS_RCE)

# Chrome
## Chrome_V8_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](v8/Utils.md)|N/A||
||wasm||[CVE-2017-5122](v8/CVE-2017-5122.md)|Out of bound read||
||wasm|async,Side effect|[CVE-2018-6122](v8/CVE-2018-6122.md)|Type confusion||
||wasm|GC|[CVE-2024-3156](v8/CVE-2024-3156.md)|Inappropriate implementation||
||wasm||[CVE-2024-3832](v8/CVE-2024-3832.md)|Type confusion|Need more time|
|O|wasm||[CVE-2023-4070](v8/CVE-2023-4070.md)|Type confusion||
|O|TurboFan|Concurrent compilation|[CVE-2023-3420](v8/CVE-2023-3420.md)|Type confusion||
|O|TurboFan||[CVE-2018-17463](v8/CVE-2018-17463.md)|Type confusion|Phrack70|
|||enum cache|[CVE-2023-4427](v8/CVE-2023-4427.md)|Out of bound read||
|||enum cache|[CVE-2024-3159](v8/CVE-2024-3159.md)|Out of bound read||
|O|wasm||[CVE-2024-2887](v8/CVE-2024-2887.md)|Type confusion||
||wasm||[CVE-2024-5830](v8/CVE-2024-5830.md)|Type confusion||
|▵|wasm||[CVE-2024-4761](v8/CVE-2024-4761.md)|Out of bound write||
|▵|wasm||[issue-339736513](v8/issue-339736513.md)| Type confusion, OOB read||
||wasm||[CVE-2024-6100](v8/CVE-2024-6100.md)|Type confusion|Variant CVE-2024-2887|
||wasm||[CVE-2024-5158](v8/CVE-2024-5158.md)|Type confusion||
||wasm|Turboshaft|[issue-352720899](v8/issue-352720899.md)|Type confusion|Regress|
|O|Maglev|MaglevGraphBuilder|[CVE-2024-4947](v8/CVE-2024-4947.md)|Type confusion||
|O|Maglev|MaglevGraphBuilder|[CVE-2023-4069](v8/CVE-2023-4069.md)|Type confusion||
|O|||[CVE-2017-5030](v8/CVE-2017-5030.md)|Out of bound read||
|O|||[18-issue-880207](v8/18-issue-880207.md)|Type confusion||
|O|||[CVE-2019-5825](v8/CVE-2019-5825.md)|Type confusion||
|O|||[CVE-2020-6383](v8/CVE-2020-6383.md)|Type confusion||
|O|||[CVE-2021-21225](v8/CVE-2021-21225.md)|Out of bound read||
|O||Property access|[CVE-2021-30632](v8/CVE-2021-30632.md)|Type confusion||
|O|Tutorial||[CVE-2021-38003](Renderer/CVE-2021-38003.md)|Type confusion|Leak Hole|
|O|||[CVE-2022-1310](v8/CVE-2022-1310.md)|Use after free||
|O|||[CVE-2022-1364](v8/CVE-2022-1364.md)|Type confusion|Leak Hole|
|O|||[CVE-2022-4174](v8/CVE-2022-4174.md)|Type confusion|Leak Hole|
|O|||[CVE-2023-2033](v8/CVE-2023-2033.md)|Type confusion|Leak Hole|
|O|||[CVE-2023-3079](v8/CVE-2023-3079.md)|Type confusion|Leak Hole|
||Tutorial||[CVE-2023-3420](v8/CVE-2023-3420.md)|Type confusion|Man Yue Mo|
|O|Maglev||[CVE-2023-4069](v8/CVE-2023-4069.md)|Type confusion|Man Yue Mo|
||||[CVE-2024-4761](v8/CVE-2024-4761.md)|Out of bound write||
|O|||[CVE-2023-4762](v8/CVE-2023-4762.md)|Type confusion|Leak Hole||
||||[CVE-2024-4947](v8/CVE-2024-4947.md)|Type confusion|||
|O||enum cache|[CVE-2023-4427](Haboob/v8/CVE-2023-4427.md)|Out of bound read||
||||[CVE-2024-0517](CVE-2024-0517.md)|Out of Bounds||
||||CVE-2024-0519|Out of bounds||ITW|
|O|||[CVE-2024-5274](v8/CVE-2024-5274.md)|||


## Chrome_V8_cage_escape(V8_SBX)
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](v8/Utils.md)|N/A||
|O|N/A||[Cage_escape](v8/Cage_Escape.md)|2024.6.6||
||wasm||[issue-349529650](v8/issue-349529650.md)|function import signature check race||
||wasm||[issue-336009921](v8/issue-336009921.md)|function signature confusion||
||wasm||[issue-354408144](v8/issue-354408144.md)|function signature confusion||
|O|wasm||[CVE-2024-7024](v8/CVE-2024-7024.md)|function signature confusion||
|O|wasm||[CVE-2024-8904](v8/CVE-2024-8904.md)|Type confusion||
||wasm||[CVE-2024-6779](v8/CVE-2024-6779.md)|Out of Bounds||
|O|wasm||[CVE-2024-8194](v8/CVE-2024-8194.md)|Type confusion|incomplete CVE-2024-6100|
|▵|wasm||[issue-348084786](v8/issue-348084786.md)|Type confusion||
||wasm||[issue-373703277](v8/issue-373703277.md)|Type confusion||



## Chrome_Renderer_RCE

|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Renderer/Utils.md)|N/A||
|O|||[CVE-2021-30551](v8/CVE-2021-30551.md)|Type confusion|Leak Hole|
|O|||[2022-issue-1352549](Renderer/issue-1352549.md)|Type confusion|Leak Hole|
||||[CVE-2024-1669](Renderer/CVE-2024-1669.md)|Out of bound read|reward-7000|
|O|||[CVE-2024-1283](Renderer/CVE-2024-1283.md)|Heap buf overflow||
||Compositing||[CVE-2024-3157](Renderer/CVE-2024-3157.md)|Out of bound write||

## Chrome_SBX
|Pwn|Target|Feature|CVE/issue|Vulnerability|OS|Comment|
|---|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](SBX/Utils.md)|N/A|N/A||
||Mojo||[(2019)75.0.3770.89](SBX/75.0.3770.89.md)|Use after free|All|Refactoring|
||appcache||[2018-Hack2Win](Haboob/SBX/2018-Hack2Win.md)|Use after free|Windows|Full-chain|
|O|Mojo||[CVE-2019-13768](SBX/CVE-2019-13768.md)|Use after free|Windows|Mark Brand|
|O|Mojo||[20-issue-1062091](SBX/20-issue-1062091.md)|Use after free|All||
||Mojo||[CVE-2020-16045](SBX/CVE-2020-16045.md)|Use after free|Android||
||Mojo||[CVE-2021-30528](SBX/CVE-2021-30528.md)|Use after free|Android|Tutorial|
|O|Mojo||[CVE-2021-30633](SBX/CVE-2021-30633.md)|Use after free||
|O|Mojo||[CVE-2022-3075](SBX/CVE-2022-3075.md)|Insufficient data validation|All||
||Mojo||[CVE-2022-4178](SBX/CVE-2022-4178.md)|Use after free|All||
||Mojo||[CVE-2023-6347](SBX/CVE-2023-6347.md)|Use after free||
|X|Mojo||[CVE-2023-0941](SBX/CVE-2023-0941.md)|Use after free|||
||Mojo||[CVE-2023-5218](SBX/CVE-2023-5218.md)|Use after free||reward-28000|
|O|ANGLE||[CVE-2023-1818](SBX/CVE-2023-1818.md)|Use after free|All|Activate SwiftShader|
||ANGLE|SwiftShader|[CVE-2018-16069](SBX/CVE-2018-16069.md)|Heap buf overflow||Project zero|
||ANGLE|SwiftShader|[CVE-2022-4135](SBX/CVE-2022-4135.md)|Heap buf overflow||
||ANGLE|SwiftShader|[CVE-2023-2929](SBX/CVE-2023-2929.md)|Out of bounds write||ITW|
||ANGLE|Vulkan|[CVE-2024-2883](SBX/CVE-2024-2883.md)|Use after free|||
||Skia||[CVE-2023-2136](SBX/CVE-2023-2136.md)|Integer overflow|Android|ITW|
||Skia||[CVE-2023-4354](SBX/CVE-2023-4354.md)|Heap buf overflow||
||Skia||[CVE-2023-6345](SBX/CVE-2023-6345.md)|Integer overflow||ITW|
||||[CVE-2023-2934](SBX/CVE-2023-2934.md)|TOCTOU|||


# Safari
## Safari_JavaScriptCore_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Safari/jsc/Utils.md)|N/A||
|O|Array.slice|Side effect|[CVE-2016-4622](Safari/jsc/CVE-2016-4622.md)|Out of bounds|Phrack70|
|O|Array.reverse||[CVE-2018-4192](Safari/jsc/CVE-2018-4192.md)|Use after free|pwn2own-2018|

## Safari_SBX
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Safari/SBX/Utils.md)|N/A||
|O|WindowServer||[CVE-2018-4193](Safari/SBX/CVE-2018-4193.md)|Out of bounds|pwn2own-2018|


# Firefox
## Firefox_JS_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Firefox/js/Utils.md)|N/A||
|O|SpiderMonkey|Side effect|[CVE-2024-8381](Firefox/js/CVE-2024-8381.md)|Type confusion||
