- [Chrome](#Chrome)
	- [Chrome V8 RCE](<#Chrome V8 RCE>)
	- [Chrome V8 Sandbox bypass](<#Chrome V8 Sandbox bypass>)
	- [Chrome Renderer RCE](<#Chrome Renderer RCE>)
	- [Chrome sandbox escape](<#Chrome sandbox escape>)
- [Safari](#Safari)
	- [Safari JavaScriptCore RCE](<#Safari JavaScriptCore RCE>)
	- [Safari SBX](<#Safari SBX>)
- [Firefox](#Firefox)
	- [Firefox Gecko RCE](<#Firefox Gecko RCE>)
	- [Firefox Renderer RCE](<#Firefox Renderer RCE>)

# Chrome
## Chrome V8 RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A||
||wasm||CVE-2017-5122|Out of bound read||
||wasm|Side effect|CVE-2018-6122|Type confusion||
||wasm||CVE-2024-3832|Type confusion||
|O|wasm||CVE-2023-4070|Type confusion||
|O|wasm||CVE-2024-2887|Type confusion||
|O|wasm|Stack switching|CVE-2024-8904|Type confusion||
||wasm|Stack switching|issue-393557652|Race condition ||
||wasm|Stack switching|CVE-2025-5959|Type confusion||
|O|wasm|TierUp|CVE-2024-10230|Type confusion||
|▵|wasm||CVE-2024-4761|Out of bound write||
|▵|wasm||issue-339736513| Type confusion||
||wasm||CVE-2024-6100|Type confusion||
||wasm||CVE-2024-5158|Type confusion||
||wasm|Turboshaft|issue-352720899|Type confusion||
|▵|wasm|Turboshaft|issue-373703277|Type confusion||
||wasm|Turboshaft|CVE-2024-12381|Type confusion||
||wasm|Turboshaft|CVE-2025-0291|Type confusion||
||wasm|Liftoff|CVE-2024-7971|Type confusion||
||wasm||issue-40647140|Integer truncation||
||wasm||CVE-2024-10231|Type confusion||
||wasm|Torque|CVE-2024-12053|Type confusion||
||wasm||CVE-2025-5959|Type confusion||
||wasm|DrumBrake|issue-482742896|Use after free||
|O|TurboFan|Concurrent compilation|CVE-2023-3420|Type confusion||
|O|TurboFan|Side effect|CVE-2018-17463|Type confusion||
|O|TurboFan|Property access|CVE-2021-30632||
||TurboFan|Node properties|CVE-2025-2135|Type Confusion||
|O|TurboFan|js-inlining|CVE-2025-0612|Out of bounds||
||TurboFan|Turboshaft|CVE-2025-5419|Out of bounds||
||TurboFan|Value serializer|CVE-2023-1214|Type confusion||
|O|TurboFan||CVE-2023-4762|Type confusion||
|O|TurboFan||CVE-2022-1364|Type confusion||
||TurboFan|TryFastAddDataProperty|CVE-2024-5830|Type confusion||
|▵|TurboFan|TryFastAddDataProperty|CVE-2026-11645|Out of bounds||
|O|Maglev|MaglevGraphBuilder|CVE-2024-4947|Type confusion||
|O|Maglev|MaglevGraphBuilder|CVE-2023-4069|Type confusion||
|O|Maglev|MaglevGraphBuilder|CVE-2024-4947|Type confusion|||
||Maglev|graph construction|issue-386565144|Incorrect node||
||Maglev|LateLoadElimination|issue-480438199|Type confusion||
||Maglev||CVE-2026-7337|Type confusion||
|O|||CVE-2017-5030|Out of bound read||
|O|||18-issue-880207|Type confusion||
|O|||CVE-2019-5825|Type confusion||
|O|||CVE-2020-6383|Type confusion||
|O|||CVE-2021-21225|Out of bound read||
|O|Runtime||CVE-2021-38003|Type confusion||
|O|||CVE-2022-1310|Use after free||
|O|Runtime||CVE-2022-4174|Type confusion||
|O|Runtime|builtins|CVE-2023-2033|Type confusion||
|O|Runtime||CVE-2023-3079|Type confusion||
||||CVE-2023-3420|Type confusion||
||||CVE-2024-4761|Out of bound write||
||Runtime|Interpreter|CVE-2025-6554|Type confusion||
||Runtime|Interpreter|CVE-2025-0434|Out of bounds||
|O|Runtime|enum cache|CVE-2023-4427|Out of bound read||
||Runtime|enum cache|CVE-2024-3159|Out of bound read||
||Runtime||CVE-2025-0445|Use after free||
||Runtime||CVE-2026-0899|Out of bounds||
||||CVE-2024-0517|Out of bounds||
||||CVE-2024-0519|Out of bounds|||
|O|Parser|Incorrect parsing|CVE-2024-5274|Type confusion||
|O|Parser|Incorrect parsing|issue-379774687|Type confusion||
||||issue-384549659|||
||||CVE-2025-9864|Use after free||
||Torque||issue-380677637|Type confusion||

## Chrome V8 Sandbox bypass
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|O|N/A||v8sbx|N/A||
|O|Runtime||my-v8sbx-bug|Insufficient data validation||
||wasm||issue-349529650|Function import signature check race||
|O|wasm||issue-336009921|Function signature confusion||
|O|wasm||issue-354408144|Function signature confusion||
|O|wasm||CVE-2024-7024|Inappropriate implementation||
|O|wasm||issue-369748454|Inappropriate implementation||
|X|wasm|GC|CVE-2024-3156|Inappropriate implementation||
|O|wasm|Runtime|issue-361862752|Function signature confusion||
|▵|wasm|Builder|CVE-2024-6779|Out of Bounds||
|▵|wasm||issue-348084786|Type confusion||
|O|wasm|Liftoff|issue-350292240|Function signature confusion|||
||wasm|Liftoff|issue-421403261|Type confusion||
|O|wasm||CVE-2024-8194|Type confusion||
||wasm||CVE-2024-11395|Type confusion||
||wasm||issue-394120667|||
||wasm||issue-432289371|Function signature confusion||
||Wasm||issue-430960844|Type confusion||
||wasm||issue-480579170|Inappropriate implementation||
||wasm|protected_uses|issue-483220222|Inappropriate implementation||
||wasm|WasmDispatchTable|issue-503422307|Reuse unpublished WasmDispatchTable||
|O|Runtime|Baseline|issue-417636716|Function signature confusion||
|X|Runtime|Leaptiering|issue-342297062|Function signature confusion||
||Runtime|Heap|issue-389713719|Out of bound write||
|▵|Runtime|TypedArrays|issue-385775375|Double fetch||
||Runtime||issue-338381304|Stack corruption||
||Runtime|JSDispatchEntry|issue-443772809||
||Runtime|DebugBreakTrampoline|issue-435630467|Inappropriate implementation||
||Runtime||issue-487213150|Type confusion||
|O|Runtime|Deoptimization|issue-395659804|Type confusion||
|X|BigInt||issue-389970331|Stack buffer overflow||
||BigInt||issue-490769268|Heap buffer overflow||
||||issue-412741811|Out of Bound read||
||||issue-384186547|Use after free||
||Regexp||issue-330404819|Out of Bounds||
|O|Torque|SortState|issue-390639820|Type confusion||
|O|Torque||issue-391169061|Double fetch||
||JSON||issue-396446145|Out of bound write||
||TurboFan|Boilerplate|issue-395895382|Out of bound write||
|O|TurboFan||issue-420637585|Type confusion||
||||issue-411598604|Use after free||
||||issue-435630461|Double fetch||
||GC||issue-462217236|Use after free||

## Chrome Renderer RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A||
|O|||CVE-2021-30551|Type confusion||
|O|||issue-1352549|Type confusion||
||||CVE-2024-1669|Out of bound read||
|O|image-decoders|BMP image|CVE-2024-1283|Heap buffer overflow||
||Compositing||CVE-2024-3157|Out of bound write||
||wasm||issue-433533359|Race condition||
||Dawn|WebGPU|CVE-2026-5281|Use after free||
||IndexedDB||CVE-2025-11460|Use after free||

## Chrome sandbox escape
|Pwn|Target|Feature|CVE/issue|Vulnerability|OS|Comment|
|---|---|---|---|---|---|---|
|N|N/A|N/A|Utils|N/A|N/A||
|N|ANGLE|N/A|Collection|Heap buffer overflow|N/A||
|N|Mojo|N/A|Mojo|N/A|N/A||
||Mojo||19-75.0.3770.89|Use after free|All||
|O|Mojo||CVE-2019-13768|Use after free|Windows||
|O|Mojo||20-issue-1062091|Use after free|All||
|▵|Mojo|AI|CVE-2024-9954|Use after free|All||
||Mojo||CVE-2020-16045|Use after free|Android||
|O|Mojo||CVE-2021-30633|Use after free||
|O|Mojo||CVE-2022-3075|Insufficient data validation|All||
||Mojo||CVE-2022-4178|Use after free|All||
||Mojo||CVE-2023-6347|Use after free||
|X|Mojo||CVE-2023-0941|Use after free|||
||Mojo||CVE-2023-5218|Use after free|||
||Mojo|Deserialize|CVE-2022-0797|Out of bounds|All||
|▵|Mojo|Deserialize|CVE-2023-2934|TOCTOU|All||
|▵|Mojo|C++|CVE-2021-21146|Use after free|All||
|X|Mojo|C++|CVE-2021-30528|Use after free|Android||
||Mojo|RFH|20-issue-1068395|Use after free|Android||
||Mojo|IPCZ|issue-40062130|Use after free|All||
||Mojo||issue-40061915|Use after free|All||
||Mojo|MojoPipe|CVE-2023-6347|Use after free|All||
|X|Mojo|Prompts|CVE-2023-0941|Use after free|All||
|X|Mojo|Site Isolation|CVE-2023-5218|Use after free|All||
||Mojo|Visuals|CVE-2024-3157|Out of bounds|All||
|▵|Mojo|Visuals|CVE-2024-4671|Use after free|All||
||Mojo|Visuals|issue-397601495|Use after free|All||
||Mojo||CVE-2025-2783|Incorrect handle|Windows||
||Mojo||issue-453094710|Out of bound read|All||
|O|ANGLE|SwiftShader|CVE-2023-1818|Use after free|All||
||ANGLE|SwiftShader|CVE-2018-16069|Heap buffer overflow|||
||ANGLE|SwiftShader|CVE-2022-0789|Heap buffer overflow|All||
|▵|ANGLE|SwiftShader|CVE-2022-4135|Heap buffer overflow||
||ANGLE|SwiftShader|CVE-2023-2929|Out of bound write|||
|O|ANGLE|SwiftShader|CVE-2023-4072|Out of bounds|All||
||ANGLE|SwiftShader|issue-40063963|Integer overflow|All||
|X|ANGLE|SwiftShader|CVE-2024-4058|Type confusion|All||
|X|ANGLE|Translator|CVE-2024-3516|Heap buffer overflow|||
||ANGLE|Vulkan|CVE-2024-2883|Use after free|||
||ANGLE|Vulkan|CVE-2026-3536|Integer overflow|All||
||ANGLE||CVE-2023-1534|Out of bound read|All||
||ANGLE||CVE-2016-1649|Heap buffer overflow|||
|O|ANGLE||CVE-2025-1426|Heap buffer overflow|All||
||ANGLE|WebGL|CVE-2026-4440|Out of bounds|All||
|▵|ANGLE|Qualcomm|CVE-2025-27038|Use after free|Android||
|▵|ANGLE||CVE-2025-6558|Incorrect validation|Android||
||Skia||CVE-2023-2136|Integer overflow|Android||
||Skia||CVE-2023-4354|Heap buffer overflow||
||Skia||CVE-2023-6345|Integer overflow|||
||Skia|Tag|CVE-2018-6126|Heap buffer overflow|All||
||Skia||CVE-2021-37981|Heap buffer overflow||
||Skia||CVE-2023-4354|Heap buffer overflow|All||
||Skia||CVE-2023-6345|Integer overflow|||
|▵|Skia||CVE-2026-3538|Integer overflow|||
||appcache||2018-Hack2Win|Use after free|Windows||
||WebRTC||CVE-2023-7024|Heap buffer overflow|||
||Kernel|Binder|CVE-2020-0041|Use after free|Android||
|||Model|CVE-2021-21201|Use after free|All||
||||issue-40063125|Use after free|All||
|||Site Isolation|CVE-2020-16017|Use after free||
|||Site Isolation|CVE-2022-0290|Use after free||
||Navigation||CVE-2023-2721|Use after free|All||
||Navigation||CVE-2026-3545|Insufficient data validation|All||
||Extension|DevTools|CVE-2024-5836|Race condition|All||
||WebAudio||CVE-2020-6449|Use after free|All||
||Views|File|CVE-2024-11114|Inappropriate implementation|Windows||
||COM||CVE-2023-36719|Use after free|Windows||
||StateRepository|AppXSvc|CVE-2020-1124|Improperly handles|Windows||
||StateRepository|AppXSvc|CVE-2020-1186|Improperly handles|Windows||
||StateRepository|AppXSvc|CVE-2024-35265||Windows||
||StateRepository|AppXSvc|CVE-2020-1185||Windows||
||StateRepository|AppXSvc|CVE-2025-49723|Server file tampering|Windows||
||StateRepository|AppXSvc|CVE-2022-21863||Windows||
|▵|StateRepository|AppXSvc|CVE-2025-53789|Missing authentication|Windows||
||StateRepository|AppXSvc|CVE-2025-59203|An information disclosure|Windows||
||UUS/WUSvc||CVE-2020-1305|Initialize(),Undo() logic error|Windows||
||UsoSvc||CVE-2020-1313||Windows||
||AppXSvc||CVE-2019-1253|Inappropriate implementation|Windows||
||AppXSvc||CVE-2019-1385||Windows||
||AppXSvc||CVE-2019-0841||Windows||
||Kernel|NTOS|CVE-2023–21674|Use after free|Windows||
|▵|kernel|ntoskrnl|CVE-2026-40369|Untrusted pointer dereference|Windows||
|O|Blink|WindowDialog|CVE-2026-3924|Use after free|All||

# Safari

## Safari JavaScriptCore RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A||
|O|Array.slice|Side effect|CVE-2016-4622|Out of bounds||
|O|Array.reverse||CVE-2018-4192|Use after free||

## Safari SBX
|Pwn|Target|Feature|CVE/issue|Vulnerability|OS|Comment|
|---|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A|||
|O|WindowServer||CVE-2018-4193|Out of bounds|Mac||
||WindowServer||CVE-2018-4237||Mac||
||SharedFileList||CVE-2024-54498|A path handling issue||
||WebGPU||CVE-2023-28205|Use after free|iOS||

# Firefox
## Firefox Gecko RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A||
|O|SpiderMonkey|Side effect|CVE-2024-8381|Type confusion||

## Firefox Renderer RCE
|Pwn|Target|Feature|CVE/issue|Vulnerability|Comment|
|---|---|---|---|---|---|
|N/A|N/A|N/A|Utils|N/A||
||||CVE-2022-1802|Out of bounds||
