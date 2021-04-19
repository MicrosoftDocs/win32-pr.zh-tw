---
description: MsiServiceConfig 資料表會設定由目前封裝安裝或安裝的服務。
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: MsiServiceConfig 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997878"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="91003-103">MsiServiceConfig 資料表</span><span class="sxs-lookup"><span data-stu-id="91003-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="91003-104">MsiServiceConfig 資料表會設定由目前封裝安裝或安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="91003-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="91003-105">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="91003-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="91003-106">從 Windows Installer 5.0 開始，可以使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="91003-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="91003-107">MsiServiceConfig 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="91003-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="91003-108">Column</span><span class="sxs-lookup"><span data-stu-id="91003-108">Column</span></span>           | <span data-ttu-id="91003-109">類型</span><span class="sxs-lookup"><span data-stu-id="91003-109">Type</span></span>                         | <span data-ttu-id="91003-110">答案</span><span class="sxs-lookup"><span data-stu-id="91003-110">Key</span></span> | <span data-ttu-id="91003-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="91003-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="91003-112">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="91003-112">MsiServiceConfig</span></span> | [<span data-ttu-id="91003-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="91003-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="91003-114">Y</span><span class="sxs-lookup"><span data-stu-id="91003-114">Y</span></span>   | <span data-ttu-id="91003-115">N</span><span class="sxs-lookup"><span data-stu-id="91003-115">N</span></span>        |
| <span data-ttu-id="91003-116">Name</span><span class="sxs-lookup"><span data-stu-id="91003-116">Name</span></span>             | [<span data-ttu-id="91003-117">格式 化</span><span class="sxs-lookup"><span data-stu-id="91003-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="91003-118">N</span><span class="sxs-lookup"><span data-stu-id="91003-118">N</span></span>   | <span data-ttu-id="91003-119">N</span><span class="sxs-lookup"><span data-stu-id="91003-119">N</span></span>        |
| <span data-ttu-id="91003-120">事件</span><span class="sxs-lookup"><span data-stu-id="91003-120">Event</span></span>            | [<span data-ttu-id="91003-121">整數</span><span class="sxs-lookup"><span data-stu-id="91003-121">Integer</span></span>](integer.md)       | <span data-ttu-id="91003-122">N</span><span class="sxs-lookup"><span data-stu-id="91003-122">N</span></span>   | <span data-ttu-id="91003-123">N</span><span class="sxs-lookup"><span data-stu-id="91003-123">N</span></span>        |
| <span data-ttu-id="91003-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="91003-124">ConfigType</span></span>       | [<span data-ttu-id="91003-125">整數</span><span class="sxs-lookup"><span data-stu-id="91003-125">Integer</span></span>](integer.md)       | <span data-ttu-id="91003-126">N</span><span class="sxs-lookup"><span data-stu-id="91003-126">N</span></span>   | <span data-ttu-id="91003-127">N</span><span class="sxs-lookup"><span data-stu-id="91003-127">N</span></span>        |
| <span data-ttu-id="91003-128">引數</span><span class="sxs-lookup"><span data-stu-id="91003-128">Argument</span></span>         | [<span data-ttu-id="91003-129">格式 化</span><span class="sxs-lookup"><span data-stu-id="91003-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="91003-130">N</span><span class="sxs-lookup"><span data-stu-id="91003-130">N</span></span>   | <span data-ttu-id="91003-131">Y</span><span class="sxs-lookup"><span data-stu-id="91003-131">Y</span></span>        |
| <span data-ttu-id="91003-132">元件\_</span><span class="sxs-lookup"><span data-stu-id="91003-132">Component\_</span></span>      | [<span data-ttu-id="91003-133">識別碼</span><span class="sxs-lookup"><span data-stu-id="91003-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="91003-134">N</span><span class="sxs-lookup"><span data-stu-id="91003-134">N</span></span>   | <span data-ttu-id="91003-135">N</span><span class="sxs-lookup"><span data-stu-id="91003-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="91003-136">資料行</span><span class="sxs-lookup"><span data-stu-id="91003-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="91003-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="91003-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="91003-138">這是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="91003-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="91003-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="91003-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="91003-140">此資料行包含屬於此封裝或已安裝之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="91003-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="91003-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件</span><span class="sxs-lookup"><span data-stu-id="91003-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="91003-142">這個資料行會指定變更服務設定的時機。</span><span class="sxs-lookup"><span data-stu-id="91003-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="91003-143">下列值可以合併以表示多個作業。</span><span class="sxs-lookup"><span data-stu-id="91003-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="91003-144">包含的任何值都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="91003-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="91003-145">常數</span><span class="sxs-lookup"><span data-stu-id="91003-145">Constant</span></span>                                         | <span data-ttu-id="91003-146">描述</span><span class="sxs-lookup"><span data-stu-id="91003-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="91003-147">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="91003-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="91003-148">在元件安裝期間採取動作。</span><span class="sxs-lookup"><span data-stu-id="91003-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="91003-149">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="91003-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="91003-150">在元件卸載期間採取動作。</span><span class="sxs-lookup"><span data-stu-id="91003-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="91003-151">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="91003-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="91003-152">在元件重新安裝期間採取動作。</span><span class="sxs-lookup"><span data-stu-id="91003-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="91003-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>名稱 configtype</span><span class="sxs-lookup"><span data-stu-id="91003-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="91003-154">此欄位中的值與 [引數] 欄位中的值結合，可指定要對服務設定進行的變更。</span><span class="sxs-lookup"><span data-stu-id="91003-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="91003-155">指定的變更會在系統下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="91003-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="91003-156">Config</span><span class="sxs-lookup"><span data-stu-id="91003-156">Config</span></span>                                                      | <span data-ttu-id="91003-157">Description</span><span class="sxs-lookup"><span data-stu-id="91003-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91003-158">**服務 \_設定 \_ 延遲 \_ 自動 \_ 啟動** 3</span><span class="sxs-lookup"><span data-stu-id="91003-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="91003-159">設定 [自動啟動服務](../services/automatically-starting-services.md)的時間延遲。</span><span class="sxs-lookup"><span data-stu-id="91003-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="91003-160">在 [引數] 欄位中輸入1，以在其他自動啟動服務加上時間延遲之後啟動服務。</span><span class="sxs-lookup"><span data-stu-id="91003-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="91003-161">在 [引數] 欄位中輸入0，以關閉自動啟動服務延遲。</span><span class="sxs-lookup"><span data-stu-id="91003-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="91003-162">僅適用于已安裝的自動啟動服務，或此封裝所安裝的服務，以及 [ServiceInstall 資料表](serviceinstall-table.md)的 StartType 欄位中的 **服務 \_ 自動 \_ 啟動**。</span><span class="sxs-lookup"><span data-stu-id="91003-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="91003-163">**服務 \_CONFIG \_ REQUIRED \_ 許可權 \_ 資訊** 6</span><span class="sxs-lookup"><span data-stu-id="91003-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="91003-164">變更服務所需的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="91003-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="91003-165">在 [引數] 欄位中輸入要求的許可權清單。</span><span class="sxs-lookup"><span data-stu-id="91003-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="91003-166">[引數] 欄位中的 [格式化](formatted.md) 字串值會列出所要求之許可權的 [**許可權常數**](../secauthz/privilege-constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="91003-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="91003-167">您可以使用 \[ ~ \] [格式化](formatted.md)字串的語法來插入 null 字元。</span><span class="sxs-lookup"><span data-stu-id="91003-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="91003-168">分隔清單中的許可權常數 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="91003-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="91003-169">**服務 \_CONFIG \_ 服務 \_ SID \_ 資訊** 5</span><span class="sxs-lookup"><span data-stu-id="91003-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="91003-170">將服務 SID 類型新增至包含此服務的進程權杖。</span><span class="sxs-lookup"><span data-stu-id="91003-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="91003-171">在 [引數] 欄位中，為 [**服務 \_ sid \_ 資訊**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) 結構輸入有效的服務 sid 類型： **服務 sid 類型 [ \_ \_ \_ 無** ] (0x00) 、 **服務 \_ sid \_ 類型 \_ 限制** (0x03) 或 **服務 \_ sid \_ 類型 \_** [不受限制] (0x01) 。</span><span class="sxs-lookup"><span data-stu-id="91003-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="91003-172">**服務 \_CONFIG \_ PRESHUTDOWN \_ INFO** 7</span><span class="sxs-lookup"><span data-stu-id="91003-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="91003-173">設定 [服務控制管理員](../services/service-control-manager.md) (SCM) 等待的時間長度，再繼續進行其他關機作業。</span><span class="sxs-lookup"><span data-stu-id="91003-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="91003-174">SCM 會在將 **服務 \_ 控制 \_ PRESHUTDOWN** 通知傳送至服務之後等候這段時間。</span><span class="sxs-lookup"><span data-stu-id="91003-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="91003-175">在 [引數] 欄位中輸入時間延遲長度（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="91003-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="91003-176">將 [引數] 欄位保留為空白，以將時間延遲重設為預設值3分鐘。</span><span class="sxs-lookup"><span data-stu-id="91003-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="91003-177">**服務 \_設定 \_ 失敗 \_ 動作 \_ 旗** 標4</span><span class="sxs-lookup"><span data-stu-id="91003-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="91003-178">設定何時執行此服務的失敗動作。</span><span class="sxs-lookup"><span data-stu-id="91003-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="91003-179">如果服務沒有設定的失敗動作，就會忽略此設定。</span><span class="sxs-lookup"><span data-stu-id="91003-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="91003-180">輸入0，只在服務終止但未 **\_ 停止 reporting service** 時執行動作。</span><span class="sxs-lookup"><span data-stu-id="91003-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="91003-181">輸入1以在服務終止報表 **服務 \_** 且 [**服務 \_ 狀態**](/windows/win32/api/winsvc/ns-winsvc-service_status)結構的 **dwWin32ExitCode** 成員不 **\_ 成功時** 執行動作。</span><span class="sxs-lookup"><span data-stu-id="91003-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="91003-182">如果服務在沒有報表服務的情況下終止，也 **會 \_** 執行設定的失敗動作。</span><span class="sxs-lookup"><span data-stu-id="91003-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="91003-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數</span><span class="sxs-lookup"><span data-stu-id="91003-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="91003-184">此欄位中的值與 [名稱 configtype] 欄位中的值結合，可指定要對服務設定進行的變更。</span><span class="sxs-lookup"><span data-stu-id="91003-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="91003-185">指定的變更會在系統下次啟動時生效。</span><span class="sxs-lookup"><span data-stu-id="91003-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="91003-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="91003-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="91003-187">[元件資料表](component-table.md)的元件資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="91003-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="91003-188">驗證</span><span class="sxs-lookup"><span data-stu-id="91003-188">Validation</span></span>

<dl>

[<span data-ttu-id="91003-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="91003-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="91003-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="91003-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="91003-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="91003-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="91003-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="91003-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="91003-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="91003-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="91003-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="91003-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="91003-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="91003-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
