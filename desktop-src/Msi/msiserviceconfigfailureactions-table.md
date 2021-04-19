---
description: MsiServiceConfigFailureActions 資料表會列出服務失敗之後要執行的作業。 下表中指定的作業會在系統下次啟動時執行。
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: MsiServiceConfigFailureActions 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985290"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="23a79-104">MsiServiceConfigFailureActions 資料表</span><span class="sxs-lookup"><span data-stu-id="23a79-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="23a79-105">MsiServiceConfigFailureActions 資料表會列出服務失敗之後要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="23a79-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="23a79-106">下表中指定的作業會在系統下次啟動時執行。</span><span class="sxs-lookup"><span data-stu-id="23a79-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="23a79-107">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="23a79-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="23a79-108">從 Windows Installer 5.0 開始，可以使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="23a79-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="23a79-109">MsiServiceConfigFailureActions 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="23a79-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="23a79-110">Column</span><span class="sxs-lookup"><span data-stu-id="23a79-110">Column</span></span>                         | <span data-ttu-id="23a79-111">類型</span><span class="sxs-lookup"><span data-stu-id="23a79-111">Type</span></span>                         | <span data-ttu-id="23a79-112">答案</span><span class="sxs-lookup"><span data-stu-id="23a79-112">Key</span></span> | <span data-ttu-id="23a79-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="23a79-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="23a79-114">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="23a79-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="23a79-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="23a79-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="23a79-116">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-116">Y</span></span>   | <span data-ttu-id="23a79-117">N</span><span class="sxs-lookup"><span data-stu-id="23a79-117">N</span></span>        |
| <span data-ttu-id="23a79-118">Name</span><span class="sxs-lookup"><span data-stu-id="23a79-118">Name</span></span>                           | [<span data-ttu-id="23a79-119">格式 化</span><span class="sxs-lookup"><span data-stu-id="23a79-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23a79-120">N</span><span class="sxs-lookup"><span data-stu-id="23a79-120">N</span></span>   | <span data-ttu-id="23a79-121">N</span><span class="sxs-lookup"><span data-stu-id="23a79-121">N</span></span>        |
| <span data-ttu-id="23a79-122">事件</span><span class="sxs-lookup"><span data-stu-id="23a79-122">Event</span></span>                          | [<span data-ttu-id="23a79-123">整數</span><span class="sxs-lookup"><span data-stu-id="23a79-123">Integer</span></span>](integer.md)       | <span data-ttu-id="23a79-124">N</span><span class="sxs-lookup"><span data-stu-id="23a79-124">N</span></span>   | <span data-ttu-id="23a79-125">N</span><span class="sxs-lookup"><span data-stu-id="23a79-125">N</span></span>        |
| <span data-ttu-id="23a79-126">ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="23a79-126">ResetPeriod</span></span>                    | [<span data-ttu-id="23a79-127">整數</span><span class="sxs-lookup"><span data-stu-id="23a79-127">Integer</span></span>](integer.md)       | <span data-ttu-id="23a79-128">N</span><span class="sxs-lookup"><span data-stu-id="23a79-128">N</span></span>   | <span data-ttu-id="23a79-129">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-129">Y</span></span>        |
| <span data-ttu-id="23a79-130">RebootMessage</span><span class="sxs-lookup"><span data-stu-id="23a79-130">RebootMessage</span></span>                  | [<span data-ttu-id="23a79-131">格式 化</span><span class="sxs-lookup"><span data-stu-id="23a79-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23a79-132">N</span><span class="sxs-lookup"><span data-stu-id="23a79-132">N</span></span>   | <span data-ttu-id="23a79-133">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-133">Y</span></span>        |
| <span data-ttu-id="23a79-134">Command</span><span class="sxs-lookup"><span data-stu-id="23a79-134">Command</span></span>                        | [<span data-ttu-id="23a79-135">格式 化</span><span class="sxs-lookup"><span data-stu-id="23a79-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="23a79-136">N</span><span class="sxs-lookup"><span data-stu-id="23a79-136">N</span></span>   | <span data-ttu-id="23a79-137">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-137">Y</span></span>        |
| <span data-ttu-id="23a79-138">動作</span><span class="sxs-lookup"><span data-stu-id="23a79-138">Actions</span></span>                        | [<span data-ttu-id="23a79-139">Text</span><span class="sxs-lookup"><span data-stu-id="23a79-139">Text</span></span>](text.md)             | <span data-ttu-id="23a79-140">N</span><span class="sxs-lookup"><span data-stu-id="23a79-140">N</span></span>   | <span data-ttu-id="23a79-141">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-141">Y</span></span>        |
| <span data-ttu-id="23a79-142">DelayActions</span><span class="sxs-lookup"><span data-stu-id="23a79-142">DelayActions</span></span>                   | [<span data-ttu-id="23a79-143">Text</span><span class="sxs-lookup"><span data-stu-id="23a79-143">Text</span></span>](text.md)             | <span data-ttu-id="23a79-144">N</span><span class="sxs-lookup"><span data-stu-id="23a79-144">N</span></span>   | <span data-ttu-id="23a79-145">Y</span><span class="sxs-lookup"><span data-stu-id="23a79-145">Y</span></span>        |
| <span data-ttu-id="23a79-146">元件\_</span><span class="sxs-lookup"><span data-stu-id="23a79-146">Component\_</span></span>                    | [<span data-ttu-id="23a79-147">識別碼</span><span class="sxs-lookup"><span data-stu-id="23a79-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="23a79-148">N</span><span class="sxs-lookup"><span data-stu-id="23a79-148">N</span></span>   | <span data-ttu-id="23a79-149">N</span><span class="sxs-lookup"><span data-stu-id="23a79-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="23a79-150">資料行</span><span class="sxs-lookup"><span data-stu-id="23a79-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="23a79-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="23a79-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="23a79-152">這是識別失敗動作之資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="23a79-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="23a79-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="23a79-154">此資料行包含屬於此封裝或已安裝之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="23a79-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件</span><span class="sxs-lookup"><span data-stu-id="23a79-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="23a79-156">這個資料行會指定何時變更服務的設定。</span><span class="sxs-lookup"><span data-stu-id="23a79-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="23a79-157">下列值是可以結合以代表多個作業的位欄位。</span><span class="sxs-lookup"><span data-stu-id="23a79-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="23a79-158">任何其他位域值都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="23a79-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="23a79-159">常數</span><span class="sxs-lookup"><span data-stu-id="23a79-159">Constant</span></span>                                         | <span data-ttu-id="23a79-160">描述</span><span class="sxs-lookup"><span data-stu-id="23a79-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="23a79-161">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="23a79-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="23a79-162">在元件安裝期間變更。</span><span class="sxs-lookup"><span data-stu-id="23a79-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="23a79-163">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="23a79-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="23a79-164">在元件卸載期間變更。</span><span class="sxs-lookup"><span data-stu-id="23a79-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="23a79-165">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="23a79-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="23a79-166">重新安裝元件期間的變更。</span><span class="sxs-lookup"><span data-stu-id="23a79-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="23a79-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="23a79-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="23a79-168">服務失敗計數的重設期間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="23a79-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="23a79-169">[服務控制管理員](../services/service-control-manager.md) (SCM) 計算自上次重新開機系統之後每個服務失敗的次數。</span><span class="sxs-lookup"><span data-stu-id="23a79-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="23a79-170">如果重設期間的服務不會失敗，則會將計數重設為零。</span><span class="sxs-lookup"><span data-stu-id="23a79-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="23a79-171">當服務在第 n 次失敗時，系統會在 [ \[ \] 動作] 欄位中指定之陣列的元素 N-1 執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="23a79-172">將 [ResetPeriod] 欄位保留為空白，表示永遠不會重設失敗計數。</span><span class="sxs-lookup"><span data-stu-id="23a79-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span><span class="sxs-lookup"><span data-stu-id="23a79-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="23a79-174">在重新開機電腦之前傳送給使用者的訊息，以回應 [動作] 資料行中指定的 **SC \_ 動作 \_ 重新開機** 動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="23a79-175">您可以使用空字串 ""，以不變更的情況傳送目前的訊息。</span><span class="sxs-lookup"><span data-stu-id="23a79-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="23a79-176">您可以使用 \[ ~ \] [格式化](formatted.md)資料類型的語法來刪除目前的訊息，而不傳送任何訊息。</span><span class="sxs-lookup"><span data-stu-id="23a79-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>命令</span><span class="sxs-lookup"><span data-stu-id="23a79-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="23a79-178">由 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數所建立的進程所執行的命令列，以回應 [動作] 資料行中指定的 **SC \_ action \_ run \_ 命令** 動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="23a79-179">新的進程會在與服務相同的帳戶下執行，而且只有在 [動作] 欄位是 **SC \_ Action \_ RUN \_ 命令** 的情況下才會執行。</span><span class="sxs-lookup"><span data-stu-id="23a79-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="23a79-180">您可以使用空字串 ""，以不變更的情況使用目前的命令列。</span><span class="sxs-lookup"><span data-stu-id="23a79-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="23a79-181">您可以使用 \[ ~ \] [格式化](formatted.md)資料類型的語法來刪除目前的命令列，並在服務失敗時不執行任何操作。</span><span class="sxs-lookup"><span data-stu-id="23a79-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>行動</span><span class="sxs-lookup"><span data-stu-id="23a79-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="23a79-183">此欄位包含整數值的陣列，這些值會指定當服務失敗時，SCM 所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="23a79-184">分隔陣列中的值 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="23a79-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="23a79-185">陣列的第 n 個專案中的整數值會指定服務在第 n 次失敗時所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="23a79-186">陣列的每個成員都是下列其中一個整數值。</span><span class="sxs-lookup"><span data-stu-id="23a79-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="23a79-187">常數</span><span class="sxs-lookup"><span data-stu-id="23a79-187">Constant</span></span>                                 | <span data-ttu-id="23a79-188">描述</span><span class="sxs-lookup"><span data-stu-id="23a79-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="23a79-189">**SC \_動作 \_ 無** 0</span><span class="sxs-lookup"><span data-stu-id="23a79-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="23a79-190">不進行動作。</span><span class="sxs-lookup"><span data-stu-id="23a79-190">No action.</span></span>            |
| <span data-ttu-id="23a79-191">**SC \_動作 \_ 重新開機** 2</span><span class="sxs-lookup"><span data-stu-id="23a79-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="23a79-192">重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="23a79-192">Restart the computer.</span></span> |
| <span data-ttu-id="23a79-193">**SC \_動作 \_ 重新開機** 1</span><span class="sxs-lookup"><span data-stu-id="23a79-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="23a79-194">重新啟動服務。</span><span class="sxs-lookup"><span data-stu-id="23a79-194">Restart the service.</span></span>  |
| <span data-ttu-id="23a79-195">**SC \_動作 \_ 執行 \_ 命令** 3</span><span class="sxs-lookup"><span data-stu-id="23a79-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="23a79-196">執行命令。</span><span class="sxs-lookup"><span data-stu-id="23a79-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="23a79-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span><span class="sxs-lookup"><span data-stu-id="23a79-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="23a79-198">此欄位包含整數值的陣列，這些值會指定在執行動作資料行中指定的動作之前，要等候的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="23a79-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="23a79-199">分隔陣列中的值 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="23a79-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="23a79-200">DelayActions 陣列中的元素數目必須等於動作陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="23a79-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="23a79-201">DelayActions 陣列的第 n 個元素會指定動作陣列第 n 個元素的時間延遲。</span><span class="sxs-lookup"><span data-stu-id="23a79-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="23a79-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="23a79-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="23a79-203">[元件資料表](component-table.md)中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="23a79-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="23a79-204">驗證</span><span class="sxs-lookup"><span data-stu-id="23a79-204">Validation</span></span>

<dl>

[<span data-ttu-id="23a79-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="23a79-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="23a79-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="23a79-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="23a79-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="23a79-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="23a79-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="23a79-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="23a79-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="23a79-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="23a79-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="23a79-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="23a79-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="23a79-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
