- [Chrome](#Chrome)
	- [Chrome_V8_RCE](#Chrome_V8_RCE)
	- [Chrome_V8_cage_escape(V8_SBX)](#Chrome_V8_cage_escape(V8_SBX))
	- [Chrome_Renderer_RCE](#Chrome_Renderer_RCE)
	- [Chrome_SBX](#Chrome_SBX)
- [Safari](#Safari)
	- [Safari_JavaScriptCore_RCE](#Safari_JavaScriptCore_RCE)
	- [Safari_SBX](#Safari_SBX)
- [Firefox](#Firefox)
	- [Firefox_Gecko_RCE](#Firefox_Gecko_RCE)
	- [Firefox_Renderer_RCE](#Firefox_Renderer_RCE)

# Chrome
## Chrome_V8_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](v8/Utils.md)|N/A||
||wasm||[CVE-2017-5122](v8/CVE-2017-5122.md)|Out of bound read||
||wasm|async,Side effect|[CVE-2018-6122](v8/CVE-2018-6122.md)|Type confusion||
||wasm|GC|[CVE-2024-3156](v8/CVE-2024-3156.md)|Inappropriate implementation||
||wasm||[CVE-2024-3832](v8/CVE-2024-3832.md)|Type confusion||
|O|wasm||[CVE-2023-4070](v8/CVE-2023-4070.md)|Type confusion||
|O|wasm||[CVE-2024-2887](v8/CVE-2024-2887.md)|Type confusion||
|▵|wasm||[CVE-2024-4761](v8/CVE-2024-4761.md)|Out of bound write||
|▵|wasm||[issue-339736513](v8/issue-339736513.md)| Type confusion, OOB read||
||wasm||[CVE-2024-6100](v8/CVE-2024-6100.md)|Type confusion||
||wasm||[CVE-2024-5158](v8/CVE-2024-5158.md)|Type confusion||
||wasm|Turboshaft|[issue-352720899](v8/issue-352720899.md)|Type confusion||
|O|TurboFan|Concurrent compilation|[CVE-2023-3420](v8/CVE-2023-3420.md)|Type confusion||
|O|TurboFan|Side effect|[CVE-2018-17463](v8/CVE-2018-17463.md)|Type confusion||
|O|TurboFan|Property access|[CVE-2021-30632](v8/CVE-2021-30632.md)|Type confusion||
|O|TurboFan||[CVE-2025-0612](v8/CVE-2025-0612.md)|Out of bounds|||
|O|Maglev|MaglevGraphBuilder|[CVE-2024-4947](v8/CVE-2024-4947.md)|Type confusion||
|O|Maglev|MaglevGraphBuilder|[CVE-2023-4069](v8/CVE-2023-4069.md)|Type confusion||
||Map transition|Value serializer|[CVE-2023-1214](v8/CVE-2023-1214.md)|Type confusion||
||Map transition|TryFastAddDataProperty|[CVE-2024-5830](v8/CVE-2024-5830.md)|Type confusion||
|O|||[CVE-2017-5030](v8/CVE-2017-5030.md)|Out of bound read||
|O|||[18-issue-880207](v8/18-issue-880207.md)|Type confusion||
|O|||[CVE-2019-5825](v8/CVE-2019-5825.md)|Type confusion||
|O|||[CVE-2020-6383](v8/CVE-2020-6383.md)|Type confusion||
|O|||[CVE-2021-21225](v8/CVE-2021-21225.md)|Out of bound read||
|O|||[CVE-2021-38003](Renderer/CVE-2021-38003.md)|Type confusion||
|O|||[CVE-2022-1310](v8/CVE-2022-1310.md)|Use after free||
|O|||[CVE-2022-1364](v8/CVE-2022-1364.md)|Type confusion||
|O|||[CVE-2022-4174](v8/CVE-2022-4174.md)|Type confusion||
|O|||[CVE-2023-2033](v8/CVE-2023-2033.md)|Type confusion||
|O|||[CVE-2023-3079](v8/CVE-2023-3079.md)|Type confusion||
||||[CVE-2023-3420](v8/CVE-2023-3420.md)|Type confusion||
||||[CVE-2024-4761](v8/CVE-2024-4761.md)|Out of bound write||
|O|||[CVE-2023-4762](v8/CVE-2023-4762.md)|Type confusion|Leak Hole||
||||[CVE-2024-4947](v8/CVE-2024-4947.md)|Type confusion|||
|O||enum cache|[CVE-2023-4427](v8/CVE-2023-4427.md)|Out of bound read||
|||enum cache|[CVE-2024-3159](v8/CVE-2024-3159.md)|Out of bound read||
||||[CVE-2024-0517](v8/CVE-2024-0517.md)|Out of Bounds||
||||[CVE-2024-0519](v8/CVE-2024-0519)|Out of bounds|||
|O|Parser|Incorrect parsing|[CVE-2024-5274](v8/CVE-2024-5274.md)|Type confusion||


## Chrome_V8_cage_escape(V8_SBX)
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|O|Runtime|Isolate|[my-v8sbx-bug](v8/my-v8sbx-bug.md)|N/A||
||wasm||[issue-349529650](v8/issue-349529650.md)|Function import signature check race||
|O|wasm||[issue-336009921](v8/issue-336009921.md)|Function signature confusion||
|O|wasm||[issue-354408144](v8/issue-354408144.md)|Function signature confusion||
|O|wasm||[CVE-2024-7024](v8/CVE-2024-7024.md)|Inappropriate implementation||
|O|wasm||[issue-369748454](v8/issue-369748454.md)|Inappropriate implementation||
|X|wasm|GC|[CVE-2024-3156](v8/CVE-2024-3156.md)|Inappropriate implementation||
|O|wasm|Runtime|[issue-361862752](v8/issue-361862752.md)|Function signature confusion||
|*|wasm|Builder|[CVE-2024-6779](v8/CVE-2024-6779.md)|Out of Bounds||
|▵|wasm||[issue-348084786](v8/issue-348084786.md)|Type confusion||
|O|wasm|Liftoff|[issue-350292240](v8/issue-350292240.md)|Function signature confusion|||
||wasm|Liftoff|[issue-421403261](v8/SBX/issue-421403261.md)|Type confusion||
|O|wasm||[CVE-2024-8194](v8/CVE-2024-8194.md)|Type confusion||
||wasm||[CVE-2024-11395](v8/CVE-2024-11395.md)|Type confusion||
||wasm||[issue-394120667](v8/issue-394120667.md)|||
|O|Runtime|Baseline|[issue-417636716](v8/issue-417636716.md)|Function signature confusion||
|X|Runtime|Leaptiering|[issue-342297062](v8/issue-342297062.md)|Function signature confusion||
||Runtime|Heap|[issue-389713719](v8/issue-389713719.md)|Out of bound write||
|▵|Runtime|TypedArrays|[issue-385775375](v8/issue-385775375.md)|Double fetch||
|X|||[issue-389970331](v8/issue-389970331.md)|Stack buffer overflow||
||||[issue-412741811](v8/issue-412741811.md)|Out of Bound read||
||||[issue-384186547](v8/issue-384186547.md)|Use after free||
||Runtime||[issue-338381304](v8/issue-338381304.md)|Stack corruption||
|O|||[issue-395659804](v8/issue-395659804.md)|Type confusion||
||Regexp||[issue-330404819](v8/issue-330404819.md)|Out of Bounds||
|O|Torque|SortState|[issue-390639820](v8/issue-390639820.md)|Type confusion||
|O|Torque||[issue-391169061](v8/issue-391169061.md)|Double fetch||
||JSON||[issue-396446145](v8/issue-396446145.md)|Out of bound write||
||TurboFan|Boilerplate|[issue-395895382](v8/issue-395895382.md)|Out of bound write||
|O|TurboFan||[issue-420637585](v8/issue-420637585.md)|||
||||[issue-411598604](v8/issue-411598604.md)|Use after free||
||||[issue-435630461](v8/SBX/issue-435630461.md)||
||||[issue-443772809](v8/SBX/issue-443772809.md)|||
||||[issue-430960844](v8/SBX/issue-430960844.md)|||



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
||Mojo||[(19)75.0.3770.89](SBX/75.0.3770.89.md)|Use after free|All|Refactoring|
|O|Mojo||[CVE-2019-13768](SBX/CVE-2019-13768.md)|Use after free|Windows|Mark Brand|
|O|Mojo||[20-issue-1062091](SBX/20-issue-1062091.md)|Use after free|All||
||Mojo||[CVE-2020-16045](SBX/CVE-2020-16045.md)|Use after free|Android||
|O|Mojo||[CVE-2021-30633](SBX/CVE-2021-30633.md)|Use after free||
|O|Mojo||[CVE-2022-3075](SBX/CVE-2022-3075.md)|Insufficient data validation|All||
||Mojo||[CVE-2022-4178](SBX/CVE-2022-4178.md)|Use after free|All||
||Mojo||[CVE-2023-6347](SBX/CVE-2023-6347.md)|Use after free||
|X|Mojo||[CVE-2023-0941](SBX/CVE-2023-0941.md)|Use after free|||
||Mojo||[CVE-2023-5218](SBX/CVE-2023-5218.md)|Use after free|||
||Mojo||[CVE-2023-2934](SBX/CVE-2023-2934.md)|TOCTOU|All||
|▵|Mojo|C++|[CVE-2021-21146](SBX/CVE-2021-21146.md)|Use after free|All||
|X|Mojo|C++|[CVE-2021-30528](SBX/CVE-2021-30528.md)|Use after free|Android||
||Mojo|RFH|[20-issue-1068395](SBX/20-issue-1068395.md)|Use after free|Android||
||Mojo|IPCZ|[22-issue-40062130](SBX/22-issue-40062130.md)|Use after free|All||
||Mojo||[22-issue-40061915](SBX/22-issue-40061915.md)|Use after free|All||
||Mojo|MojoPipe|[CVE-2023-6347](SBX/CVE-2023-6347.md)|Use after free|All||
|X|Mojo|Prompts|[CVE-2023-0941](SBX/CVE-2023-0941.md)|Use after free|All||
|X|Mojo|Site Isolation|[CVE-2023-5218](SBX/CVE-2023-5218.md)|Use after free|All||
||Mojo|Visuals|[CVE-2024-3157](SBX/CVE-2024-3157.md)|Out of bounds|All||
|▵|Mojo|Visuals|[CVE-2024-4671](SBX/CVE-2024-4671.md)|Use after free|All||
|O|ANGLE|SwiftShader|[CVE-2023-1818](SBX/CVE-2023-1818.md)|Use after free|All||
||ANGLE|SwiftShader|[CVE-2018-16069](SBX/CVE-2018-16069.md)|Heap buf overflow|||
||ANGLE|SwiftShader|[CVE-2022-4135](SBX/CVE-2022-4135.md)|Heap buf overflow||
||ANGLE|SwiftShader|[CVE-2023-2929](SBX/CVE-2023-2929.md)|Out of bound write|||
|O|ANGLE|SwiftShader|[CVE-2023-4072](CVE-2023-4072.md)|Out of bounds|All||
||ANGLE|SwiftShader|[23-issue-40063963](SBX/23-issue-40063963.md)|Integer overflow|All||
|X|ANGLE|Translator|[CVE-2024-3516](SBX/CVE-2024-3516.md)|Heap buffer overflow|||
||ANGLE|Vulkan|[CVE-2024-2883](SBX/CVE-2024-2883.md)|Use after free|||
||ANGLE||[CVE-2023-1534](SBX/CVE-2023-1534.md)|Out of bound read|All||
|X|ANGLE|SwiftShader|[CVE-2024-4058](SBX/CVE-2024-4058.md)|Type confusion|All||
||ANGLE||[CVE-2016-1649](SBX/CVE-2016-1649.md)|Heap buf overflow|||
||Skia||[CVE-2023-2136](SBX/CVE-2023-2136.md)|Integer overflow|Android||
||Skia||[CVE-2023-4354](SBX/CVE-2023-4354.md)|Heap buf overflow||
||Skia||[CVE-2023-6345](SBX/CVE-2023-6345.md)|Integer overflow|||
||Skia|Tag|[CVE-2018-6126](SBX/CVE-2018-6126.md)|Heap buf overflow|All||
||Skia||[CVE-2021-37981](SBX/CVE-2021-37981.md)|Heap buf overflow||
||Skia||[CVE-2023-4354](SBX/CVE-2023-4354.md)|Heap buf overflow|All||
||Skia||[CVE-2023-6345](SBX/CVE-2023-6345.md)|Integer overflow|||
||appcache||[2018-Hack2Win](SBX/2018-Hack2Win.md)|Use after free|Windows||
||WebRTC||[CVE-2023-7024](SBX/CVE-2023-7024.md)|Heap buf overflow|||
||COM||[CVE-2023-36719](SBX/CVE-2023-36719.md)|Use after free|Windows||
||Kernel|NTOS|[CVE-2023–21674](SBX/CVE-2023–21674.md)|Use after free|Windows||
||Driver|Binder|[CVE-2020-0041](SBX/CVE-2020-0041.md)|Use after free|Android||
|||Model|[CVE-2021-21201](SBX/CVE-2021-21201.md)|Use after free|All||
||||[23-issue-40063125](SBX/23-issue-40063125.md)|Use after free|All||
|||Site Isolation|[CVE-2020-16017](SBX/CVE-2020-16017.md)|Use after free||
|||Site Isolation|[CVE-2022-0290](SBX/CVE-2022-0290.md)|Use after free||
|||Navigation|[CVE-2023-2721](SBX/CVE-2023-2721.md)|Use after free|All||
||Extension|DevTools|[CVE-2024-5836](SBX/CVE-2024-5836.md)|Race condition|All||

# Safari
## Safari_JavaScriptCore_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Safari/jsc/Utils.md)|N/A||
|O|Array.slice|Side effect|[CVE-2016-4622](Safari/jsc/CVE-2016-4622.md)|Out of bounds|Phrack70|
|O|Array.reverse||[CVE-2018-4192](Safari/jsc/CVE-2018-4192.md)|Use after free|pwn2own-2018|

## Safari_SBX
|Pwn|Target|Feature|CVE/issue|Vulnerability|OS|Comment|
|---|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Safari/SBX/Utils.md)|N/A|||
|O|WindowServer||[CVE-2018-4193](Safari/SBX/CVE-2018-4193.md)|Out of bounds|Mac|pwn2own-2018|
||SharedFileList||[CVE-2024-54498](Safari/SBX/CVE-2024-54498.md)|A path handling issue|Mac|
||WebGPU||[CVE-2023-28205](Safari/SBX/CVE-2023-28205.md)|Use after free|iOS|Project zero|

# Firefox
## Firefox_Gecko_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Firefox/Gecko/Utils.md)|N/A||
|O|SpiderMonkey|Side effect|[CVE-2024-8381](Firefox/Gecko/CVE-2024-8381.md)|Type confusion||


## Firefox_Renderer_RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|[Utils](Firefox/Renderer/Utils.md)|N/A||
||||[CVE-2022-1802](Firefox/Renderer/CVE-2022-1802.md)|Out of bounds|pwn2own-2022|
