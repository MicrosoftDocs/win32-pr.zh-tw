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
# <a name="schtasksexe"></a><span data-ttu-id="e71cf-104">Schtasks.exe</span><span class="sxs-lookup"><span data-stu-id="e71cf-104">Schtasks.exe</span></span>

<span data-ttu-id="e71cf-105">可讓系統管理員在本機或遠端電腦上建立、刪除、查詢、變更、執行和結束排定的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-105">Enables an administrator to create, delete, query, change, run, and end scheduled tasks on a local or remote computer.</span></span> <span data-ttu-id="e71cf-106">執行不含引數的 Schtasks.exe 會顯示每個已註冊工作的狀態和下次執行時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-106">Running Schtasks.exe without arguments displays the status and next run time for each registered task.</span></span> 

<span data-ttu-id="e71cf-107">如需工作排程器的詳細資訊，請參閱這篇簡介： [適用于開發人員的工作排程器](task-scheduler-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="e71cf-107">For more information on Task Scheduler, see this introduction: [Task Scheduler for developers](task-scheduler-start-page.md).</span></span>

## <a name="creating-a-task"></a><span data-ttu-id="e71cf-108">建立工作</span><span class="sxs-lookup"><span data-stu-id="e71cf-108">Creating a Task</span></span>

<span data-ttu-id="e71cf-109">下列語法用來在本機或遠端電腦上建立工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-109">The following syntax is used to create a task on the local or remote computer.</span></span>

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a><span data-ttu-id="e71cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-111"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-112">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-112">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-113">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-113">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-114"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-115">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-115">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-116"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-117">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-117">A value that specifies the password for a given user context.</span></span> <span data-ttu-id="e71cf-118">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-118">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/Ru** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-119"><span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-120">值，這個值會指定工作執行所在的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-120">A value that specifies the user context under which the task runs.</span></span> <span data-ttu-id="e71cf-121">系統帳戶的有效值為 ""、"NT 授權單位 \\ system" 或 "system"。</span><span class="sxs-lookup"><span data-stu-id="e71cf-121">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="e71cf-122">針對工作排程器2.0 工作，「NT 授權單位 \\ LOCALSERVICE」和「NT 授權單位 NETWORKSERVICE」 \\ 也是有效的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-122">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE", and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/Rp** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-123"><span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-124">值，指定使用/RU 參數指定之使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-124">A value that specifies the password for the user specified with the /RU parameter.</span></span> <span data-ttu-id="e71cf-125">若要提示輸入密碼，此值必須是 " \* " 或無值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-125">To prompt for the password, the value must be either "\*" or no value.</span></span> <span data-ttu-id="e71cf-126">系統帳戶會忽略此密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-126">This password is ignored for the system account.</span></span> <span data-ttu-id="e71cf-127">此參數必須與/RU 或/XML 參數結合。</span><span class="sxs-lookup"><span data-stu-id="e71cf-127">This parameter must be combined with either /RU or the /XML switch.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **排程**</span><span class="sxs-lookup"><span data-stu-id="e71cf-128"><span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-129">指定排程頻率的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-129">A value that specifies the schedule frequency.</span></span> <span data-ttu-id="e71cf-130">有效的值為： MINUTE、每小時、每日、每週、每月、一次、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-130">Valid values are: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** **修飾** 詞</span><span class="sxs-lookup"><span data-stu-id="e71cf-131"><span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/MO** **modifier**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-132">值，這個值會調整排程類型，以允許更精確地控制排程週期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-132">A value that refines the schedule type to allow for finer control over the schedule recurrence.</span></span> <span data-ttu-id="e71cf-133">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e71cf-133">Valid values are:</span></span>

-   <span data-ttu-id="e71cf-134">分鐘： 1-1439 分鐘。</span><span class="sxs-lookup"><span data-stu-id="e71cf-134">MINUTE: 1 - 1439 minutes.</span></span>
-   <span data-ttu-id="e71cf-135">每小時： 1-23 小時。</span><span class="sxs-lookup"><span data-stu-id="e71cf-135">HOURLY: 1 - 23 hours.</span></span>
-   <span data-ttu-id="e71cf-136">每日： 1-365 天。</span><span class="sxs-lookup"><span data-stu-id="e71cf-136">DAILY: 1 - 365 days.</span></span>
-   <span data-ttu-id="e71cf-137">每週：每週 1-52。</span><span class="sxs-lookup"><span data-stu-id="e71cf-137">WEEKLY: weeks 1 - 52.</span></span>
-   <span data-ttu-id="e71cf-138">一次：無修飾詞。</span><span class="sxs-lookup"><span data-stu-id="e71cf-138">ONCE: No modifiers.</span></span>
-   <span data-ttu-id="e71cf-139">ONSTART：無修飾詞。</span><span class="sxs-lookup"><span data-stu-id="e71cf-139">ONSTART: No modifiers.</span></span>
-   <span data-ttu-id="e71cf-140">整理：無修飾詞。</span><span class="sxs-lookup"><span data-stu-id="e71cf-140">ONLOGON: No modifiers.</span></span>
-   <span data-ttu-id="e71cf-141">ONIDLE：無修飾詞。</span><span class="sxs-lookup"><span data-stu-id="e71cf-141">ONIDLE: No modifiers.</span></span>
-   <span data-ttu-id="e71cf-142">每月： 1-12、第二、第二、第三、第四、最後和 LASTDAY。</span><span class="sxs-lookup"><span data-stu-id="e71cf-142">MONTHLY: 1 - 12, or FIRST, SECOND, THIRD, FOURTH, LAST, and LASTDAY.</span></span>
-   <span data-ttu-id="e71cf-143">ONEVENT： XPath 事件查詢字串。</span><span class="sxs-lookup"><span data-stu-id="e71cf-143">ONEVENT: XPath event query string.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **天**</span><span class="sxs-lookup"><span data-stu-id="e71cf-144"><span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **days**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-145">值，指定執行工作的周中日。</span><span class="sxs-lookup"><span data-stu-id="e71cf-145">A value that specifies the day of the week to run the task.</span></span> <span data-ttu-id="e71cf-146">有效值為：週一、週二、週三、星期四、星期五、週六、周日和每月排程 1-31 (每月的日期) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-146">Valid values are: MON, TUE, WED, THU, FRI, SAT, SUN and for MONTHLY schedules 1 - 31 (days of the month).</span></span> <span data-ttu-id="e71cf-147">萬用字元 (\*) 指定所有天數。</span><span class="sxs-lookup"><span data-stu-id="e71cf-147">The wildcard character (\*) specifies all days.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **個月**</span><span class="sxs-lookup"><span data-stu-id="e71cf-148"><span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-149">指定年度月份的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-149">A value that specifies months of the year.</span></span> <span data-ttu-id="e71cf-150">預設為當月的第一天。</span><span class="sxs-lookup"><span data-stu-id="e71cf-150">Defaults to the first day of the month.</span></span> <span data-ttu-id="e71cf-151">有效值為： JAN、二月、MAR、四月、5月、六月、七月、8月、SEP、OCT、11月和 DEC。</span><span class="sxs-lookup"><span data-stu-id="e71cf-151">Valid values are: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV, and DEC.</span></span> <span data-ttu-id="e71cf-152">萬用字元 (\*) 指定所有月份。</span><span class="sxs-lookup"><span data-stu-id="e71cf-152">The wildcard character (\*) specifies all months.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-153"><span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-154">值，指定執行排定的 ONIDLE 工作之前要等待的閒置時間量。</span><span class="sxs-lookup"><span data-stu-id="e71cf-154">A value that specifies the amount of idle time to wait before running a scheduled ONIDLE task.</span></span> <span data-ttu-id="e71cf-155">有效範圍是 1-999 分鐘。</span><span class="sxs-lookup"><span data-stu-id="e71cf-155">The valid range is 1 - 999 minutes.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-156"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-157">值，指定可唯一識別已排程工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e71cf-157">A value that specifies a name which uniquely identifies the scheduled task.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** **/tr**</span><span class="sxs-lookup"><span data-stu-id="e71cf-158"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-159">值，指定要在排程時間執行之工作的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="e71cf-159">A value that specifies the path and file name of the task to be run at the scheduled time.</span></span> <span data-ttu-id="e71cf-160">例如： C： \\ Windows \\ System32 \\calc.exe。</span><span class="sxs-lookup"><span data-stu-id="e71cf-160">For example: C:\\Windows\\System32\\calc.exe.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **starttime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-161"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-162">值，指定執行工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-162">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="e71cf-163">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-163">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-164">例如，14:30 會指定2：30PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-164">For example, 14:30 specifies 2:30PM.</span></span> <span data-ttu-id="e71cf-165">預設值是未指定/ST 的目前時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-165">The default is the current time is /ST is not specified.</span></span> <span data-ttu-id="e71cf-166">此選項是/SC 一次引數的必要項。</span><span class="sxs-lookup"><span data-stu-id="e71cf-166">This option is required wit the /SC ONCE argument.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **間隔**</span><span class="sxs-lookup"><span data-stu-id="e71cf-167"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-168">指定重複間隔（以分鐘為單位）的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-168">A value that specifies the repetition interval in minutes.</span></span> <span data-ttu-id="e71cf-169">這不適用於下列排程類型： MINUTE、每小時、ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-169">This is not applicable for the following schedule types: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e71cf-170">有效範圍是 1-599940 分鐘。</span><span class="sxs-lookup"><span data-stu-id="e71cf-170">The valid range is 1 - 599940 minutes.</span></span> <span data-ttu-id="e71cf-171">如果指定了/ET 或/DU 參數，預設值為10分鐘。</span><span class="sxs-lookup"><span data-stu-id="e71cf-171">If either the /ET or /DU parameters are specified, the default is 10 minutes.</span></span>

<span data-ttu-id="e71cf-172">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-172">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **endtime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-173"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-174">值，指定執行工作的結束時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-174">A value that specifies the end time to run the task.</span></span> <span data-ttu-id="e71cf-175">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-175">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-176">例如，14:50 會指定2：50PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-176">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e71cf-177">這不適用於下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-177">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

<span data-ttu-id="e71cf-178">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-178">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **持續時間**</span><span class="sxs-lookup"><span data-stu-id="e71cf-179"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-180">值，指定執行工作的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-180">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="e71cf-181">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-181">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-182">例如，14:50 會指定2：50PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-182">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e71cf-183">這不適用於/ET 和下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-183">This is not applicable with /ET and for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e71cf-184">針對 (工作排程器1.0 工作的/V1 工作) ，如果指定/RI，則持續時間預設值為一小時。</span><span class="sxs-lookup"><span data-stu-id="e71cf-184">For /V1 tasks (Task Scheduler 1.0 tasks), if /RI is specified, then the duration default is one hour.</span></span>

<span data-ttu-id="e71cf-185">**WINDOWS XP：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-185">**Windows XP:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="e71cf-186"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-187">值，這個值會在結束時間或持續時間結束工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-187">A value that terminates the task at the end time or duration time.</span></span> <span data-ttu-id="e71cf-188">這不適用於下列排程類型： ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-188">This is not applicable for the following schedule types: ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span> <span data-ttu-id="e71cf-189">必須指定/ET 或/DU。</span><span class="sxs-lookup"><span data-stu-id="e71cf-189">Either /ET or /DU must be specified.</span></span>

<span data-ttu-id="e71cf-190">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-190">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/Sd** 開始 **日期**</span><span class="sxs-lookup"><span data-stu-id="e71cf-191"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-192">值，指定要在其上執行工作的第一個日期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-192">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="e71cf-193">格式為 mm/dd/yyyy。</span><span class="sxs-lookup"><span data-stu-id="e71cf-193">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="e71cf-194">此值預設為目前的日期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-194">This value defaults to the current date.</span></span> <span data-ttu-id="e71cf-195">這不適用於下列排程類型：一次、ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-195">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **結束** 日期</span><span class="sxs-lookup"><span data-stu-id="e71cf-196"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-197">值，指定工作將執行的最後日期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-197">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="e71cf-198">格式為 mm/dd/yyyy。</span><span class="sxs-lookup"><span data-stu-id="e71cf-198">The format is mm/dd/yyyy.</span></span> <span data-ttu-id="e71cf-199">這不適用於下列排程類型：一次、ONSTART、整理、ONIDLE 和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-199">This is not applicable for the following schedule types: ONCE, ONSTART, ONLOGON, ONIDLE, and ONEVENT.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span><span class="sxs-lookup"><span data-stu-id="e71cf-200"><span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-201">值，指定 ONEVENT 觸發程式的事件通道。</span><span class="sxs-lookup"><span data-stu-id="e71cf-201">A value that specifies the event channel for ONEVENT triggers.</span></span>

<span data-ttu-id="e71cf-202">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-202">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="e71cf-203"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-204">值，只有在工作執行時，如果/RU 使用者目前登入，才讓工作以互動方式執行。</span><span class="sxs-lookup"><span data-stu-id="e71cf-204">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="e71cf-205">只有在使用者登入時才會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-205">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="e71cf-206">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-206">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span><span class="sxs-lookup"><span data-stu-id="e71cf-207"><span id="_NP_"></span><span id="_np_"></span>**/NP**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-208">指出未儲存任何密碼的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-208">A value that indicates that no password is stored.</span></span> <span data-ttu-id="e71cf-209">此工作不會以互動方式執行為指定的使用者。</span><span class="sxs-lookup"><span data-stu-id="e71cf-209">The task does not run interactively as the given user.</span></span> <span data-ttu-id="e71cf-210">只有本機資源可以使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-210">Only local resources are available.</span></span>

<span data-ttu-id="e71cf-211">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-211">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="e71cf-212"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-213">值，這個值會標記要在其最終執行之後刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-213">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="e71cf-214">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-214">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/Xml** **xmlfile**</span><span class="sxs-lookup"><span data-stu-id="e71cf-215"><span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-216">從 XML 檔案建立工作的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-216">A value that creates a task from an XML file.</span></span> <span data-ttu-id="e71cf-217">此參數可以與/RU 和/RP 參數結合，或在工作 XML 已包含主體時，單獨使用/RP 參數。</span><span class="sxs-lookup"><span data-stu-id="e71cf-217">This parameter can be combined with /RU and /RP switches, or with the /RP switch alone when the task XML already contains the principal.</span></span>

<span data-ttu-id="e71cf-218">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-218">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span><span class="sxs-lookup"><span data-stu-id="e71cf-219"><span id="_V1_"></span><span id="_v1_"></span>**/V1**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-220">此值會建立 Windows 2000、Windows Server 2003 和 Windows XP 平臺可以看見的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-220">A value that creates a task visible to Windows 2000, Windows Server 2003, and Windows XP platforms.</span></span>

<span data-ttu-id="e71cf-221">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-221">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="e71cf-222"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-223">強制建立工作的值，如果指定的工作已存在，則會隱藏警告。</span><span class="sxs-lookup"><span data-stu-id="e71cf-223">A value that forcefully creates the task and suppresses warnings if the specified task already exists.</span></span>

<span data-ttu-id="e71cf-224">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-224">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **層級**</span><span class="sxs-lookup"><span data-stu-id="e71cf-225"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-226">值，這個值會設定工作的執行層級。</span><span class="sxs-lookup"><span data-stu-id="e71cf-226">A value that sets the run level for the task.</span></span> <span data-ttu-id="e71cf-227">有效的值為受限和最高。</span><span class="sxs-lookup"><span data-stu-id="e71cf-227">Valid values are LIMITED and HIGHEST.</span></span> <span data-ttu-id="e71cf-228">預設值為 [有限]。</span><span class="sxs-lookup"><span data-stu-id="e71cf-228">The default is LIMITED.</span></span>

<span data-ttu-id="e71cf-229">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-229">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-230"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-231">值，指定在引發觸發程式之後，延遲工作的等候時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-231">A value that specifies the wait time to delay the task after the trigger is fired.</span></span> <span data-ttu-id="e71cf-232">時間格式為 mmmm： ss。</span><span class="sxs-lookup"><span data-stu-id="e71cf-232">The time format is mmmm:ss.</span></span> <span data-ttu-id="e71cf-233">此選項只適用于排程類型 ONSTART、整理和 ONEVENT。</span><span class="sxs-lookup"><span data-stu-id="e71cf-233">This option is only valid for schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="e71cf-234">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-234">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-235"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-235"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-236">值，顯示 Schtasks.exe 的說明訊息。</span><span class="sxs-lookup"><span data-stu-id="e71cf-236">A value that displays the help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e71cf-237">備註</span><span class="sxs-lookup"><span data-stu-id="e71cf-237">Remarks</span></span>

<span data-ttu-id="e71cf-238">在 Windows XP、Windows Server 2003 或 Windows 2000 作業系統上執行的遠端電腦上建立工作時，請使用/V1 參數。</span><span class="sxs-lookup"><span data-stu-id="e71cf-238">When creating a task on a remote computer running on the Windows XP, Windows Server 2003, or Windows 2000 operating system, use the /V1 switch.</span></span>

<span data-ttu-id="e71cf-239">如果遠端電腦已啟用 [檔案及印表機共用] 防火牆例外，且已停用 [遠端排程工作管理] 防火牆例外，您就無法建立非互動式遠端工作排程器1.0 工作 (使用/IT 參數建立工作，並使用/V1 參數) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-239">You cannot create a non-interactive remote Task Scheduler 1.0 task (create a task by not using the /IT switch and using the /V1 switch) if the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled.</span></span>

## <a name="deleting-a-task"></a><span data-ttu-id="e71cf-240">刪除工作</span><span class="sxs-lookup"><span data-stu-id="e71cf-240">Deleting a Task</span></span>

<span data-ttu-id="e71cf-241">下列語法用來刪除一或多個排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-241">The following syntax is used to delete one or more scheduled tasks.</span></span>

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a><span data-ttu-id="e71cf-242">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-242">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-243"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-244">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-244">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-245">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-245">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-246"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-247">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-247">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-248"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-249">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-249">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e71cf-250">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-250">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-251"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-252">值，指定要刪除之排程工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e71cf-252">A value that specifies the name of the scheduled task to delete.</span></span> <span data-ttu-id="e71cf-253">您 \* 可以使用萬用字元 () 來刪除所有工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-253">The wildcard character (\*) can be used to delete all tasks.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span><span class="sxs-lookup"><span data-stu-id="e71cf-254"><span id="_F_"></span><span id="_f_"></span>**/F**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-255">強制刪除工作的值，如果指定的工作正在執行，則隱藏警告。</span><span class="sxs-lookup"><span data-stu-id="e71cf-255">A value that forcefully deletes the task and suppresses warnings if the specified task is running.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-256"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-256"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-257">顯示 Schtasks.exe 說明的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-257">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="running-a-task"></a><span data-ttu-id="e71cf-258">正在執行工作</span><span class="sxs-lookup"><span data-stu-id="e71cf-258">Running a Task</span></span>

<span data-ttu-id="e71cf-259">下列語法可用來立即執行排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-259">The following syntax is used to immediately run a scheduled task.</span></span>

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="e71cf-260">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-260">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-261"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-262">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-262">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-263">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-263">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-264"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-265">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-265">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-266"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-267">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-267">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e71cf-268">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-268">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-269"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-270">值，指定要執行之排程工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e71cf-270">A value that specifies the name of the scheduled task to run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-271"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-271"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-272">顯示 Schtasks.exe 說明的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-272">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="ending-a-running-task"></a><span data-ttu-id="e71cf-273">結束正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="e71cf-273">Ending a Running Task</span></span>

<span data-ttu-id="e71cf-274">下列語法用來停止執行中的排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-274">The following syntax is used to stop a running scheduled task.</span></span>

> [!Note]  
> <span data-ttu-id="e71cf-275">若要停止執行遠端工作，請確定遠端電腦已啟用 [檔案及印表機共用] 和 [遠端排程工作] 管理防火牆例外。</span><span class="sxs-lookup"><span data-stu-id="e71cf-275">To stop a remote task from running, ensure that the remote computer has the File and Printer Sharing and Remote Scheduled Tasks Management firewall exceptions enabled.</span></span>

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a><span data-ttu-id="e71cf-276">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-276">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-277"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-278">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-278">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-279">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-279">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-280"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-281">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-281">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-282"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-283">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-283">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e71cf-284">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-284">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-285"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-286">值，指定要停止之排程工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="e71cf-286">A value that specifies the name of the scheduled task to stop.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-287"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-287"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-288">顯示 Schtasks.exe 說明的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-288">A value that displays Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="querying-for-task-information"></a><span data-ttu-id="e71cf-289">查詢工作資訊</span><span class="sxs-lookup"><span data-stu-id="e71cf-289">Querying for Task Information</span></span>

<span data-ttu-id="e71cf-290">下列語法用來顯示本機或遠端電腦上的排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-290">The following syntax is used to display the scheduled tasks from the local or remote computer.</span></span>

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a><span data-ttu-id="e71cf-291">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-291">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-292"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-293">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-293">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-294">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-294">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-295"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-296">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-296">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-297"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-298">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-298">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e71cf-299">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-299">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/Fo** **格式**</span><span class="sxs-lookup"><span data-stu-id="e71cf-300"><span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-301">指定輸出格式的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-301">A value that specifies the output format.</span></span> <span data-ttu-id="e71cf-302">有效的值為 TABLE、LIST 和 CSV。</span><span class="sxs-lookup"><span data-stu-id="e71cf-302">The valid values are TABLE, LIST, and CSV.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span><span class="sxs-lookup"><span data-stu-id="e71cf-303"><span id="_NH_"></span><span id="_nh_"></span>**/NH**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-304">值，指定不應該在輸出中顯示資料行標題。</span><span class="sxs-lookup"><span data-stu-id="e71cf-304">A value that specifies that the column header should not be displayed in the output.</span></span> <span data-ttu-id="e71cf-305">這僅適用于資料表和 CSV 格式。</span><span class="sxs-lookup"><span data-stu-id="e71cf-305">This is valid only for TABLE and CSV formats.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span><span class="sxs-lookup"><span data-stu-id="e71cf-306"><span id="_V_"></span><span id="_v_"></span>**/V**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-307">顯示詳細資訊工作輸出的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-307">A value that displays verbose task output.</span></span>

> [!Note]  
> <span data-ttu-id="e71cf-308">如果工作排定為僅執行一次，則顯示的排程資訊為「無法使用此格式的資料。」</span><span class="sxs-lookup"><span data-stu-id="e71cf-308">If a task was scheduled to run only one time, then the displayed schedule information is "Scheduling data is not available in this format."</span></span>

 

</dd> <dt>

<span data-ttu-id="e71cf-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-309"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-310">值，指定要取得其資訊的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="e71cf-310">A value that specifies the task name for which to retrieve the information.</span></span> <span data-ttu-id="e71cf-311">如果未指定工作名稱，則會顯示所有工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="e71cf-311">If no task name is specified, then information for all the tasks will be displayed.</span></span>

<span data-ttu-id="e71cf-312">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-312">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span><span class="sxs-lookup"><span data-stu-id="e71cf-313"><span id="_XML_"></span><span id="_xml_"></span>**/XML**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-314">值，用來顯示 XML 格式的工作定義。</span><span class="sxs-lookup"><span data-stu-id="e71cf-314">A value that is used to display the task definitions in XML format.</span></span>

<span data-ttu-id="e71cf-315">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-315">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-316"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-316"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-317">用來顯示 Schtasks.exe 說明的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-317">A value that is used to display the Help for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="changing-a-task"></a><span data-ttu-id="e71cf-318">變更工作</span><span class="sxs-lookup"><span data-stu-id="e71cf-318">Changing a Task</span></span>

<span data-ttu-id="e71cf-319">下列語法用來變更程式執行的方式，或變更排程工作所使用的使用者帳戶和密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-319">The following syntax is used to change how the program runs, or change the user account and password used by a scheduled task.</span></span>

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a><span data-ttu-id="e71cf-320">參數</span><span class="sxs-lookup"><span data-stu-id="e71cf-320">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cf-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **系統**</span><span class="sxs-lookup"><span data-stu-id="e71cf-321"><span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **system**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-322">值，指定要連接的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-322">A value that specifies the remote computer to connect to.</span></span> <span data-ttu-id="e71cf-323">如果省略，系統參數會預設為本機電腦。</span><span class="sxs-lookup"><span data-stu-id="e71cf-323">If omitted, the system parameter defaults to the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** 使用者 **名稱**</span><span class="sxs-lookup"><span data-stu-id="e71cf-324"><span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-325">值，指定 Schtasks.exe 應該在其上執行的使用者內容。</span><span class="sxs-lookup"><span data-stu-id="e71cf-325">A value that specifies the user context under which Schtasks.exe should run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ 密碼 \]**</span><span class="sxs-lookup"><span data-stu-id="e71cf-326"><span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[password\]**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-327">值，指定指定使用者內容的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-327">A value that specifies the password for the given user context.</span></span> <span data-ttu-id="e71cf-328">如果省略，Schtasks.exe 會提示使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="e71cf-328">If omitted, Schtasks.exe prompts the user for input.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/Tn** **taskname**</span><span class="sxs-lookup"><span data-stu-id="e71cf-329"><span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-330">值，指定要變更的排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-330">A value that specifies which scheduled task to change.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **runasuser**</span><span class="sxs-lookup"><span data-stu-id="e71cf-331"><span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-332">值，這個值會變更排定的工作將在其中執行的使用者名稱 (使用者內容) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-332">A value that changes the user name (user context) under which the scheduled task will run.</span></span> <span data-ttu-id="e71cf-333">系統帳戶的有效值為 ""、"NT 授權單位 \\ system" 或 "system"。</span><span class="sxs-lookup"><span data-stu-id="e71cf-333">For the system account, valid values are "", "NT AUTHORITY\\SYSTEM", or "SYSTEM".</span></span> <span data-ttu-id="e71cf-334">針對工作排程器2.0 工作，「NT 授權單位 \\ LOCALSERVICE」和「NT 授權單位 NETWORKSERVICE」 \\ 也是有效的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-334">For Task Scheduler 2.0 tasks, "NT AUTHORITY\\LOCALSERVICE" and "NT AUTHORITY\\NETWORKSERVICE" are also valid values.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/Rp** **runaspassword**</span><span class="sxs-lookup"><span data-stu-id="e71cf-335"><span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-336">值，指定現有使用者內容的新密碼或新使用者帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-336">A value that specifies a new password for the existing user context or the password for a new user account.</span></span> <span data-ttu-id="e71cf-337">系統帳戶會忽略此密碼。</span><span class="sxs-lookup"><span data-stu-id="e71cf-337">This password is ignored for the system account.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/Tr** **/tr**</span><span class="sxs-lookup"><span data-stu-id="e71cf-338"><span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-339">值，指定工作將執行的新程式。</span><span class="sxs-lookup"><span data-stu-id="e71cf-339">A value that specifies a new program that the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **starttime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-340"><span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-341">值，指定執行工作的開始時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-341">A value that specifies the start time to run the task.</span></span> <span data-ttu-id="e71cf-342">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-342">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-343">例如，14:30 會指定2：30PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-343">For example, 14:30 specifies 2:30PM.</span></span>

<span data-ttu-id="e71cf-344">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-344">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **間隔**</span><span class="sxs-lookup"><span data-stu-id="e71cf-345"><span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-346">值，指定重複間隔（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="e71cf-346">A value that specifies the repetition interval, in minutes.</span></span> <span data-ttu-id="e71cf-347">有效範圍是 1-599940 分鐘。</span><span class="sxs-lookup"><span data-stu-id="e71cf-347">The valid range is 1 - 599940 minutes.</span></span>

<span data-ttu-id="e71cf-348">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-348">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **endtime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-349"><span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-350">值，指定工作的結束時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-350">A value that specifies the end time for the task.</span></span> <span data-ttu-id="e71cf-351">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-351">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-352">例如，14:50 會指定2：50PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-352">For example, 14:50 specifies 2:50PM.</span></span>

<span data-ttu-id="e71cf-353">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-353">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **持續時間**</span><span class="sxs-lookup"><span data-stu-id="e71cf-354"><span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-355">值，指定執行工作的持續時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-355">A value that specifies the duration to run the task.</span></span> <span data-ttu-id="e71cf-356">時間格式為 HH： mm (24 小時的時間) 。</span><span class="sxs-lookup"><span data-stu-id="e71cf-356">The time format is HH:mm (24-hour time).</span></span> <span data-ttu-id="e71cf-357">例如，14:50 會指定2：50PM。</span><span class="sxs-lookup"><span data-stu-id="e71cf-357">For example, 14:50 specifies 2:50PM.</span></span> <span data-ttu-id="e71cf-358">這不適用於/ET 參數。</span><span class="sxs-lookup"><span data-stu-id="e71cf-358">This is not applicable with the /ET parameter.</span></span>

<span data-ttu-id="e71cf-359">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-359">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span><span class="sxs-lookup"><span data-stu-id="e71cf-360"><span id="_K_"></span><span id="_k_"></span>**/K**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-361">值，這個值會在結束時間或持續時間結束工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-361">A value that terminates the task at the end time or duration time.</span></span>

<span data-ttu-id="e71cf-362">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-362">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/Sd** 開始 **日期**</span><span class="sxs-lookup"><span data-stu-id="e71cf-363"><span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-364">值，指定要在其上執行工作的第一個日期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-364">A value that specifies the first date on which to run the task.</span></span> <span data-ttu-id="e71cf-365">格式為 mm/dd/yyyy。</span><span class="sxs-lookup"><span data-stu-id="e71cf-365">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="e71cf-366">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-366">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **結束** 日期</span><span class="sxs-lookup"><span data-stu-id="e71cf-367"><span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-368">值，指定工作將執行的最後日期。</span><span class="sxs-lookup"><span data-stu-id="e71cf-368">A value that specifies the last date that the task will run.</span></span> <span data-ttu-id="e71cf-369">格式為 mm/dd/yyyy。</span><span class="sxs-lookup"><span data-stu-id="e71cf-369">The format is mm/dd/yyyy.</span></span>

<span data-ttu-id="e71cf-370">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-370">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span><span class="sxs-lookup"><span data-stu-id="e71cf-371"><span id="_IT_"></span><span id="_it_"></span>**/IT**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-372">值，只有在工作執行時，如果/RU 使用者目前登入，才讓工作以互動方式執行。</span><span class="sxs-lookup"><span data-stu-id="e71cf-372">A value that enables the task to run interactively only if the /RU user is currently logged on at the time the task runs.</span></span> <span data-ttu-id="e71cf-373">只有在使用者登入時才會執行此工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-373">The task runs only if the user is logged on.</span></span>

<span data-ttu-id="e71cf-374">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-374">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **層級**</span><span class="sxs-lookup"><span data-stu-id="e71cf-375"><span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-376">值，這個值會設定工作的執行層級。</span><span class="sxs-lookup"><span data-stu-id="e71cf-376">A value that sets the run level for the task.</span></span> <span data-ttu-id="e71cf-377">有效的值為受限和最高。</span><span class="sxs-lookup"><span data-stu-id="e71cf-377">Valid values are LIMITED and HIGHEST.</span></span>

<span data-ttu-id="e71cf-378">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-378">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span><span class="sxs-lookup"><span data-stu-id="e71cf-379"><span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-380">啟用排程工作的值。</span><span class="sxs-lookup"><span data-stu-id="e71cf-380">A value that enables the scheduled task.</span></span> <span data-ttu-id="e71cf-381">啟用的工作可以執行，而且無法執行已停用的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-381">An enabled task can run, and a disabled task cannot run.</span></span>

<span data-ttu-id="e71cf-382">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-382">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span><span class="sxs-lookup"><span data-stu-id="e71cf-383"><span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-384">值，這個值會停用執行中的排程工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-384">A value that disables the scheduled task from running.</span></span>

> [!Note]  
> <span data-ttu-id="e71cf-385">如果 Schtasks.exe 停用遠端工作排程器1.0 工作，且遠端電腦已啟用 [檔案及印表機共用] 防火牆例外，而 [遠端排程工作管理防火牆] 例外已停用，則從工作排程器 2.0 API 讀取時，不會停用此工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-385">If a remote Task Scheduler 1.0 task is disabled by Schtasks.exe and the remote computer has the File and Printer Sharing firewall exception enabled and the Remote Scheduled Tasks Management firewall exception disabled, then the task will not be disabled when read from a Task Scheduler 2.0 API.</span></span>

 

<span data-ttu-id="e71cf-386">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-386">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span><span class="sxs-lookup"><span data-stu-id="e71cf-387"><span id="_Z_"></span><span id="_z_"></span>**/Z**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-388">值，這個值會標記要在其最終執行之後刪除的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-388">A value that marks the task to be deleted after its final run.</span></span>

<span data-ttu-id="e71cf-389">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-389">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span><span class="sxs-lookup"><span data-stu-id="e71cf-390"><span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**</span></span>
</dt> <dd>

<span data-ttu-id="e71cf-391">值，指定引發觸發程式之後，順延強制工作的等候時間。</span><span class="sxs-lookup"><span data-stu-id="e71cf-391">A value that specifies the wait time to delay the running of the task after the trigger is fired.</span></span> <span data-ttu-id="e71cf-392">時間格式為 mmmm： ss。</span><span class="sxs-lookup"><span data-stu-id="e71cf-392">The time format is mmmm:ss.</span></span> <span data-ttu-id="e71cf-393">此選項僅適用于排程類型為 ONSTART、整理和 ONEVENT 的工作。</span><span class="sxs-lookup"><span data-stu-id="e71cf-393">This option is only valid for tasks with the schedule types ONSTART, ONLOGON, and ONEVENT.</span></span>

<span data-ttu-id="e71cf-394">**WINDOWS XP 和 Windows Server 2003：** 此選項無法使用。</span><span class="sxs-lookup"><span data-stu-id="e71cf-394">**Windows XP and Windows Server 2003:** This option is not available.</span></span>

</dd> <dt>

<span data-ttu-id="e71cf-395"><span id="___"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="e71cf-395"><span id="___"></span>**/?**</span></span> 
</dt> <dd>

<span data-ttu-id="e71cf-396">值，顯示 Schtasks.exe 的說明訊息。</span><span class="sxs-lookup"><span data-stu-id="e71cf-396">A value that displays the Help message for Schtasks.exe.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e71cf-397">規格需求</span><span class="sxs-lookup"><span data-stu-id="e71cf-397">Requirements</span></span>



| <span data-ttu-id="e71cf-398">需求</span><span class="sxs-lookup"><span data-stu-id="e71cf-398">Requirement</span></span> | <span data-ttu-id="e71cf-399">值</span><span class="sxs-lookup"><span data-stu-id="e71cf-399">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e71cf-400">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e71cf-400">Minimum supported client</span></span><br/> | <span data-ttu-id="e71cf-401">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71cf-401">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e71cf-402">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e71cf-402">Minimum supported server</span></span><br/> | <span data-ttu-id="e71cf-403">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e71cf-403">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 





