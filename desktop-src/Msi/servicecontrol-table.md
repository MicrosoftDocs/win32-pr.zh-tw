---
description: ServiceControl 資料表是用來控制已安裝或已卸載的服務。注意：相依于全域組件快取中之元件的服務 (GAC) 無法使用 ServiceInstall 和 ServiceControl 資料表來安裝或啟動。
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: ServiceControl 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693724"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="2374a-103">ServiceControl 資料表</span><span class="sxs-lookup"><span data-stu-id="2374a-103">ServiceControl Table</span></span>

<span data-ttu-id="2374a-104">ServiceControl 資料表是用來控制已安裝或已卸載的服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="2374a-105">依賴全域組件快取中的 [元件](assemblies.md) 存在 (GAC) 的服務無法使用 [ServiceInstall](serviceinstall-table.md) 和 ServiceControl 資料表來安裝或啟動。</span><span class="sxs-lookup"><span data-stu-id="2374a-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="2374a-106">如果您需要啟動相依于 GAC 中元件的服務，您必須使用 [InstallFinalize 動作](installfinalize-action.md) 或 [認可自訂動作](commit-custom-actions.md)之後排序的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="2374a-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="2374a-107">如需將元件安裝至 GAC 的詳細資訊，請參閱將元件 [安裝到全域組件快取](installation-of-assemblies-to-the-global-assembly-cache.md)。</span><span class="sxs-lookup"><span data-stu-id="2374a-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="2374a-108">ServiceControl 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="2374a-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="2374a-109">Column</span><span class="sxs-lookup"><span data-stu-id="2374a-109">Column</span></span>         | <span data-ttu-id="2374a-110">類型</span><span class="sxs-lookup"><span data-stu-id="2374a-110">Type</span></span>                         | <span data-ttu-id="2374a-111">答案</span><span class="sxs-lookup"><span data-stu-id="2374a-111">Key</span></span> | <span data-ttu-id="2374a-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="2374a-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="2374a-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="2374a-113">ServiceControl</span></span> | [<span data-ttu-id="2374a-114">識別碼</span><span class="sxs-lookup"><span data-stu-id="2374a-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="2374a-115">Y</span><span class="sxs-lookup"><span data-stu-id="2374a-115">Y</span></span>   | <span data-ttu-id="2374a-116">N</span><span class="sxs-lookup"><span data-stu-id="2374a-116">N</span></span>        |
| <span data-ttu-id="2374a-117">Name</span><span class="sxs-lookup"><span data-stu-id="2374a-117">Name</span></span>           | [<span data-ttu-id="2374a-118">格式 化</span><span class="sxs-lookup"><span data-stu-id="2374a-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2374a-119">N</span><span class="sxs-lookup"><span data-stu-id="2374a-119">N</span></span>   | <span data-ttu-id="2374a-120">N</span><span class="sxs-lookup"><span data-stu-id="2374a-120">N</span></span>        |
| <span data-ttu-id="2374a-121">事件</span><span class="sxs-lookup"><span data-stu-id="2374a-121">Event</span></span>          | [<span data-ttu-id="2374a-122">整數</span><span class="sxs-lookup"><span data-stu-id="2374a-122">Integer</span></span>](integer.md)       | <span data-ttu-id="2374a-123">N</span><span class="sxs-lookup"><span data-stu-id="2374a-123">N</span></span>   | <span data-ttu-id="2374a-124">N</span><span class="sxs-lookup"><span data-stu-id="2374a-124">N</span></span>        |
| <span data-ttu-id="2374a-125">引數</span><span class="sxs-lookup"><span data-stu-id="2374a-125">Arguments</span></span>      | [<span data-ttu-id="2374a-126">格式 化</span><span class="sxs-lookup"><span data-stu-id="2374a-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="2374a-127">N</span><span class="sxs-lookup"><span data-stu-id="2374a-127">N</span></span>   | <span data-ttu-id="2374a-128">Y</span><span class="sxs-lookup"><span data-stu-id="2374a-128">Y</span></span>        |
| <span data-ttu-id="2374a-129">等候</span><span class="sxs-lookup"><span data-stu-id="2374a-129">Wait</span></span>           | [<span data-ttu-id="2374a-130">整數</span><span class="sxs-lookup"><span data-stu-id="2374a-130">Integer</span></span>](integer.md)       | <span data-ttu-id="2374a-131">N</span><span class="sxs-lookup"><span data-stu-id="2374a-131">N</span></span>   | <span data-ttu-id="2374a-132">Y</span><span class="sxs-lookup"><span data-stu-id="2374a-132">Y</span></span>        |
| <span data-ttu-id="2374a-133">元件\_</span><span class="sxs-lookup"><span data-stu-id="2374a-133">Component\_</span></span>    | [<span data-ttu-id="2374a-134">識別碼</span><span class="sxs-lookup"><span data-stu-id="2374a-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="2374a-135">N</span><span class="sxs-lookup"><span data-stu-id="2374a-135">N</span></span>   | <span data-ttu-id="2374a-136">N</span><span class="sxs-lookup"><span data-stu-id="2374a-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2374a-137">資料行</span><span class="sxs-lookup"><span data-stu-id="2374a-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2374a-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="2374a-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="2374a-139">這是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2374a-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="2374a-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="2374a-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="2374a-141">此資料行是為服務命名的字串。</span><span class="sxs-lookup"><span data-stu-id="2374a-141">This column is the string naming the service.</span></span> <span data-ttu-id="2374a-142">您可以使用這個資料行來控制未安裝的服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="2374a-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>事件</span><span class="sxs-lookup"><span data-stu-id="2374a-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="2374a-144">此資料行包含要在命名服務上執行的作業。</span><span class="sxs-lookup"><span data-stu-id="2374a-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="2374a-145">請注意，當您停止服務時，所有相依于該服務的服務也會停止。</span><span class="sxs-lookup"><span data-stu-id="2374a-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="2374a-146">當刪除正在執行的服務時，安裝程式會停止服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="2374a-147">此欄位中的值是位欄位，可以合併成代表數個作業的單一值。</span><span class="sxs-lookup"><span data-stu-id="2374a-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="2374a-148">下列值只會在安裝期間使用。</span><span class="sxs-lookup"><span data-stu-id="2374a-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="2374a-149">常數</span><span class="sxs-lookup"><span data-stu-id="2374a-149">Constant</span></span>                           | <span data-ttu-id="2374a-150">十六進位</span><span class="sxs-lookup"><span data-stu-id="2374a-150">Hexadecimal</span></span> | <span data-ttu-id="2374a-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="2374a-151">Decimal</span></span> | <span data-ttu-id="2374a-152">Description</span><span class="sxs-lookup"><span data-stu-id="2374a-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2374a-153">**msidbServiceControlEventStart**</span><span class="sxs-lookup"><span data-stu-id="2374a-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="2374a-154">0x001</span><span class="sxs-lookup"><span data-stu-id="2374a-154">0x001</span></span>       | <span data-ttu-id="2374a-155">1</span><span class="sxs-lookup"><span data-stu-id="2374a-155">1</span></span>       | <span data-ttu-id="2374a-156">在 [StartServices 動作](startservices-action.md)期間啟動服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="2374a-157">**msidbServiceControlEventStop**</span><span class="sxs-lookup"><span data-stu-id="2374a-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="2374a-158">0x002</span><span class="sxs-lookup"><span data-stu-id="2374a-158">0x002</span></span>       | <span data-ttu-id="2374a-159">2</span><span class="sxs-lookup"><span data-stu-id="2374a-159">2</span></span>       | <span data-ttu-id="2374a-160">在 [StopServices 動作](stopservices-action.md)期間停止服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="2374a-161">(無)</span><span class="sxs-lookup"><span data-stu-id="2374a-161">(none)</span></span>                             | <span data-ttu-id="2374a-162">0x004</span><span class="sxs-lookup"><span data-stu-id="2374a-162">0x004</span></span>       | <span data-ttu-id="2374a-163">4</span><span class="sxs-lookup"><span data-stu-id="2374a-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="2374a-164">**msidbServiceControlEventDelete**</span><span class="sxs-lookup"><span data-stu-id="2374a-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="2374a-165">0x008</span><span class="sxs-lookup"><span data-stu-id="2374a-165">0x008</span></span>       | <span data-ttu-id="2374a-166">8</span><span class="sxs-lookup"><span data-stu-id="2374a-166">8</span></span>       | <span data-ttu-id="2374a-167">在 [DeleteServices 動作](deleteservices-action.md)期間刪除服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="2374a-168">下列值只會在卸載期間使用。</span><span class="sxs-lookup"><span data-stu-id="2374a-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="2374a-169">常數</span><span class="sxs-lookup"><span data-stu-id="2374a-169">Constant</span></span>                                    | <span data-ttu-id="2374a-170">十六進位</span><span class="sxs-lookup"><span data-stu-id="2374a-170">Hexadecimal</span></span> | <span data-ttu-id="2374a-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="2374a-171">Decimal</span></span> | <span data-ttu-id="2374a-172">Description</span><span class="sxs-lookup"><span data-stu-id="2374a-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2374a-173">**msidbServiceControlEventUninstallStart**</span><span class="sxs-lookup"><span data-stu-id="2374a-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="2374a-174">0x010</span><span class="sxs-lookup"><span data-stu-id="2374a-174">0x010</span></span>       | <span data-ttu-id="2374a-175">16</span><span class="sxs-lookup"><span data-stu-id="2374a-175">16</span></span>      | <span data-ttu-id="2374a-176">在 [StartServices 動作](startservices-action.md)期間啟動服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="2374a-177">**msidbServiceControlEventUninstallStop**</span><span class="sxs-lookup"><span data-stu-id="2374a-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="2374a-178">0x020</span><span class="sxs-lookup"><span data-stu-id="2374a-178">0x020</span></span>       | <span data-ttu-id="2374a-179">32</span><span class="sxs-lookup"><span data-stu-id="2374a-179">32</span></span>      | <span data-ttu-id="2374a-180">在 [StopServices 動作](stopservices-action.md)期間停止服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="2374a-181">(無)</span><span class="sxs-lookup"><span data-stu-id="2374a-181">(none)</span></span>                                      | <span data-ttu-id="2374a-182">0x040</span><span class="sxs-lookup"><span data-stu-id="2374a-182">0x040</span></span>       | <span data-ttu-id="2374a-183">64</span><span class="sxs-lookup"><span data-stu-id="2374a-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="2374a-184">**msidbServiceControlEventUninstallDelete**</span><span class="sxs-lookup"><span data-stu-id="2374a-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="2374a-185">0x080</span><span class="sxs-lookup"><span data-stu-id="2374a-185">0x080</span></span>       | <span data-ttu-id="2374a-186">128</span><span class="sxs-lookup"><span data-stu-id="2374a-186">128</span></span>     | <span data-ttu-id="2374a-187">在 [DeleteServices 動作](deleteservices-action.md)期間刪除服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="2374a-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>參數</span><span class="sxs-lookup"><span data-stu-id="2374a-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="2374a-189">用於啟動服務的引數清單。</span><span class="sxs-lookup"><span data-stu-id="2374a-189">A list of arguments for starting services.</span></span> <span data-ttu-id="2374a-190">引數是以 null 字元分隔 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="2374a-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="2374a-191">例如，引數清單一、二和三列為： \[ ~ \] 兩個引數 \[ ~ \] 。</span><span class="sxs-lookup"><span data-stu-id="2374a-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="2374a-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>等</span><span class="sxs-lookup"><span data-stu-id="2374a-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="2374a-193">將此欄位保留為 null 或輸入值1，會導致安裝程式等候最多30秒，讓服務完成後再繼續。</span><span class="sxs-lookup"><span data-stu-id="2374a-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="2374a-194">等候可以用來允許重大事件的額外時間傳回失敗錯誤。</span><span class="sxs-lookup"><span data-stu-id="2374a-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="2374a-195">在此欄位中，值為0表示只等候，直到服務控制管理員 (SCM) 報告此服務處於擱置狀態，再繼續進行安裝。</span><span class="sxs-lookup"><span data-stu-id="2374a-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="2374a-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="2374a-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="2374a-197">[元件資料表](component-table.md)中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2374a-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2374a-198">備註</span><span class="sxs-lookup"><span data-stu-id="2374a-198">Remarks</span></span>

<span data-ttu-id="2374a-199">[*順序資料表*](s-gly.md)中的 [StartServices](startservices-action.md)、 [StopServices](stopservices-action.md)和 [DeleteServices](deleteservices-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="2374a-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="2374a-200">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="2374a-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="2374a-201">使用 [名稱] 欄來啟動、停止或刪除由安裝所取代的服務，或是相依于所安裝之新服務的服務。</span><span class="sxs-lookup"><span data-stu-id="2374a-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="2374a-202">例如，在 ServiceControl 資料行中輸入 MyService 可以將此服務系結至元件資料行中的 MyComponent \_ 。</span><span class="sxs-lookup"><span data-stu-id="2374a-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="2374a-203">如果在安裝時將事件資料行中的位欄位設定為 [啟動]，則安裝程式會在安裝 MyComponent 時開始 MyService。</span><span class="sxs-lookup"><span data-stu-id="2374a-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="2374a-204">驗證</span><span class="sxs-lookup"><span data-stu-id="2374a-204">Validation</span></span>

<dl>

[<span data-ttu-id="2374a-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="2374a-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2374a-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="2374a-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2374a-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="2374a-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2374a-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="2374a-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="2374a-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="2374a-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2374a-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="2374a-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



