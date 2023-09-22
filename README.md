# @redplc/node-red-redplc

[![platform](https://img.shields.io/badge/platform-Node--RED-red)](https://nodered.org)
[![platform](https://img.shields.io/badge/platform-redPlc-ffa500)](https://flows.nodered.org/node/@redplc/node-red-redplc/)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZDRCZBQFWV3A6)

Node-Red nodes for the realization of Software-PLC with Ladder-Logic

#### Documentation and examples can be found here:
https://github.com/redplc/automation_using_nodered

## Nodes
- **contact**: Ladder Logic Contact.
- **coil**: Ladder Logic Coil.
- **function**: Ladder Logic Digital Function.
- **counter**: Ladder Logic Counter Coil.
- **timer**: Ladder Logic Timer Coil.
- **flipflop**: Ladder Logic FlipFlop.
- **move**: Ladder Logic Move.
- **math**: Ladder Logic Calculation.
- **scale**: Ladder Logic Scale.
- **compare**: Ladder Logic Compare.
- **M memory**: Digital (M) Memory Variable.
- **MA memory**: Analog (MA) Memory Variable.
- **s-inject**: Sequential Inject.
- **onstart**: Execute On Start.
- **firstscan**: Execute On First Scan.
- **rail**: Ladder Logic Rail.
- **import**: Import Data.
- **export**: Export Data.


## Detail

redPlc nodes implements Software PLC functionality in Node-Red.<br>
The control logic is realized as [ladder logic](https://en.wikipedia.org/wiki/Ladder_logic) (LD) according standard IEC 61131-3.<br>
Modules are nodes that use hardware or communication and updates the redPlc variables.<br>
Variables are stored in Node-Red global context memory as arrays:

|Variable|Function|Array Of|Created by|
|---|---|---|---|
|**I**|Digital Input|Boolean|Digital Input Modules|
|**Q**|Digital Output|Boolean|Digital Output Modules|
|**M**|Digital Memory|Boolean|Memory Node|
|**C**|Counter|Boolean/Number|Counter Node|
|**T**|Timer|Boolean/Number|Timer Node|
|**FF**|Flip-Flop|Boolean|Flip-Flop Node|
|**IA**|Analog Input|Number|Analog Input Modules|
|**QA**|Analog Output|Number|Analog Output Modules|
|**MA**|Analog Memory|Number|Memory Node|

The variable notation is [variable][address].[index]<br>
where maximum address is 999 and index is 63.<br>
Example for Digital Input: **I5.3**<br>
Some indexes also have symbolic names: **C0.CV** (Counter Value).<br>
Unused array elements are set to **undefined**.

