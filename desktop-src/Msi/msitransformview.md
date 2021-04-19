---
description: 此臨時表可針對由修補程式新增或更新的自訂動作，啟用自訂動作修補程式卸載選項。
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980598"
---
# <a name="msitransformview"></a><span data-ttu-id="ee643-103">MsiTransformView</span><span class="sxs-lookup"><span data-stu-id="ee643-103">MsiTransformView</span></span>

<span data-ttu-id="ee643-104">此臨時表可針對由修補程式新增或更新的自訂動作，啟用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee643-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="ee643-105">如果修補程式新增或更新具有 **msidbCustomActionTypePatchUninstall** 屬性的自訂動作，Windows Installer 會在卸載修補程式時執行新的或更新的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="ee643-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="ee643-106">Windows Installer 會將修補程式內的更新提供給修補程式卸載自訂動作。</span><span class="sxs-lookup"><span data-stu-id="ee643-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="ee643-107">修補程式必須包含 MsiTransformView *<PatchGUID>* 資料表，以提供此資訊給 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="ee643-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="ee643-108">此表格中的資訊可供任何立即的自訂動作使用，並無法用於延後的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="ee643-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="ee643-109">**[Windows Installer 4.0 及更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="ee643-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="ee643-110">自 Windows Installer 4.5 開始提供 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) 。</span><span class="sxs-lookup"><span data-stu-id="ee643-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="ee643-111">此資料表應命名為 MsiTransformView *<PatchGUID>* table，其中 *<PatchGUID>* 是可唯一識別修補程式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ee643-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="ee643-112">MsiTransformView *<PatchGUID>* 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="ee643-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="ee643-113">Column</span><span class="sxs-lookup"><span data-stu-id="ee643-113">Column</span></span>  | <span data-ttu-id="ee643-114">類型</span><span class="sxs-lookup"><span data-stu-id="ee643-114">Type</span></span>                         | <span data-ttu-id="ee643-115">答案</span><span class="sxs-lookup"><span data-stu-id="ee643-115">Key</span></span> | <span data-ttu-id="ee643-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="ee643-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="ee643-117">資料表</span><span class="sxs-lookup"><span data-stu-id="ee643-117">Table</span></span>   | [<span data-ttu-id="ee643-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="ee643-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="ee643-119">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-119">Y</span></span>   | <span data-ttu-id="ee643-120">N</span><span class="sxs-lookup"><span data-stu-id="ee643-120">N</span></span>        |
| <span data-ttu-id="ee643-121">Column</span><span class="sxs-lookup"><span data-stu-id="ee643-121">Column</span></span>  | [<span data-ttu-id="ee643-122">Text</span><span class="sxs-lookup"><span data-stu-id="ee643-122">Text</span></span>](text.md)             | <span data-ttu-id="ee643-123">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-123">Y</span></span>   | <span data-ttu-id="ee643-124">N</span><span class="sxs-lookup"><span data-stu-id="ee643-124">N</span></span>        |
| <span data-ttu-id="ee643-125">資料列</span><span class="sxs-lookup"><span data-stu-id="ee643-125">Row</span></span>     | [<span data-ttu-id="ee643-126">Text</span><span class="sxs-lookup"><span data-stu-id="ee643-126">Text</span></span>](text.md)             | <span data-ttu-id="ee643-127">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-127">Y</span></span>   | <span data-ttu-id="ee643-128">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-128">Y</span></span>        |
| <span data-ttu-id="ee643-129">資料</span><span class="sxs-lookup"><span data-stu-id="ee643-129">Data</span></span>    | [<span data-ttu-id="ee643-130">Text</span><span class="sxs-lookup"><span data-stu-id="ee643-130">Text</span></span>](text.md)             | <span data-ttu-id="ee643-131">N</span><span class="sxs-lookup"><span data-stu-id="ee643-131">N</span></span>   | <span data-ttu-id="ee643-132">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-132">Y</span></span>        |
| <span data-ttu-id="ee643-133">目前</span><span class="sxs-lookup"><span data-stu-id="ee643-133">Current</span></span> | [<span data-ttu-id="ee643-134">Text</span><span class="sxs-lookup"><span data-stu-id="ee643-134">Text</span></span>](text.md)             | <span data-ttu-id="ee643-135">N</span><span class="sxs-lookup"><span data-stu-id="ee643-135">N</span></span>   | <span data-ttu-id="ee643-136">Y</span><span class="sxs-lookup"><span data-stu-id="ee643-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="ee643-137">Column</span><span class="sxs-lookup"><span data-stu-id="ee643-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="ee643-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="ee643-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="ee643-139">改變的資料庫資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ee643-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="ee643-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>列</span><span class="sxs-lookup"><span data-stu-id="ee643-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="ee643-141">改變的資料表資料行名稱，或插入、刪除、建立或卸載。</span><span class="sxs-lookup"><span data-stu-id="ee643-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="ee643-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>行</span><span class="sxs-lookup"><span data-stu-id="ee643-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="ee643-143">以定位字元分隔的主鍵值清單。</span><span class="sxs-lookup"><span data-stu-id="ee643-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="ee643-144">Null 主鍵值是以單一空白字元表示。</span><span class="sxs-lookup"><span data-stu-id="ee643-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="ee643-145">此資料行中的 Null 值表示架構變更。</span><span class="sxs-lookup"><span data-stu-id="ee643-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="ee643-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>資料</span><span class="sxs-lookup"><span data-stu-id="ee643-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="ee643-147">資料、資料流程的名稱或資料行定義。</span><span class="sxs-lookup"><span data-stu-id="ee643-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="ee643-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>當前</span><span class="sxs-lookup"><span data-stu-id="ee643-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="ee643-149">參考資料庫的目前值，或資料行 a 數位。</span><span class="sxs-lookup"><span data-stu-id="ee643-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee643-150">備註</span><span class="sxs-lookup"><span data-stu-id="ee643-150">Remarks</span></span>

<span data-ttu-id="ee643-151">修補程式卸載時，修補卸載自訂動作執行。</span><span class="sxs-lookup"><span data-stu-id="ee643-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="ee643-152">卸載產品時，不會執行這些功能。</span><span class="sxs-lookup"><span data-stu-id="ee643-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="ee643-153">使用 [自訂動作修補程式卸載選項](custom-action-patch-uninstall-option.md) ，此資料表可在卸載修補程式時執行自訂。</span><span class="sxs-lookup"><span data-stu-id="ee643-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="ee643-154">修補程式可以更新原始封裝 ( .msi 檔案中提供的自訂動作。 ) 在卸載修補程式時執行自訂動作的更新版本，請在原始封裝中將 **msidbCustomActionTypePatchUninstall** 屬性標示為自訂動作。</span><span class="sxs-lookup"><span data-stu-id="ee643-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



