---
title: Schtasks.exe
description: 可讓系統管理員在本機或遠端電腦上建立、刪除、查詢、變更、執行和結束排定的工作。
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe 工作排程器
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1c9ba2c13053a8c550128f5d66623b5eed3a9dec
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314631"
---
# <a name="schtasksexe"></a>Schtasks.exe

可讓系統管理員在本機或遠端電腦上建立、刪除、查詢、變更、執行和結束排定的工作。 執行不含引數的 Schtasks.exe 會顯示每個已註冊工作的狀態和下次執行時間。 

如需工作排程器的詳細資訊，請參閱這篇簡介： [適用于開發人員的工作排程器](task-scheduler-start-page.md)。

## <a name="creating-a-task"></a>建立工作

下列語法用來在本機或遠端電腦上建立工作。

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/Ru** 使用者 **名稱**
</dt> <dd>

值，這個值會指定工作執行所在的使用者內容。 系統帳戶的有效值為 ""、"NT 授權單位 \\ system" 或 "system"。 針對工作排程器2.0 工作，「NT 授權單位 \\ LOCALSERVICE」和「NT 授權單位 NETWORKSERVICE」 \\ 也是有效的值。

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/Rp** **\[ 密碼 \]**
</dt> <dd>

值，指定使用/RU 參數指定之使用者的密碼。 若要提示輸入密碼，此值必須是 " \* " 或無值。 系統帳戶會忽略此密碼。 此參數必須與/RU 或/XML 參數結合。

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **排程**
</dt> <dd>

指定排程頻率的值。 有效的值為： MINUTE、每小時、每日、每週、每月、一次、整理、ONIDLE 和 ONEVENT。

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** **修飾** 詞
</dt> <dd>

值，這個值會調整排程類型，以允許更精確地控制排程週期。 有效值為：

-   分鐘： 1-1439 分鐘。
-   每小時： 1-23 小時。
-   每日： 1-365 天。
-   每週：每週 1-52。
-   一次：無修飾詞。
-   ONSTART：無修飾詞。
-   整理：無修飾詞。
-   ONIDLE：無修飾詞。
-   每月： 1-12、第二、第二、第三、第四、最後和 LASTDAY。
-   ONEVENT： XPath 事件查詢字串。

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **天**
</dt> <dd>

值，指定執行工作的周中日。 有效值為：週一、週二、週三、星期四、星期五、週六、周日和每月排程 1-31 (每月的日期) 。 萬用字元 (\*) 指定所有天數。

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **個月**
</dt> <dd>

指定年度月份的值。 預設為當月的第一天。 有效值為： JAN、二月、MAR、四月、5月、六月、七月、8月、SEP、OCT、11月和 DEC。 萬用字元 (\*) 指定所有月份。

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**
</dt> <dd>

值，指定執行排定的 ONIDLE 工作之前要等待的閒置時間量。 有效範圍是 1-999 分鐘。

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定可唯一識別已排程工作的名稱。

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** **/tr**
</dt> <dd>

值，指定要在排程時間執行之工作的路徑和檔案名。 例如： C： \\ Windows \\ System32 \\calc.exe。

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **starttime**
</dt> <dd>

值，指定執行工作的開始時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:30 會指定2：30PM。 預設值是未指定/ST 的目前時間。 此選項是/SC 一次引數的必要項。

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **間隔**
</dt> <dd>

指定重複間隔（以分鐘為單位）的值。 這不適用於下列排程類型： MINUTE、每小時、ONSTART、整理、ONIDLE 和 ONEVENT。 有效範圍是 1-599940 分鐘。 如果指定了/ET 或/DU 參數，預設值為10分鐘。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **endtime**
</dt> <dd>

值，指定執行工作的結束時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:50 會指定2：50PM。 這不適用於下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **持續時間**
</dt> <dd>

值，指定執行工作的持續時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:50 會指定2：50PM。 這不適用於/ET 和下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。 針對 (工作排程器1.0 工作的/V1 工作) ，如果指定/RI，則持續時間預設值為一小時。

**WINDOWS XP：** 此選項無法使用。

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

值，這個值會在結束時間或持續時間結束工作。 這不適用於下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。 必須指定/ET 或/DU。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/Sd** 開始 **日期**
</dt> <dd>

值，指定要在其上執行工作的第一個日期。 格式為 mm/dd/yyyy。 此值預設為目前的日期。 這不適用於下列排程類型：一次、ONSTART、整理、ONIDLE 和 ONEVENT。

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **結束** 日期
</dt> <dd>

值，指定工作將執行的最後日期。 格式為 mm/dd/yyyy。 這不適用於下列排程類型：一次、ONSTART、整理、ONIDLE 和 ONEVENT。

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

值，指定 ONEVENT 觸發程式的事件通道。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

值，只有在工作執行時，如果/RU 使用者目前登入，才讓工作以互動方式執行。 只有在使用者登入時才會執行此工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

指出未儲存任何密碼的值。 此工作不會以互動方式執行為指定的使用者。 只有本機資源可以使用。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

值，這個值會標記要在其最終執行之後刪除的工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/Xml** **xmlfile**
</dt> <dd>

從 XML 檔案建立工作的值。 此參數可以與/RU 和/RP 參數結合，或在工作 XML 已包含主體時，單獨使用/RP 參數。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

此值會建立 Windows 2000、Windows Server 2003 和 Windows XP 平臺可以看見的工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

強制建立工作的值，如果指定的工作已存在，則會隱藏警告。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **層級**
</dt> <dd>

值，這個值會設定工作的執行層級。 有效的值為受限和最高。 預設值為 [有限]。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

值，指定在引發觸發程式之後，延遲工作的等候時間。 時間格式為 mmmm： ss。 此選項只適用于排程類型 ONSTART、整理和 ONEVENT。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

值，顯示 Schtasks.exe 的說明訊息。

</dd> </dl>

## <a name="remarks"></a>備註

在 Windows XP、Windows Server 2003 或 Windows 2000 作業系統上執行的遠端電腦上建立工作時，請使用/V1 參數。

如果遠端電腦已啟用 [檔案及印表機共用] 防火牆例外，且已停用 [遠端排程工作管理] 防火牆例外，您就無法建立非互動式遠端工作排程器1.0 工作 (使用/IT 參數建立工作，並使用/V1 參數) 。

## <a name="deleting-a-task"></a>刪除工作

下列語法用來刪除一或多個排程工作。

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定要刪除之排程工作的名稱。 您 \* 可以使用萬用字元 () 來刪除所有工作。

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

強制刪除工作的值，如果指定的工作正在執行，則隱藏警告。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示 Schtasks.exe 說明的值。

</dd> </dl>

## <a name="running-a-task"></a>正在執行工作

下列語法可用來立即執行排程工作。

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定要執行之排程工作的名稱。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示 Schtasks.exe 說明的值。

</dd> </dl>

## <a name="ending-a-running-task"></a>結束正在執行的工作

下列語法用來停止執行中的排程工作。

> [!Note]  
> 若要停止執行遠端工作，請確定遠端電腦已啟用 [檔案及印表機共用] 和 [遠端排程工作] 管理防火牆例外。

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定要停止之排程工作的名稱。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示 Schtasks.exe 說明的值。

</dd> </dl>

## <a name="querying-for-task-information"></a>查詢工作資訊

下列語法用來顯示本機或遠端電腦上的排程工作。

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/Fo** **格式**
</dt> <dd>

指定輸出格式的值。 有效的值為 TABLE、LIST 和 CSV。

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

值，指定不應該在輸出中顯示資料行標題。 這僅適用于資料表和 CSV 格式。

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

顯示詳細資訊工作輸出的值。

> [!Note]  
> 如果工作排定為僅執行一次，則顯示的排程資訊為「無法使用此格式的資料。」

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定要取得其資訊的工作名稱。 如果未指定工作名稱，則會顯示所有工作的資訊。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

值，用來顯示 XML 格式的工作定義。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

用來顯示 Schtasks.exe 說明的值。

</dd> </dl>

## <a name="changing-a-task"></a>變更工作

下列語法用來變更程式執行的方式，或變更排程工作所使用的使用者帳戶和密碼。

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**
</dt> <dd>

值，指定要連接的遠端電腦。 如果省略，系統參數會預設為本機電腦。

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**
</dt> <dd>

值，指定 Schtasks.exe 應該在其上執行的使用者內容。

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**
</dt> <dd>

值，指定指定使用者內容的密碼。 如果省略，Schtasks.exe 會提示使用者輸入。

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**
</dt> <dd>

值，指定要變更的排程工作。

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **runasuser**
</dt> <dd>

值，這個值會變更排定的工作將在其中執行的使用者名稱 (使用者內容) 。 系統帳戶的有效值為 ""、"NT 授權單位 \\ system" 或 "system"。 針對工作排程器2.0 工作，「NT 授權單位 \\ LOCALSERVICE」和「NT 授權單位 NETWORKSERVICE」 \\ 也是有效的值。

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/Rp** **runaspassword**
</dt> <dd>

值，指定現有使用者內容的新密碼或新使用者帳戶的密碼。 系統帳戶會忽略此密碼。

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** **/tr**
</dt> <dd>

值，指定工作將執行的新程式。

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **starttime**
</dt> <dd>

值，指定執行工作的開始時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:30 會指定2：30PM。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **間隔**
</dt> <dd>

值，指定重複間隔（以分鐘為單位）。 有效範圍是 1-599940 分鐘。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **endtime**
</dt> <dd>

值，指定工作的結束時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:50 會指定2：50PM。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **持續時間**
</dt> <dd>

值，指定執行工作的持續時間。 時間格式為 HH： mm (24 小時的時間) 。 例如，14:50 會指定2：50PM。 這不適用於/ET 參數。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

值，這個值會在結束時間或持續時間結束工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/Sd** 開始 **日期**
</dt> <dd>

值，指定要在其上執行工作的第一個日期。 格式為 mm/dd/yyyy。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **結束** 日期
</dt> <dd>

值，指定工作將執行的最後日期。 格式為 mm/dd/yyyy。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

值，只有在工作執行時，如果/RU 使用者目前登入，才讓工作以互動方式執行。 只有在使用者登入時才會執行此工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **層級**
</dt> <dd>

值，這個值會設定工作的執行層級。 有效的值為受限和最高。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

啟用排程工作的值。 啟用的工作可以執行，而且無法執行已停用的工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

值，這個值會停用執行中的排程工作。

> [!Note]  
> 如果 Schtasks.exe 停用遠端工作排程器1.0 工作，且遠端電腦已啟用 [檔案及印表機共用] 防火牆例外，而 [遠端排程工作管理防火牆] 例外已停用，則從工作排程器 2.0 API 讀取時，不會停用此工作。

 

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

值，這個值會標記要在其最終執行之後刪除的工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

值，指定引發觸發程式之後，順延強制工作的等候時間。 時間格式為 mmmm： ss。 此選項僅適用于排程類型為 ONSTART、整理和 ONEVENT 的工作。

**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

值，顯示 Schtasks.exe 的說明訊息。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



 

 





