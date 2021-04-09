---
description: ProgId 資料表包含程式識別碼和版本獨立程式識別碼的相關資訊，這些程式識別碼必須在產品公告中產生。
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: ProgId 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945254"
---
# <a name="progid-table"></a><span data-ttu-id="46112-103">ProgId 資料表</span><span class="sxs-lookup"><span data-stu-id="46112-103">ProgId Table</span></span>

<span data-ttu-id="46112-104">ProgId 資料表包含程式識別碼和版本獨立程式識別碼的相關資訊，這些程式識別碼必須在產品公告中產生。</span><span class="sxs-lookup"><span data-stu-id="46112-104">The ProgId table contains information for program IDs and version independent program IDs that must be generated as a part of the product advertisement.</span></span>

<span data-ttu-id="46112-105">ProgId 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="46112-105">The ProgId table has the following columns.</span></span>



| <span data-ttu-id="46112-106">Column</span><span class="sxs-lookup"><span data-stu-id="46112-106">Column</span></span>         | <span data-ttu-id="46112-107">類型</span><span class="sxs-lookup"><span data-stu-id="46112-107">Type</span></span>                         | <span data-ttu-id="46112-108">答案</span><span class="sxs-lookup"><span data-stu-id="46112-108">Key</span></span> | <span data-ttu-id="46112-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="46112-109">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="46112-110">ProgId</span><span class="sxs-lookup"><span data-stu-id="46112-110">ProgId</span></span>         | [<span data-ttu-id="46112-111">Text</span><span class="sxs-lookup"><span data-stu-id="46112-111">Text</span></span>](text.md)             | <span data-ttu-id="46112-112">Y</span><span class="sxs-lookup"><span data-stu-id="46112-112">Y</span></span>   | <span data-ttu-id="46112-113">N</span><span class="sxs-lookup"><span data-stu-id="46112-113">N</span></span>        |
| <span data-ttu-id="46112-114">ProgId \_ 父系</span><span class="sxs-lookup"><span data-stu-id="46112-114">ProgId\_Parent</span></span> | [<span data-ttu-id="46112-115">Text</span><span class="sxs-lookup"><span data-stu-id="46112-115">Text</span></span>](text.md)             | <span data-ttu-id="46112-116">N</span><span class="sxs-lookup"><span data-stu-id="46112-116">N</span></span>   | <span data-ttu-id="46112-117">Y</span><span class="sxs-lookup"><span data-stu-id="46112-117">Y</span></span>        |
| <span data-ttu-id="46112-118">類別\_</span><span class="sxs-lookup"><span data-stu-id="46112-118">Class\_</span></span>        | [<span data-ttu-id="46112-119">GUID</span><span class="sxs-lookup"><span data-stu-id="46112-119">GUID</span></span>](guid.md)             | <span data-ttu-id="46112-120">N</span><span class="sxs-lookup"><span data-stu-id="46112-120">N</span></span>   | <span data-ttu-id="46112-121">Y</span><span class="sxs-lookup"><span data-stu-id="46112-121">Y</span></span>        |
| <span data-ttu-id="46112-122">Description</span><span class="sxs-lookup"><span data-stu-id="46112-122">Description</span></span>    | [<span data-ttu-id="46112-123">Text</span><span class="sxs-lookup"><span data-stu-id="46112-123">Text</span></span>](text.md)             | <span data-ttu-id="46112-124">N</span><span class="sxs-lookup"><span data-stu-id="46112-124">N</span></span>   | <span data-ttu-id="46112-125">Y</span><span class="sxs-lookup"><span data-stu-id="46112-125">Y</span></span>        |
| <span data-ttu-id="46112-126">圖示\_</span><span class="sxs-lookup"><span data-stu-id="46112-126">Icon\_</span></span>         | [<span data-ttu-id="46112-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="46112-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="46112-128">N</span><span class="sxs-lookup"><span data-stu-id="46112-128">N</span></span>   | <span data-ttu-id="46112-129">Y</span><span class="sxs-lookup"><span data-stu-id="46112-129">Y</span></span>        |
| <span data-ttu-id="46112-130">>iconindex</span><span class="sxs-lookup"><span data-stu-id="46112-130">IconIndex</span></span>      | [<span data-ttu-id="46112-131">整數</span><span class="sxs-lookup"><span data-stu-id="46112-131">Integer</span></span>](integer.md)       | <span data-ttu-id="46112-132">N</span><span class="sxs-lookup"><span data-stu-id="46112-132">N</span></span>   | <span data-ttu-id="46112-133">Y</span><span class="sxs-lookup"><span data-stu-id="46112-133">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="46112-134">資料行</span><span class="sxs-lookup"><span data-stu-id="46112-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="46112-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span><span class="sxs-lookup"><span data-stu-id="46112-135"><span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId</span></span>
</dt> <dd>

<span data-ttu-id="46112-136">程式識別碼或版本獨立的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="46112-136">The program ID or version independent program ID.</span></span> <span data-ttu-id="46112-137">如果此資料表的類別資料行中所列的 CLSID \_ 已排程要進行公告或安裝，則會註冊 ProgId 資料表中所列的 progid。</span><span class="sxs-lookup"><span data-stu-id="46112-137">ProgIds listed in the ProgId table are registered if the CLSID listed in the Class\_column of this table is scheduled to be advertised or installed.</span></span> <span data-ttu-id="46112-138">選取 ProgId 以進行註冊時，也會選取透過 ProgId 父資料行參考此資料 \_ 列的所有 progid 進行註冊。</span><span class="sxs-lookup"><span data-stu-id="46112-138">When the ProgId is selected for registration, all ProgIds that refer to this row through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="46112-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ 父系</span><span class="sxs-lookup"><span data-stu-id="46112-139"><span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId\_Parent</span></span>
</dt> <dd>

<span data-ttu-id="46112-140">只定義為版本獨立的程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="46112-140">Defined only for version independent program IDs.</span></span> <span data-ttu-id="46112-141">此欄位是 ProgId 資料行中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="46112-141">This field is a foreign key into the ProgId column.</span></span> <span data-ttu-id="46112-142">若要定義版本獨立程式識別碼，請在 ProgId 父資料行中輸入對應的 ProgId \_ 。</span><span class="sxs-lookup"><span data-stu-id="46112-142">To define a version independent program ID, enter the corresponding ProgId into the ProgId\_Parent column.</span></span> <span data-ttu-id="46112-143">選取 ProgId 以進行安裝時，也會選取透過 ProgId 父資料行相關聯的對應與版本無關的 Progid \_ 來進行註冊。</span><span class="sxs-lookup"><span data-stu-id="46112-143">When the ProgId is selected for installation, the corresponding version-independent ProgIds associated through the ProgId\_Parent column are also selected for registration.</span></span>

</dd> <dt>

<span data-ttu-id="46112-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>類\_</span><span class="sxs-lookup"><span data-stu-id="46112-144"><span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Class\_</span></span>
</dt> <dd>

<span data-ttu-id="46112-145">[類別資料表](class-table.md)中的選擇性外鍵。</span><span class="sxs-lookup"><span data-stu-id="46112-145">An optional foreign key into the [Class table](class-table.md).</span></span> <span data-ttu-id="46112-146">針對版本獨立的 ProgId，此資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="46112-146">This column must be Null for a version independent ProgId.</span></span> <span data-ttu-id="46112-147">如果 ProgId 的類別值為 null，則會在延伸模組資料表中的資料 \_ 列的 progid 資料行中出現 progid 時[](extension-table.md)註冊，而且此延伸模組在[動詞資料表](verb-table.md)中至少有一個與其相關聯的動詞。</span><span class="sxs-lookup"><span data-stu-id="46112-147">If the Class\_value for a ProgId is null, the ProgId is registered when it appears in the ProgId column of a row in the [Extension table](extension-table.md) and the extension has at least one Verb associated with it in the [Verb table](verb-table.md).</span></span> <span data-ttu-id="46112-148">以這種方式選取以進行註冊的 Progid，不會安裝透過 ProgId 預設值參考目前 ProgId 的其他 Progid \_ 。</span><span class="sxs-lookup"><span data-stu-id="46112-148">ProgIds selected for registration in this manner do not install other ProgIds that reference the current ProgId through the ProgId\_Default value.</span></span>

</dd> <dt>

<span data-ttu-id="46112-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="46112-149"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="46112-150">相關聯程式識別碼的選擇性當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="46112-150">An optional localized description of the associated program ID.</span></span>

</dd> <dt>

<span data-ttu-id="46112-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_</span><span class="sxs-lookup"><span data-stu-id="46112-151"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="46112-152">[圖示表格](icon-table.md)中的選擇性外鍵，可指定與這個 ProgId 相關聯的圖示檔。</span><span class="sxs-lookup"><span data-stu-id="46112-152">An optional foreign key into the [Icon table](icon-table.md) that specifies the icon file associated with this ProgId.</span></span> <span data-ttu-id="46112-153">這會寫入與此 ProgId 相關聯的 DefaultIcon 索引鍵下。</span><span class="sxs-lookup"><span data-stu-id="46112-153">This is written under the DefaultIcon key associated with this ProgId.</span></span> <span data-ttu-id="46112-154">針對版本獨立的 ProgId，此資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="46112-154">This column must be Null for a version independent ProgId.</span></span>

</dd> <dt>

<span data-ttu-id="46112-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex</span><span class="sxs-lookup"><span data-stu-id="46112-155"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="46112-156">圖示檔中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="46112-156">The Icon index into the icon file.</span></span> <span data-ttu-id="46112-157">針對版本獨立的 ProgId，此資料行必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="46112-157">This column must be Null for a version independent ProgId.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46112-158">備註</span><span class="sxs-lookup"><span data-stu-id="46112-158">Remarks</span></span>

<span data-ttu-id="46112-159">[*順序資料表*](s-gly.md)中的 [RegisterProgIdInfo](registerprogidinfo-action.md)和 [UnregisterProgIdInfo](unregisterprogidinfo-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="46112-159">The [RegisterProgIdInfo](registerprogidinfo-action.md) and [UnregisterProgIdInfo](unregisterprogidinfo-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="46112-160">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="46112-160">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="46112-161">驗證</span><span class="sxs-lookup"><span data-stu-id="46112-161">Validation</span></span>

<dl>

[<span data-ttu-id="46112-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="46112-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="46112-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="46112-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="46112-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="46112-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="46112-165">ICE36</span><span class="sxs-lookup"><span data-stu-id="46112-165">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="46112-166">ICE89</span><span class="sxs-lookup"><span data-stu-id="46112-166">ICE89</span></span>](ice89.md)  
</dl>

 

 



