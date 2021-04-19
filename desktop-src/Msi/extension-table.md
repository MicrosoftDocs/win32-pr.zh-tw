---
description: 延伸模組資料表包含必須在產品公告中產生的副檔名伺服器的相關資訊。 每個資料列都會產生一組登錄機碼和值。
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: 延伸模組資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974178"
---
# <a name="extension-table"></a><span data-ttu-id="88946-104">延伸模組資料表</span><span class="sxs-lookup"><span data-stu-id="88946-104">Extension Table</span></span>

<span data-ttu-id="88946-105">延伸模組資料表包含必須在產品公告中產生的副檔名伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88946-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="88946-106">每個資料列都會產生一組登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="88946-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="88946-107">延伸模組資料表包含下表所示的資料行。</span><span class="sxs-lookup"><span data-stu-id="88946-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="88946-108">Column</span><span class="sxs-lookup"><span data-stu-id="88946-108">Column</span></span>      | <span data-ttu-id="88946-109">類型</span><span class="sxs-lookup"><span data-stu-id="88946-109">Type</span></span>                         | <span data-ttu-id="88946-110">答案</span><span class="sxs-lookup"><span data-stu-id="88946-110">Key</span></span> | <span data-ttu-id="88946-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="88946-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="88946-112">分機</span><span class="sxs-lookup"><span data-stu-id="88946-112">Extension</span></span>   | [<span data-ttu-id="88946-113">Text</span><span class="sxs-lookup"><span data-stu-id="88946-113">Text</span></span>](text.md)             | <span data-ttu-id="88946-114">Y</span><span class="sxs-lookup"><span data-stu-id="88946-114">Y</span></span>   | <span data-ttu-id="88946-115">N</span><span class="sxs-lookup"><span data-stu-id="88946-115">N</span></span>        |
| <span data-ttu-id="88946-116">元件\_</span><span class="sxs-lookup"><span data-stu-id="88946-116">Component\_</span></span> | [<span data-ttu-id="88946-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="88946-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="88946-118">Y</span><span class="sxs-lookup"><span data-stu-id="88946-118">Y</span></span>   | <span data-ttu-id="88946-119">N</span><span class="sxs-lookup"><span data-stu-id="88946-119">N</span></span>        |
| <span data-ttu-id="88946-120">ProgId\_</span><span class="sxs-lookup"><span data-stu-id="88946-120">ProgId\_</span></span>    | [<span data-ttu-id="88946-121">Text</span><span class="sxs-lookup"><span data-stu-id="88946-121">Text</span></span>](text.md)             | <span data-ttu-id="88946-122">N</span><span class="sxs-lookup"><span data-stu-id="88946-122">N</span></span>   | <span data-ttu-id="88946-123">Y</span><span class="sxs-lookup"><span data-stu-id="88946-123">Y</span></span>        |
| <span data-ttu-id="88946-124">MIME\_</span><span class="sxs-lookup"><span data-stu-id="88946-124">MIME\_</span></span>      | [<span data-ttu-id="88946-125">Text</span><span class="sxs-lookup"><span data-stu-id="88946-125">Text</span></span>](text.md)             | <span data-ttu-id="88946-126">N</span><span class="sxs-lookup"><span data-stu-id="88946-126">N</span></span>   | <span data-ttu-id="88946-127">Y</span><span class="sxs-lookup"><span data-stu-id="88946-127">Y</span></span>        |
| <span data-ttu-id="88946-128">功能\_</span><span class="sxs-lookup"><span data-stu-id="88946-128">Feature\_</span></span>   | [<span data-ttu-id="88946-129">識別碼</span><span class="sxs-lookup"><span data-stu-id="88946-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="88946-130">N</span><span class="sxs-lookup"><span data-stu-id="88946-130">N</span></span>   | <span data-ttu-id="88946-131">N</span><span class="sxs-lookup"><span data-stu-id="88946-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="88946-132">資料行</span><span class="sxs-lookup"><span data-stu-id="88946-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="88946-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>擴展</span><span class="sxs-lookup"><span data-stu-id="88946-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="88946-134">與資料表資料列相關聯的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="88946-134">The extension associated with the table row.</span></span> <span data-ttu-id="88946-135">延伸模組的長度最多可達255個字元。</span><span class="sxs-lookup"><span data-stu-id="88946-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="88946-136">在此欄位中輸入延伸模組，但不含前置句點。</span><span class="sxs-lookup"><span data-stu-id="88946-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="88946-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="88946-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="88946-138">[元件](component-table.md)資料表第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="88946-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="88946-139">此資料行參考控制延伸模組安裝的元件。</span><span class="sxs-lookup"><span data-stu-id="88946-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="88946-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span><span class="sxs-lookup"><span data-stu-id="88946-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="88946-141">與此延伸模組相關聯的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="88946-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="88946-142">這是 [ProgId](progid-table.md) 資料表中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="88946-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="88946-143"><span id="MIME_"></span><span id="mime_"></span>Mime\_</span><span class="sxs-lookup"><span data-stu-id="88946-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="88946-144">要為延伸模組資料行撰寫的內容類型。</span><span class="sxs-lookup"><span data-stu-id="88946-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="88946-145">[MIME](mime-table.md)資料表第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="88946-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="88946-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="88946-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="88946-147">在 [功能](feature-table.md) 資料表的第一個資料行中，指定提供延伸模組伺服器之功能的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="88946-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88946-148">備註</span><span class="sxs-lookup"><span data-stu-id="88946-148">Remarks</span></span>

<span data-ttu-id="88946-149">執行 [RegisterExtensionInfo](registerextensioninfo-action.md) 動作或 [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) 動作時，會參考延伸模組資料表。</span><span class="sxs-lookup"><span data-stu-id="88946-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="88946-150">驗證</span><span class="sxs-lookup"><span data-stu-id="88946-150">Validation</span></span>

<dl>

[<span data-ttu-id="88946-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="88946-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="88946-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="88946-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="88946-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="88946-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="88946-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="88946-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="88946-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="88946-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="88946-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="88946-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="88946-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="88946-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



