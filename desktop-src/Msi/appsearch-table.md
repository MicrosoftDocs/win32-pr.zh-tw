---
description: AppSearch 資料表包含搜尋具有特定檔案簽章的檔案時所需的屬性。 AppSearch 資料表也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: AppSearch 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192461"
---
# <a name="appsearch-table"></a><span data-ttu-id="9688f-104">AppSearch 資料表</span><span class="sxs-lookup"><span data-stu-id="9688f-104">AppSearch Table</span></span>

<span data-ttu-id="9688f-105">AppSearch 資料表包含搜尋具有特定檔案簽章的檔案時所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="9688f-105">The AppSearch table contains properties needed to search for a file having a particular file signature.</span></span> <span data-ttu-id="9688f-106">AppSearch 資料表也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。</span><span class="sxs-lookup"><span data-stu-id="9688f-106">The AppSearch table can also be used to set a property to the existing value of a registry or .ini file entry.</span></span>

<span data-ttu-id="9688f-107">AppSearch 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="9688f-107">The AppSearch table has the following columns.</span></span>



| <span data-ttu-id="9688f-108">Column</span><span class="sxs-lookup"><span data-stu-id="9688f-108">Column</span></span>      | <span data-ttu-id="9688f-109">類型</span><span class="sxs-lookup"><span data-stu-id="9688f-109">Type</span></span>                         | <span data-ttu-id="9688f-110">答案</span><span class="sxs-lookup"><span data-stu-id="9688f-110">Key</span></span> | <span data-ttu-id="9688f-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="9688f-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="9688f-112">屬性</span><span class="sxs-lookup"><span data-stu-id="9688f-112">Property</span></span>    | [<span data-ttu-id="9688f-113">識別碼</span><span class="sxs-lookup"><span data-stu-id="9688f-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="9688f-114">Y</span><span class="sxs-lookup"><span data-stu-id="9688f-114">Y</span></span>   | <span data-ttu-id="9688f-115">N</span><span class="sxs-lookup"><span data-stu-id="9688f-115">N</span></span>        |
| <span data-ttu-id="9688f-116">簽名\_</span><span class="sxs-lookup"><span data-stu-id="9688f-116">Signature\_</span></span> | [<span data-ttu-id="9688f-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="9688f-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="9688f-118">Y</span><span class="sxs-lookup"><span data-stu-id="9688f-118">Y</span></span>   | <span data-ttu-id="9688f-119">N</span><span class="sxs-lookup"><span data-stu-id="9688f-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9688f-120">資料行</span><span class="sxs-lookup"><span data-stu-id="9688f-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9688f-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產</span><span class="sxs-lookup"><span data-stu-id="9688f-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="9688f-122">執行 [AppSearch](appsearch-action.md) 動作時，會將這個屬性設定為簽章資料行所指出的檔案位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9688f-122">Running the [AppSearch](appsearch-action.md) action sets this property to the location of the file indicated by the Signature\_ column.</span></span> <span data-ttu-id="9688f-123">如果使用者的電腦上有檔案簽章，就會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9688f-123">This property is set if the file signature exists on the user's computer.</span></span> <span data-ttu-id="9688f-124">此資料行中使用的屬性必須是 [公用](public-properties.md) 屬性，而且具有不包含小寫字母的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9688f-124">The properties used in this column must be [public](public-properties.md) properties and have an identifier that contains no lowercase letters.</span></span>

<span data-ttu-id="9688f-125">[屬性] 欄位中所列的屬性，可以在 [屬性](property-table.md) 表中或從命令列初始化。</span><span class="sxs-lookup"><span data-stu-id="9688f-125">The property listed in the Property field may be initialized in the [Property](property-table.md) table or from a command line.</span></span> <span data-ttu-id="9688f-126">如果 [AppSearch](appsearch-action.md) 動作找出簽章，則安裝程式會使用找到的值來覆寫已初始化的屬性值。</span><span class="sxs-lookup"><span data-stu-id="9688f-126">If the [AppSearch](appsearch-action.md) action locates the signature, the installer overrides the initialized property value with the found value.</span></span> <span data-ttu-id="9688f-127">如果找不到簽章，則會使用初始屬性值。</span><span class="sxs-lookup"><span data-stu-id="9688f-127">If the signature is not found, then the initial property value is used.</span></span> <span data-ttu-id="9688f-128">如果屬性從未初始化，則只有在找到簽章時，才會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="9688f-128">If the property was never initialized, then the property will only be set if the signature is found.</span></span> <span data-ttu-id="9688f-129">否則，屬性會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="9688f-129">Otherwise, the property is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="9688f-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="9688f-130"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="9688f-131">簽章資料 \_ 行包含稱為簽章的唯一識別碼，而且也是 [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)和 [DrLocator](drlocator-table.md) 資料表中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9688f-131">The Signature\_ column contains a unique identifier called a signature and is also an external key into the [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md), and [DrLocator](drlocator-table.md) tables.</span></span> <span data-ttu-id="9688f-132">搜尋檔案時，這個資料行中的值也必須是簽 [章資料表中的外](signature-table.md) 鍵。</span><span class="sxs-lookup"><span data-stu-id="9688f-132">When searching for a file, the value in this column must also be a foreign key into the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="9688f-133">如果此資料行中的值未列在簽章資料表中，安裝程式會判斷搜尋是否為目錄。</span><span class="sxs-lookup"><span data-stu-id="9688f-133">If the value in this column is not listed in the Signature table, the installer determines that the search is for a directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9688f-134">備註</span><span class="sxs-lookup"><span data-stu-id="9688f-134">Remarks</span></span>

<span data-ttu-id="9688f-135">[*順序資料表*](s-gly.md)中的 [AppSearch](appsearch-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="9688f-135">The [AppSearch](appsearch-action.md) action in [*sequence tables*](s-gly.md) processes the information in this table.</span></span> <span data-ttu-id="9688f-136">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="9688f-136">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="9688f-137">[AppSearch](appsearch-action.md)動作會先使用[CompLocator](complocator-table.md)資料表、 [RegLocator](reglocator-table.md)資料表第二個、 [IniLocator](inilocator-table.md)資料表第三個，最後是[DrLocator](drlocator-table.md)資料表來搜尋簽章。</span><span class="sxs-lookup"><span data-stu-id="9688f-137">The [AppSearch](appsearch-action.md) action searches for signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table second, the [IniLocator](inilocator-table.md) table third, and finally the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="9688f-138">簽章會 [列在簽章資料表中](signature-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="9688f-138">File signatures are listed in the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="9688f-139">不在簽章資料表中的簽章代表目錄，而動作則會將屬性設定為該簽章的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="9688f-139">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="9688f-140">請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="9688f-140">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="9688f-141">驗證</span><span class="sxs-lookup"><span data-stu-id="9688f-141">Validation</span></span>

<dl>

[<span data-ttu-id="9688f-142">ICE03</span><span class="sxs-lookup"><span data-stu-id="9688f-142">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9688f-143">ICE06</span><span class="sxs-lookup"><span data-stu-id="9688f-143">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9688f-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="9688f-144">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9688f-145">ICE52</span><span class="sxs-lookup"><span data-stu-id="9688f-145">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="9688f-146">ICE88</span><span class="sxs-lookup"><span data-stu-id="9688f-146">ICE88</span></span>](ice88.md)  
</dl>

 

 



