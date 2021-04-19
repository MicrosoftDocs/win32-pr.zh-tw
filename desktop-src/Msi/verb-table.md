---
description: 動詞資料表包含與副檔名相關的命令動詞資訊，必須在產品公告中產生。 每個資料列都會產生一組登錄機碼和值。
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: 動詞資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7182c425e2613aa463f94bca0e6a1e62c1504c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976606"
---
# <a name="verb-table"></a><span data-ttu-id="cf96d-104">動詞資料表</span><span class="sxs-lookup"><span data-stu-id="cf96d-104">Verb Table</span></span>

<span data-ttu-id="cf96d-105">動詞資料表包含與副檔名相關的命令動詞資訊，必須在產品公告中產生。</span><span class="sxs-lookup"><span data-stu-id="cf96d-105">The Verb table contains command-verb information associated with file name extensions that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="cf96d-106">每個資料列都會產生一組登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="cf96d-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="cf96d-107">動詞資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="cf96d-107">The Verb table has the following columns.</span></span>



| <span data-ttu-id="cf96d-108">Column</span><span class="sxs-lookup"><span data-stu-id="cf96d-108">Column</span></span>      | <span data-ttu-id="cf96d-109">類型</span><span class="sxs-lookup"><span data-stu-id="cf96d-109">Type</span></span>                       | <span data-ttu-id="cf96d-110">答案</span><span class="sxs-lookup"><span data-stu-id="cf96d-110">Key</span></span> | <span data-ttu-id="cf96d-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="cf96d-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="cf96d-112">分機\_</span><span class="sxs-lookup"><span data-stu-id="cf96d-112">Extension\_</span></span> | [<span data-ttu-id="cf96d-113">Text</span><span class="sxs-lookup"><span data-stu-id="cf96d-113">Text</span></span>](text.md)           | <span data-ttu-id="cf96d-114">Y</span><span class="sxs-lookup"><span data-stu-id="cf96d-114">Y</span></span>   | <span data-ttu-id="cf96d-115">N</span><span class="sxs-lookup"><span data-stu-id="cf96d-115">N</span></span>        |
| <span data-ttu-id="cf96d-116">動詞命令</span><span class="sxs-lookup"><span data-stu-id="cf96d-116">Verb</span></span>        | [<span data-ttu-id="cf96d-117">Text</span><span class="sxs-lookup"><span data-stu-id="cf96d-117">Text</span></span>](text.md)           | <span data-ttu-id="cf96d-118">Y</span><span class="sxs-lookup"><span data-stu-id="cf96d-118">Y</span></span>   | <span data-ttu-id="cf96d-119">N</span><span class="sxs-lookup"><span data-stu-id="cf96d-119">N</span></span>        |
| <span data-ttu-id="cf96d-120">順序</span><span class="sxs-lookup"><span data-stu-id="cf96d-120">Sequence</span></span>    | [<span data-ttu-id="cf96d-121">整數</span><span class="sxs-lookup"><span data-stu-id="cf96d-121">Integer</span></span>](integer.md)     | <span data-ttu-id="cf96d-122">N</span><span class="sxs-lookup"><span data-stu-id="cf96d-122">N</span></span>   | <span data-ttu-id="cf96d-123">Y</span><span class="sxs-lookup"><span data-stu-id="cf96d-123">Y</span></span>        |
| <span data-ttu-id="cf96d-124">Command</span><span class="sxs-lookup"><span data-stu-id="cf96d-124">Command</span></span>     | [<span data-ttu-id="cf96d-125">格式 化</span><span class="sxs-lookup"><span data-stu-id="cf96d-125">Formatted</span></span>](formatted.md) | <span data-ttu-id="cf96d-126">N</span><span class="sxs-lookup"><span data-stu-id="cf96d-126">N</span></span>   | <span data-ttu-id="cf96d-127">Y</span><span class="sxs-lookup"><span data-stu-id="cf96d-127">Y</span></span>        |
| <span data-ttu-id="cf96d-128">引數</span><span class="sxs-lookup"><span data-stu-id="cf96d-128">Argument</span></span>    | [<span data-ttu-id="cf96d-129">格式 化</span><span class="sxs-lookup"><span data-stu-id="cf96d-129">Formatted</span></span>](formatted.md) | <span data-ttu-id="cf96d-130">N</span><span class="sxs-lookup"><span data-stu-id="cf96d-130">N</span></span>   | <span data-ttu-id="cf96d-131">Y</span><span class="sxs-lookup"><span data-stu-id="cf96d-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="cf96d-132">資料行</span><span class="sxs-lookup"><span data-stu-id="cf96d-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="cf96d-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>擴展\_</span><span class="sxs-lookup"><span data-stu-id="cf96d-133"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="cf96d-134">與資料表資料列相關聯的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="cf96d-134">The extension associated with the table row.</span></span> <span data-ttu-id="cf96d-135">此資料行是 [延伸模組資料表](extension-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cf96d-135">This column is an external key to the first column of the [Extension table](extension-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf96d-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>動詞</span><span class="sxs-lookup"><span data-stu-id="cf96d-136"><span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verb</span></span>
</dt> <dd>

<span data-ttu-id="cf96d-137">命令的動詞。</span><span class="sxs-lookup"><span data-stu-id="cf96d-137">The verb for the command.</span></span>

</dd> <dt>

<span data-ttu-id="cf96d-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列</span><span class="sxs-lookup"><span data-stu-id="cf96d-138"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="cf96d-139">命令的順序。</span><span class="sxs-lookup"><span data-stu-id="cf96d-139">The sequence of the commands.</span></span> <span data-ttu-id="cf96d-140">只有順序資料行為非 Null 的動詞，才能用來準備 shell 索引鍵的預設值的排序清單。</span><span class="sxs-lookup"><span data-stu-id="cf96d-140">Only verbs for which the Sequence column is non-Null are used to prepare an ordered list for the default value of the shell key.</span></span> <span data-ttu-id="cf96d-141">此資料行中具有最低值的動詞會成為預設動詞。</span><span class="sxs-lookup"><span data-stu-id="cf96d-141">The Verb with the lowest value in this column becomes the default verb.</span></span>

</dd> <dt>

<span data-ttu-id="cf96d-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>命令</span><span class="sxs-lookup"><span data-stu-id="cf96d-142"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="cf96d-143">顯示在內容功能表上的可當地語系化文字。</span><span class="sxs-lookup"><span data-stu-id="cf96d-143">The localizable text displayed on the context menu.</span></span>

</dd> <dt>

<span data-ttu-id="cf96d-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數</span><span class="sxs-lookup"><span data-stu-id="cf96d-144"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="cf96d-145">命令引數的值。</span><span class="sxs-lookup"><span data-stu-id="cf96d-145">Value for the command arguments.</span></span>

<span data-ttu-id="cf96d-146">請注意，[引數] 欄位中的屬性解析有限。</span><span class="sxs-lookup"><span data-stu-id="cf96d-146">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="cf96d-147">\[  \] 只有在已安裝擁有動詞的元件時，如果屬性已經有預期的值，就可以解析此欄位中格式化為屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf96d-147">A property formatted as \[*Property*\] in this field can only be resolved if the property already has the intended value when the component owning the verb is installed.</span></span> <span data-ttu-id="cf96d-148">例如，若要將引數 " \[ \#MyDoc.doc\] " 解析為正確的值，則相同的進程必須安裝 MyDoc.doc 以及擁有該動詞命令的元件。</span><span class="sxs-lookup"><span data-stu-id="cf96d-148">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf96d-149">備註</span><span class="sxs-lookup"><span data-stu-id="cf96d-149">Remarks</span></span>

<span data-ttu-id="cf96d-150">當執行 [RegisterExtensionInfo 動作](registerextensioninfo-action.md) 或 [UnregisterExtensionInfo 動作](unregisterextensioninfo-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="cf96d-150">This table is referred to when the [RegisterExtensionInfo action](registerextensioninfo-action.md) or the [UnregisterExtensionInfo action](unregisterextensioninfo-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="cf96d-151">驗證</span><span class="sxs-lookup"><span data-stu-id="cf96d-151">Validation</span></span>

<dl>

[<span data-ttu-id="cf96d-152">ICE03</span><span class="sxs-lookup"><span data-stu-id="cf96d-152">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="cf96d-153">ICE06</span><span class="sxs-lookup"><span data-stu-id="cf96d-153">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="cf96d-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="cf96d-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="cf96d-155">ICE46</span><span class="sxs-lookup"><span data-stu-id="cf96d-155">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="cf96d-156">ICE69</span><span class="sxs-lookup"><span data-stu-id="cf96d-156">ICE69</span></span>](ice69.md)  
</dl>

 

 



