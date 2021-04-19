---
description: ServiceInstall 資料表是用來安裝服務，並具有下列資料行。
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: ServiceInstall 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992480"
---
# <a name="serviceinstall-table"></a><span data-ttu-id="721d0-103">ServiceInstall 資料表</span><span class="sxs-lookup"><span data-stu-id="721d0-103">ServiceInstall Table</span></span>

<span data-ttu-id="721d0-104">ServiceInstall 資料表是用來安裝服務，並具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="721d0-104">The ServiceInstall table is used to install a service and has the following columns.</span></span>



| <span data-ttu-id="721d0-105">Column</span><span class="sxs-lookup"><span data-stu-id="721d0-105">Column</span></span>         | <span data-ttu-id="721d0-106">類型</span><span class="sxs-lookup"><span data-stu-id="721d0-106">Type</span></span>                               | <span data-ttu-id="721d0-107">答案</span><span class="sxs-lookup"><span data-stu-id="721d0-107">Key</span></span> | <span data-ttu-id="721d0-108">Nullable</span><span class="sxs-lookup"><span data-stu-id="721d0-108">Nullable</span></span> |
|----------------|------------------------------------|-----|----------|
| <span data-ttu-id="721d0-109">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="721d0-109">ServiceInstall</span></span> | [<span data-ttu-id="721d0-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="721d0-110">Identifier</span></span>](identifier.md)       | <span data-ttu-id="721d0-111">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-111">Y</span></span>   | <span data-ttu-id="721d0-112">N</span><span class="sxs-lookup"><span data-stu-id="721d0-112">N</span></span>        |
| <span data-ttu-id="721d0-113">Name</span><span class="sxs-lookup"><span data-stu-id="721d0-113">Name</span></span>           | [<span data-ttu-id="721d0-114">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-114">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-115">N</span><span class="sxs-lookup"><span data-stu-id="721d0-115">N</span></span>   | <span data-ttu-id="721d0-116">N</span><span class="sxs-lookup"><span data-stu-id="721d0-116">N</span></span>        |
| <span data-ttu-id="721d0-117">DisplayName</span><span class="sxs-lookup"><span data-stu-id="721d0-117">DisplayName</span></span>    | [<span data-ttu-id="721d0-118">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-118">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-119">N</span><span class="sxs-lookup"><span data-stu-id="721d0-119">N</span></span>   | <span data-ttu-id="721d0-120">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-120">Y</span></span>        |
| <span data-ttu-id="721d0-121">ServiceType</span><span class="sxs-lookup"><span data-stu-id="721d0-121">ServiceType</span></span>    | [<span data-ttu-id="721d0-122">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="721d0-122">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="721d0-123">N</span><span class="sxs-lookup"><span data-stu-id="721d0-123">N</span></span>   | <span data-ttu-id="721d0-124">N</span><span class="sxs-lookup"><span data-stu-id="721d0-124">N</span></span>        |
| <span data-ttu-id="721d0-125">StartType</span><span class="sxs-lookup"><span data-stu-id="721d0-125">StartType</span></span>      | [<span data-ttu-id="721d0-126">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="721d0-126">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="721d0-127">N</span><span class="sxs-lookup"><span data-stu-id="721d0-127">N</span></span>   | <span data-ttu-id="721d0-128">N</span><span class="sxs-lookup"><span data-stu-id="721d0-128">N</span></span>        |
| <span data-ttu-id="721d0-129">ErrorControl</span><span class="sxs-lookup"><span data-stu-id="721d0-129">ErrorControl</span></span>   | [<span data-ttu-id="721d0-130">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="721d0-130">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="721d0-131">N</span><span class="sxs-lookup"><span data-stu-id="721d0-131">N</span></span>   | <span data-ttu-id="721d0-132">N</span><span class="sxs-lookup"><span data-stu-id="721d0-132">N</span></span>        |
| <span data-ttu-id="721d0-133">LoadOrderGroup</span><span class="sxs-lookup"><span data-stu-id="721d0-133">LoadOrderGroup</span></span> | [<span data-ttu-id="721d0-134">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-134">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-135">N</span><span class="sxs-lookup"><span data-stu-id="721d0-135">N</span></span>   | <span data-ttu-id="721d0-136">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-136">Y</span></span>        |
| <span data-ttu-id="721d0-137">相依性</span><span class="sxs-lookup"><span data-stu-id="721d0-137">Dependencies</span></span>   | [<span data-ttu-id="721d0-138">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-138">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-139">N</span><span class="sxs-lookup"><span data-stu-id="721d0-139">N</span></span>   | <span data-ttu-id="721d0-140">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-140">Y</span></span>        |
| <span data-ttu-id="721d0-141">StartName</span><span class="sxs-lookup"><span data-stu-id="721d0-141">StartName</span></span>      | [<span data-ttu-id="721d0-142">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-142">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-143">N</span><span class="sxs-lookup"><span data-stu-id="721d0-143">N</span></span>   | <span data-ttu-id="721d0-144">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-144">Y</span></span>        |
| <span data-ttu-id="721d0-145">密碼</span><span class="sxs-lookup"><span data-stu-id="721d0-145">Password</span></span>       | [<span data-ttu-id="721d0-146">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-146">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-147">N</span><span class="sxs-lookup"><span data-stu-id="721d0-147">N</span></span>   | <span data-ttu-id="721d0-148">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-148">Y</span></span>        |
| <span data-ttu-id="721d0-149">引數</span><span class="sxs-lookup"><span data-stu-id="721d0-149">Arguments</span></span>      | [<span data-ttu-id="721d0-150">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-150">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-151">N</span><span class="sxs-lookup"><span data-stu-id="721d0-151">N</span></span>   | <span data-ttu-id="721d0-152">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-152">Y</span></span>        |
| <span data-ttu-id="721d0-153">元件\_</span><span class="sxs-lookup"><span data-stu-id="721d0-153">Component\_</span></span>    | [<span data-ttu-id="721d0-154">識別碼</span><span class="sxs-lookup"><span data-stu-id="721d0-154">Identifier</span></span>](identifier.md)       | <span data-ttu-id="721d0-155">N</span><span class="sxs-lookup"><span data-stu-id="721d0-155">N</span></span>   | <span data-ttu-id="721d0-156">N</span><span class="sxs-lookup"><span data-stu-id="721d0-156">N</span></span>        |
| <span data-ttu-id="721d0-157">Description</span><span class="sxs-lookup"><span data-stu-id="721d0-157">Description</span></span>    | [<span data-ttu-id="721d0-158">格式 化</span><span class="sxs-lookup"><span data-stu-id="721d0-158">Formatted</span></span>](formatted.md)         | <span data-ttu-id="721d0-159">N</span><span class="sxs-lookup"><span data-stu-id="721d0-159">N</span></span>   | <span data-ttu-id="721d0-160">Y</span><span class="sxs-lookup"><span data-stu-id="721d0-160">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="721d0-161">資料行</span><span class="sxs-lookup"><span data-stu-id="721d0-161">Columns</span></span>

<dl> <dt>

<span data-ttu-id="721d0-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="721d0-162"><span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall</span></span>
</dt> <dd>

<span data-ttu-id="721d0-163">這是資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="721d0-163">This is the primary key for the table.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="721d0-164"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="721d0-165">此資料行是提供要安裝之服務名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="721d0-165">This column is the string that gives the service name to install.</span></span> <span data-ttu-id="721d0-166">字串的長度上限為256個字元。</span><span class="sxs-lookup"><span data-stu-id="721d0-166">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="721d0-167">服務控制管理員資料庫會保留服務名稱中字元的大小寫，但服務名稱的比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="721d0-167">The service control manager database preserves the case of the characters in the service name, but comparisons of service names are case insensitive.</span></span> <span data-ttu-id="721d0-168">正斜線 (/) 和反斜線 (\\) 是不正確服務名稱字元。</span><span class="sxs-lookup"><span data-stu-id="721d0-168">Forward-slash (/) and back-slash (\\) are invalid service name characters.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span><span class="sxs-lookup"><span data-stu-id="721d0-169"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="721d0-170">此資料行是使用者介面程式用來識別服務的可當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="721d0-170">This column is the localizable string that user interface programs use to identify the service.</span></span> <span data-ttu-id="721d0-171">字串的長度上限為256個字元。</span><span class="sxs-lookup"><span data-stu-id="721d0-171">The string has a maximum length of 256 characters.</span></span> <span data-ttu-id="721d0-172">服務控制管理員會保留顯示名稱的大小寫，但顯示名稱比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="721d0-172">The service control manager preserves the case of the display name, but display name comparisons are case insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span><span class="sxs-lookup"><span data-stu-id="721d0-173"><span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType</span></span>
</dt> <dd>

<span data-ttu-id="721d0-174">此資料行是一組指定服務類型的位旗標。</span><span class="sxs-lookup"><span data-stu-id="721d0-174">This column is a set of bit flags that specify the type of service.</span></span> <span data-ttu-id="721d0-175">必須在此資料行中指定下列其中一種服務類型。</span><span class="sxs-lookup"><span data-stu-id="721d0-175">One of the following service types must be specified in this column.</span></span>



| <span data-ttu-id="721d0-176">服務類型</span><span class="sxs-lookup"><span data-stu-id="721d0-176">Type of service</span></span>                | <span data-ttu-id="721d0-177">值</span><span class="sxs-lookup"><span data-stu-id="721d0-177">Value</span></span>      | <span data-ttu-id="721d0-178">描述</span><span class="sxs-lookup"><span data-stu-id="721d0-178">Description</span></span>                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721d0-179">服務 \_ WIN32 \_ 專屬 \_ 進程</span><span class="sxs-lookup"><span data-stu-id="721d0-179">SERVICE\_WIN32\_OWN\_PROCESS</span></span>   | <span data-ttu-id="721d0-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="721d0-180">0x00000010</span></span> | <span data-ttu-id="721d0-181">執行自己的進程的 Microsoft Win32 服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-181">A Microsoft Win32 service that runs its own process.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="721d0-182">服務 \_ WIN32 \_ 共用 \_ 進程</span><span class="sxs-lookup"><span data-stu-id="721d0-182">SERVICE\_WIN32\_SHARE\_PROCESS</span></span> | <span data-ttu-id="721d0-183">0x00000020</span><span class="sxs-lookup"><span data-stu-id="721d0-183">0x00000020</span></span> | <span data-ttu-id="721d0-184">共用進程的 Win32 服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-184">A Win32 service that shares a process.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="721d0-185">服務 \_ 互動式 \_ 進程</span><span class="sxs-lookup"><span data-stu-id="721d0-185">SERVICE\_INTERACTIVE\_PROCESS</span></span>  | <span data-ttu-id="721d0-186">0x00000100</span><span class="sxs-lookup"><span data-stu-id="721d0-186">0x00000100</span></span> | <span data-ttu-id="721d0-187">與桌面互動的 Win32 服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-187">A Win32 service that interacts with the desktop.</span></span> <span data-ttu-id="721d0-188">這個值無法單獨使用，必須加入至上述兩個類型的其中一個。使用這個旗標時，StartName 資料行必須設定為 LocalSystem 或 null。</span><span class="sxs-lookup"><span data-stu-id="721d0-188">This value cannot be used alone and must be added to one of the two previous types.The StartName column must be set to LocalSystem or null when using this flag.</span></span><br/> |



 

<span data-ttu-id="721d0-189">不支援下列類型的服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-189">The following types of service are unsupported.</span></span>



| <span data-ttu-id="721d0-190">服務類型</span><span class="sxs-lookup"><span data-stu-id="721d0-190">Type of service</span></span>               | <span data-ttu-id="721d0-191">值</span><span class="sxs-lookup"><span data-stu-id="721d0-191">Value</span></span>      | <span data-ttu-id="721d0-192">描述</span><span class="sxs-lookup"><span data-stu-id="721d0-192">Description</span></span>                   |
|-------------------------------|------------|-------------------------------|
| <span data-ttu-id="721d0-193">服務 \_ 核心 \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="721d0-193">SERVICE\_KERNEL\_DRIVER</span></span>       | <span data-ttu-id="721d0-194">0x00000001</span><span class="sxs-lookup"><span data-stu-id="721d0-194">0x00000001</span></span> | <span data-ttu-id="721d0-195">驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-195">A driver service.</span></span>             |
| <span data-ttu-id="721d0-196">服務 \_ 檔 \_ 系統 \_ 驅動程式</span><span class="sxs-lookup"><span data-stu-id="721d0-196">SERVICE\_FILE\_SYSTEM\_DRIVER</span></span> | <span data-ttu-id="721d0-197">0x00000002</span><span class="sxs-lookup"><span data-stu-id="721d0-197">0x00000002</span></span> | <span data-ttu-id="721d0-198">檔案系統驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-198">A file system driver service.</span></span> |



 

</dd> <dt>

<span data-ttu-id="721d0-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType</span><span class="sxs-lookup"><span data-stu-id="721d0-199"><span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType</span></span>
</dt> <dd>

<span data-ttu-id="721d0-200">此資料行是一組位旗標，指定啟動服務的時機。</span><span class="sxs-lookup"><span data-stu-id="721d0-200">This column is a set of bit flags that specify when to start the service.</span></span> <span data-ttu-id="721d0-201">必須在此資料行中指定下列其中一種類型的服務啟動。</span><span class="sxs-lookup"><span data-stu-id="721d0-201">One of the following types of service start must be specified in this column.</span></span>



| <span data-ttu-id="721d0-202">服務啟動類型</span><span class="sxs-lookup"><span data-stu-id="721d0-202">Type of service start</span></span>  | <span data-ttu-id="721d0-203">值</span><span class="sxs-lookup"><span data-stu-id="721d0-203">Value</span></span>      | <span data-ttu-id="721d0-204">描述</span><span class="sxs-lookup"><span data-stu-id="721d0-204">Description</span></span>                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721d0-205">服務 \_ 自動 \_ 啟動</span><span class="sxs-lookup"><span data-stu-id="721d0-205">SERVICE\_AUTO\_START</span></span>   | <span data-ttu-id="721d0-206">0x00000002</span><span class="sxs-lookup"><span data-stu-id="721d0-206">0x00000002</span></span> | <span data-ttu-id="721d0-207">服務會在系統啟動時啟動。</span><span class="sxs-lookup"><span data-stu-id="721d0-207">A service start during startup of the system.</span></span>                                                              |
| <span data-ttu-id="721d0-208">服務 \_ 需求 \_ 開始</span><span class="sxs-lookup"><span data-stu-id="721d0-208">SERVICE\_DEMAND\_START</span></span> | <span data-ttu-id="721d0-209">0x00000003</span><span class="sxs-lookup"><span data-stu-id="721d0-209">0x00000003</span></span> | <span data-ttu-id="721d0-210">服務會在服務控制管理員呼叫 [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) 函數時啟動。</span><span class="sxs-lookup"><span data-stu-id="721d0-210">A service start when the service control manager calls the [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) function.</span></span> |
| <span data-ttu-id="721d0-211">服務 \_ 已停用</span><span class="sxs-lookup"><span data-stu-id="721d0-211">SERVICE\_DISABLED</span></span>      | <span data-ttu-id="721d0-212">0x00000004</span><span class="sxs-lookup"><span data-stu-id="721d0-212">0x00000004</span></span> | <span data-ttu-id="721d0-213">指定無法再啟動的服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-213">Specifies a service that can no longer be started.</span></span>                                                         |



 

<span data-ttu-id="721d0-214">Windows Installer 無法使用服務 \_ 啟動 \_ 啟動和服務 \_ 系統 \_ 啟動選項。</span><span class="sxs-lookup"><span data-stu-id="721d0-214">The Windows Installer cannot use the SERVICE\_BOOT\_START and SERVICE\_SYSTEM\_START options.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span><span class="sxs-lookup"><span data-stu-id="721d0-215"><span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl</span></span>
</dt> <dd>

<span data-ttu-id="721d0-216">如果服務在啟動期間無法啟動，則此資料行會指定啟動程式所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="721d0-216">This column specifies the action taken by the startup program if the service fails to start during startup.</span></span> <span data-ttu-id="721d0-217">這些值會影響已安裝服務的 ServiceControl StartService 事件。</span><span class="sxs-lookup"><span data-stu-id="721d0-217">These values affect the ServiceControl StartService events for installed services.</span></span> <span data-ttu-id="721d0-218">此資料行必須指定下列其中一個錯誤控制旗標。</span><span class="sxs-lookup"><span data-stu-id="721d0-218">One of the following error control flags must be specified in this column.</span></span>

<span data-ttu-id="721d0-219">將常數 **msidbServiceInstallErrorControlVital** (value = 0x08000) 新增至下表中的旗標，指定如果無法將服務安裝到系統，整體安裝應該會失敗。</span><span class="sxs-lookup"><span data-stu-id="721d0-219">Adding the constant **msidbServiceInstallErrorControlVital** (value = 0x08000) to the flags in the following table specifies that the overall install should fail if the service cannot be installed into the system.</span></span>



| <span data-ttu-id="721d0-220">錯誤控制旗標</span><span class="sxs-lookup"><span data-stu-id="721d0-220">Error control flag</span></span>       | <span data-ttu-id="721d0-221">值</span><span class="sxs-lookup"><span data-stu-id="721d0-221">Value</span></span>      | <span data-ttu-id="721d0-222">啟動程式的動作</span><span class="sxs-lookup"><span data-stu-id="721d0-222">Startup program's action</span></span>                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="721d0-223">服務 \_ 錯誤 \_ 忽略</span><span class="sxs-lookup"><span data-stu-id="721d0-223">SERVICE\_ERROR\_IGNORE</span></span>   | <span data-ttu-id="721d0-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="721d0-224">0x00000000</span></span> | <span data-ttu-id="721d0-225">記錄錯誤，並繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="721d0-225">Logs the error and continues with the startup operation.</span></span>                                                                                                                                       |
| <span data-ttu-id="721d0-226">服務 \_ 錯誤 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="721d0-226">SERVICE\_ERROR\_NORMAL</span></span>   | <span data-ttu-id="721d0-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="721d0-227">0x00000001</span></span> | <span data-ttu-id="721d0-228">記錄錯誤、顯示訊息方塊，然後繼續執行啟動作業。</span><span class="sxs-lookup"><span data-stu-id="721d0-228">Logs the error, displays a message box and continues the startup operation.</span></span>                                                                                                                    |
| <span data-ttu-id="721d0-229">服務 \_ 錯誤 \_ 嚴重</span><span class="sxs-lookup"><span data-stu-id="721d0-229">SERVICE\_ERROR\_CRITICAL</span></span> | <span data-ttu-id="721d0-230">0x00000003</span><span class="sxs-lookup"><span data-stu-id="721d0-230">0x00000003</span></span> | <span data-ttu-id="721d0-231">記錄錯誤（如果可能的話），而且系統會在最後一項已知狀況良好的情況下重新開機。</span><span class="sxs-lookup"><span data-stu-id="721d0-231">Logs the error if it is possible and the system is restarted with the last configuration known to be good.</span></span> <span data-ttu-id="721d0-232">如果正在啟動最後一個已知良好的設定，則啟動作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="721d0-232">If the last-known-good configuration is being started, the startup operation fails.</span></span> |



 

</dd> <dt>

<span data-ttu-id="721d0-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup</span><span class="sxs-lookup"><span data-stu-id="721d0-233"><span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup</span></span>
</dt> <dd>

<span data-ttu-id="721d0-234">此資料行包含的字串會為此服務所屬的載入順序群組命名。</span><span class="sxs-lookup"><span data-stu-id="721d0-234">This column contains the string that names the load ordering group of which this service is a member.</span></span> <span data-ttu-id="721d0-235">如果服務不屬於群組，請指定 null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="721d0-235">Specify null or an empty string if the service does not belong to a group.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>依賴</span><span class="sxs-lookup"><span data-stu-id="721d0-236"><span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dependencies</span></span>
</dt> <dd>

<span data-ttu-id="721d0-237">此資料行是服務名稱清單或系統必須在此服務之前啟動的載入順序群組。</span><span class="sxs-lookup"><span data-stu-id="721d0-237">This column is a list of names of services or load ordering groups that the system must start before this service.</span></span> <span data-ttu-id="721d0-238">依 Null 分隔清單中的名稱。</span><span class="sxs-lookup"><span data-stu-id="721d0-238">Separate names in the list by Nulls.</span></span> <span data-ttu-id="721d0-239">如果服務沒有相依性，請指定 Null 或空字串。</span><span class="sxs-lookup"><span data-stu-id="721d0-239">If the service has no dependencies, then specify Null or an empty string.</span></span> <span data-ttu-id="721d0-240">使用語法 \[ ~ \] 插入 Null。</span><span class="sxs-lookup"><span data-stu-id="721d0-240">Use the syntax \[~\] to insert a Null.</span></span> <span data-ttu-id="721d0-241">群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-241">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all members of the group.</span></span>

<span data-ttu-id="721d0-242">例如，若要要求系統啟動 service1 和 service2，在啟動 ServiceInstall 資料行中所列的服務之前，請在 [相依性] 資料行中輸入 service1 \[ ~ \] service2 \[ ~ \] \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="721d0-242">For example, to require that the system start service1 and service2, before starting the service listed in the ServiceInstall column, enter service1\[~\]service2\[~\]\[~\] into the Dependencies column.</span></span> <span data-ttu-id="721d0-243">Service1 和 service2 識別碼必須出現在資料表的主鍵中，或者是已安裝之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="721d0-243">The identifiers service1 and service2 must either occur in the primary key of the table or be the name of the service that is already installed.</span></span>

<span data-ttu-id="721d0-244">您必須在組名前面加上 +，使其可與服務名稱區別。</span><span class="sxs-lookup"><span data-stu-id="721d0-244">You must prefix group names with + so that they can be distinguished from a service name.</span></span> <span data-ttu-id="721d0-245">若要在啟動 ServiceInstall 資料行中所列的服務之前要求系統啟動 service1 和至少一個訂購群組 MyGroup 成員，請輸入 service1 \[ ~ \] + MyGroup \[ ~ \] \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="721d0-245">To require that the system start service1 and at least one member of the ordering group MyGroup before starting the service listed in the ServiceInstall column, enter service1\[~\]+MyGroup\[~\]\[~\].</span></span>

</dd> <dt>

<span data-ttu-id="721d0-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span><span class="sxs-lookup"><span data-stu-id="721d0-246"><span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName</span></span>
</dt> <dd>

<span data-ttu-id="721d0-247">服務會以此資料行中的字串所提供的名稱來登入。</span><span class="sxs-lookup"><span data-stu-id="721d0-247">The service is logged on as the name given by the string in this column.</span></span> <span data-ttu-id="721d0-248">如果服務類型是服務 \_ WIN32 的 \_ 進程， \_ 請使用下列格式的帳戶名稱： DomainName \\ UserName。</span><span class="sxs-lookup"><span data-stu-id="721d0-248">If the service type is SERVICE\_WIN32\_OWN\_PROCESS use an account name in the form: DomainName\\UserName.</span></span> <span data-ttu-id="721d0-249">如果帳戶屬於內建網域，則允許指定。 \\使用者。</span><span class="sxs-lookup"><span data-stu-id="721d0-249">If the account belongs to the built-in domain it is permitted to specify .\\UserName.</span></span> <span data-ttu-id="721d0-250">如果服務類型是服務 \_ WIN32 \_ 共用 \_ 進程或服務 \_ 互動式 \_ 進程，則必須使用 LocalSystem 帳戶。</span><span class="sxs-lookup"><span data-stu-id="721d0-250">The LocalSystem account must be used if the type of service is SERVICE\_WIN32\_SHARE\_PROCESS or SERVICE\_INTERACTIVE\_PROCESS.</span></span> <span data-ttu-id="721d0-251">如果將 StartName 指定為 null，且大部分服務都將此資料行保留空白，則 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) 函數會使用 LocalSystem 帳戶。</span><span class="sxs-lookup"><span data-stu-id="721d0-251">The [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function uses the LocalSystem account if StartName is specified as null and most services therefore leave this column blank.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>密碼</span><span class="sxs-lookup"><span data-stu-id="721d0-252"><span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Password</span></span>
</dt> <dd>

<span data-ttu-id="721d0-253">這個字串是 StartName 資料行中所指定之帳戶名稱的密碼。</span><span class="sxs-lookup"><span data-stu-id="721d0-253">This string is the password to the account name specified in the StartName column.</span></span> <span data-ttu-id="721d0-254">請注意，使用者必須具有以服務方式登入的許可權。</span><span class="sxs-lookup"><span data-stu-id="721d0-254">Note that the user must have permissions to log on as a service.</span></span> <span data-ttu-id="721d0-255">如果 StartName 為 null 或空字串，則服務沒有密碼。</span><span class="sxs-lookup"><span data-stu-id="721d0-255">The service has no password if StartName is null or an empty string.</span></span> <span data-ttu-id="721d0-256">LocalSystem 的 Startname 為 null，因此此實例中的密碼為 null，因此大部分的服務會將此資料行保留空白。</span><span class="sxs-lookup"><span data-stu-id="721d0-256">The Startname of LocalSystem is null, and therefore the password in this instance is null, so most services leave this column blank.</span></span>

<span data-ttu-id="721d0-257">請注意，刪除以使用者名稱和密碼安裝的服務之後，安裝程式就無法復原服務，而必須先使用自訂動作來取得密碼。</span><span class="sxs-lookup"><span data-stu-id="721d0-257">Note that after deleting a service that was installed with a user name and password, the installer cannot rollback the service without first using a custom action to get the password.</span></span> <span data-ttu-id="721d0-258">安裝程式可以取得有關服務的所有必要資訊，但密碼會儲存在系統的受保護部分中。</span><span class="sxs-lookup"><span data-stu-id="721d0-258">The installer can acquire all the necessary information about the service except the password, which is stored in a protected part of the system.</span></span> <span data-ttu-id="721d0-259">自訂動作會藉由提示使用者、從資料庫讀取屬性，或讀取檔案來取得密碼。</span><span class="sxs-lookup"><span data-stu-id="721d0-259">The custom action acquires the password by prompting the user, reading a property from the database, or reading a file.</span></span> <span data-ttu-id="721d0-260">然後，自訂動作必須呼叫 [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)，以提供密碼，才能重新安裝服務。</span><span class="sxs-lookup"><span data-stu-id="721d0-260">The custom action must then call [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga), to supply the password, before reinstalling the service.</span></span>

<span data-ttu-id="721d0-261">Windows Installer 不會將輸入密碼欄位中的值寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="721d0-261">Windows Installer does not write the value entered into the Password field into the log file.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數</span><span class="sxs-lookup"><span data-stu-id="721d0-262"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="721d0-263">此資料行包含執行服務所需的任何命令列引數或屬性。</span><span class="sxs-lookup"><span data-stu-id="721d0-263">This column contains any command line arguments or properties required to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="721d0-264"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="721d0-265">[元件資料表](component-table.md)中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="721d0-265">External key to column one of the [Component Table](component-table.md).</span></span> <span data-ttu-id="721d0-266">請注意，若要使用 InstallService 資料表安裝此服務，此元件的 KeyPath 必須是服務的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="721d0-266">Note that to install this service using the InstallService table, the KeyPath for this component must be the executable file for the service.</span></span>

</dd> <dt>

<span data-ttu-id="721d0-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="721d0-267"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="721d0-268">此資料行包含所設定之服務的可當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="721d0-268">This column contains a localizable description for the service being configured.</span></span> <span data-ttu-id="721d0-269">如果此資料行保留空白，則安裝程式會使用現有的服務描述（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="721d0-269">If this column is left blank the installer uses the existing description of the service if one exists.</span></span> <span data-ttu-id="721d0-270">如需詳細資訊，請參閱 \_ Microsoft Windows 軟體開發套件 (SDK) 中的服務描述。</span><span class="sxs-lookup"><span data-stu-id="721d0-270">For more information, see SERVICE\_DESCRIPTION in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="721d0-271">若要清除現有的描述，請 \[ ~ \] 在此資料行中輸入 ""。</span><span class="sxs-lookup"><span data-stu-id="721d0-271">To erase an existing description enter "\[~\]" in this column.</span></span> <span data-ttu-id="721d0-272">這會為新的或現有的服務產生空白描述。</span><span class="sxs-lookup"><span data-stu-id="721d0-272">This results in a blank description for either a new or existing service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="721d0-273">備註</span><span class="sxs-lookup"><span data-stu-id="721d0-273">Remarks</span></span>

<span data-ttu-id="721d0-274">[*順序資料表*](s-gly.md)中的 [InstallServices](installservices-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="721d0-274">The [InstallServices](installservices-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="721d0-275">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="721d0-275">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="721d0-276">此資料表包含 Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) 函數的大部分參數。</span><span class="sxs-lookup"><span data-stu-id="721d0-276">This table has most of the parameters to the Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="721d0-277">雖然您可以使用使用者介面來指定將服務安裝為從來源執行，但安裝程式實際上並不支援這種類型的安裝。</span><span class="sxs-lookup"><span data-stu-id="721d0-277">Although it is possible to use the user interface to specify that a service be installed as run-from-source, the installer does not actually support this type of installation.</span></span> <span data-ttu-id="721d0-278">使用本機系統的許可權層級執行的服務，必須安裝為從本機硬碟執行。</span><span class="sxs-lookup"><span data-stu-id="721d0-278">Services that run with the privilege level of the local system must be installed to run from the local hard drive.</span></span> <span data-ttu-id="721d0-279">請避免安裝可模擬特定使用者之許可權的服務，因為這可能會將安全性資料寫入至記錄檔或系統登錄。</span><span class="sxs-lookup"><span data-stu-id="721d0-279">Avoid installing services that impersonate the privileges of a particular user because this may write security data into a log or the system registry.</span></span> <span data-ttu-id="721d0-280">這可能會在系統重新開機時產生安全性問題、密碼衝突或遺失設定資料。</span><span class="sxs-lookup"><span data-stu-id="721d0-280">This can potentially create a security problem, password conflict, or the loss of configuration data when the system is restarted.</span></span>

<span data-ttu-id="721d0-281">若要在卸載期間刪除服務， [ServiceControl 資料表](servicecontrol-table.md) 中的服務必須有對應的記錄，而且 **msidbServiceControlEventUninstallDelete** 旗標必須出現在事件資料行中。</span><span class="sxs-lookup"><span data-stu-id="721d0-281">To delete a service during an uninstallation, there must be a corresponding record for the service in the [ServiceControl table](servicecontrol-table.md) and the **msidbServiceControlEventUninstallDelete** flag must appear in the Event column.</span></span> <span data-ttu-id="721d0-282">在卸載期間，安裝程式不會刪除 ServiceInstall 資料表中的服務，而不會在 ServiceControl 資料表中執行此專案。</span><span class="sxs-lookup"><span data-stu-id="721d0-282">The installer does not delete a service in the ServiceInstall table during uninstallation without this entry in the ServiceControl table.</span></span>

<span data-ttu-id="721d0-283">如需如何保護服務安全的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md)。</span><span class="sxs-lookup"><span data-stu-id="721d0-283">For information on how to secure a service see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="721d0-284">驗證</span><span class="sxs-lookup"><span data-stu-id="721d0-284">Validation</span></span>

<dl>

[<span data-ttu-id="721d0-285">ICE03</span><span class="sxs-lookup"><span data-stu-id="721d0-285">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="721d0-286">ICE06</span><span class="sxs-lookup"><span data-stu-id="721d0-286">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="721d0-287">ICE32</span><span class="sxs-lookup"><span data-stu-id="721d0-287">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="721d0-288">ICE45</span><span class="sxs-lookup"><span data-stu-id="721d0-288">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="721d0-289">ICE46</span><span class="sxs-lookup"><span data-stu-id="721d0-289">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="721d0-290">ICE66</span><span class="sxs-lookup"><span data-stu-id="721d0-290">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="721d0-291">ICE69</span><span class="sxs-lookup"><span data-stu-id="721d0-291">ICE69</span></span>](ice69.md)  
</dl>

 

 
