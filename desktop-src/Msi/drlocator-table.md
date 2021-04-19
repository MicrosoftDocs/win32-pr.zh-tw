---
description: DrLocator 資料表會透過搜尋目錄樹狀結構，來保存尋找檔案或目錄所需的資訊。
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: DrLocator 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967170"
---
# <a name="drlocator-table"></a><span data-ttu-id="b8da4-103">DrLocator 資料表</span><span class="sxs-lookup"><span data-stu-id="b8da4-103">DrLocator Table</span></span>

<span data-ttu-id="b8da4-104">DrLocator 資料表會透過搜尋目錄樹狀結構，來保存尋找檔案或目錄所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="b8da4-104">The DrLocator table holds the information needed to find a file or directory by searching the directory tree.</span></span>

<span data-ttu-id="b8da4-105">DrLocator 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="b8da4-105">The DrLocator table has the following columns.</span></span>



| <span data-ttu-id="b8da4-106">Column</span><span class="sxs-lookup"><span data-stu-id="b8da4-106">Column</span></span>      | <span data-ttu-id="b8da4-107">類型</span><span class="sxs-lookup"><span data-stu-id="b8da4-107">Type</span></span>                         | <span data-ttu-id="b8da4-108">答案</span><span class="sxs-lookup"><span data-stu-id="b8da4-108">Key</span></span> | <span data-ttu-id="b8da4-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="b8da4-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="b8da4-110">簽名\_</span><span class="sxs-lookup"><span data-stu-id="b8da4-110">Signature\_</span></span> | [<span data-ttu-id="b8da4-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="b8da4-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="b8da4-112">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-112">Y</span></span>   | <span data-ttu-id="b8da4-113">N</span><span class="sxs-lookup"><span data-stu-id="b8da4-113">N</span></span>        |
| <span data-ttu-id="b8da4-114">父代</span><span class="sxs-lookup"><span data-stu-id="b8da4-114">Parent</span></span>      | [<span data-ttu-id="b8da4-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="b8da4-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="b8da4-116">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-116">Y</span></span>   | <span data-ttu-id="b8da4-117">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-117">Y</span></span>        |
| <span data-ttu-id="b8da4-118">路徑</span><span class="sxs-lookup"><span data-stu-id="b8da4-118">Path</span></span>        | [<span data-ttu-id="b8da4-119">AnyPath</span><span class="sxs-lookup"><span data-stu-id="b8da4-119">AnyPath</span></span>](anypath.md)       | <span data-ttu-id="b8da4-120">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-120">Y</span></span>   | <span data-ttu-id="b8da4-121">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-121">Y</span></span>        |
| <span data-ttu-id="b8da4-122">深度</span><span class="sxs-lookup"><span data-stu-id="b8da4-122">Depth</span></span>       | [<span data-ttu-id="b8da4-123">整數</span><span class="sxs-lookup"><span data-stu-id="b8da4-123">Integer</span></span>](integer.md)       | <span data-ttu-id="b8da4-124">N</span><span class="sxs-lookup"><span data-stu-id="b8da4-124">N</span></span>   | <span data-ttu-id="b8da4-125">Y</span><span class="sxs-lookup"><span data-stu-id="b8da4-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b8da4-126">資料行</span><span class="sxs-lookup"><span data-stu-id="b8da4-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b8da4-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_</span><span class="sxs-lookup"><span data-stu-id="b8da4-127"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-128">簽章資料 \_ 行是簽章 [資料表](signature-table.md)第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="b8da4-128">The Signature\_ column is an external key to the first column of the [Signature table](signature-table.md).</span></span> <span data-ttu-id="b8da4-129">此欄位可能代表簽章資料表中所列的唯一檔案簽章。</span><span class="sxs-lookup"><span data-stu-id="b8da4-129">This field may represent a unique file signature listed in the Signature table.</span></span> <span data-ttu-id="b8da4-130">如果此資料行中的值不存在於簽章資料表中，則會假設搜尋是針對 DrLocator 資料表所指向的目錄。</span><span class="sxs-lookup"><span data-stu-id="b8da4-130">If the value in this column is absent from the Signature table, then the search is assumed to be for a directory pointed to by the DrLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="b8da4-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>父母</span><span class="sxs-lookup"><span data-stu-id="b8da4-131"><span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Parent</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-132">此資料行是簽章資料行中檔案或目錄之父目錄的簽章 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b8da4-132">This column is the signature of the parent directory of the file or directory in the Signature\_ column.</span></span> <span data-ttu-id="b8da4-133">如果此欄位為 null，而且 [路徑] 資料行沒有展開至完整路徑，則會使用路徑來搜尋使用者系統的所有固定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b8da4-133">If this field is null, and the Path column does not expand to a full path, then all the fixed drives of the user's system are searched by using the Path.</span></span>

<span data-ttu-id="b8da4-134">此欄位是下列其中一個資料表的索引鍵： [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)或 DrLocator 資料表。</span><span class="sxs-lookup"><span data-stu-id="b8da4-134">This field is a key into one of the following tables: the [RegLocator](reglocator-table.md), the [IniLocator](inilocator-table.md), the [CompLocator](complocator-table.md), or the DrLocator tables.</span></span>

</dd> <dt>

<span data-ttu-id="b8da4-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>路徑</span><span class="sxs-lookup"><span data-stu-id="b8da4-135"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-136">[路徑] 資料行包含使用者系統上的路徑。</span><span class="sxs-lookup"><span data-stu-id="b8da4-136">The Path column contains the path on the user's system.</span></span> <span data-ttu-id="b8da4-137">這是在父資料行中指定的目錄下方的完整路徑或相對子路徑。</span><span class="sxs-lookup"><span data-stu-id="b8da4-137">This is a either a full path or a relative subpath below the directory specified in the Parent column.</span></span> <span data-ttu-id="b8da4-138">請參閱 [AnyPath](anypath.md) 資料類型的限制。</span><span class="sxs-lookup"><span data-stu-id="b8da4-138">See the restrictions on the [AnyPath](anypath.md) data type.</span></span>

</dd> <dt>

<span data-ttu-id="b8da4-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>深度</span><span class="sxs-lookup"><span data-stu-id="b8da4-139"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Depth</span></span>
</dt> <dd>

<span data-ttu-id="b8da4-140">在安裝程式搜尋簽章資料行中所指定之檔案或目錄的路徑下方的深度 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b8da4-140">The depth below the path that the installer searches for the file or directory specified in the Signature\_ column.</span></span> <span data-ttu-id="b8da4-141">[深度] 欄位中所使用的值是以零為基礎。</span><span class="sxs-lookup"><span data-stu-id="b8da4-141">The value used in the Depth field is based on zero.</span></span> <span data-ttu-id="b8da4-142">例如，如果 [路徑] 欄位是 [c：/Program Files/bin]，則 [深度] 欄必須設定為0或更大，才能偵測位於資料夾 bin 內的檔案。</span><span class="sxs-lookup"><span data-stu-id="b8da4-142">For example, if the Path field is c:/Program Files/bin, the Depth column must be set to 0 or greater, to detect a file located inside the folder bin.</span></span> <span data-ttu-id="b8da4-143">如果 [深度] 欄位是空的，則會假設深度為零。</span><span class="sxs-lookup"><span data-stu-id="b8da4-143">If the Depth field is empty, the depth is assumed to be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8da4-144">備註</span><span class="sxs-lookup"><span data-stu-id="b8da4-144">Remarks</span></span>

<span data-ttu-id="b8da4-145">此資料表與 [AppSearch 資料表](appsearch-table.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b8da4-145">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="b8da4-146">此資料表的資料行通常不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="b8da4-146">This table's columns are generally not localized.</span></span> <span data-ttu-id="b8da4-147">如果作者決定要搜尋多種語言的產品，則每種語言的表格中都必須包含個別的專案。</span><span class="sxs-lookup"><span data-stu-id="b8da4-147">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="b8da4-148">請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。</span><span class="sxs-lookup"><span data-stu-id="b8da4-148">See [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="b8da4-149">驗證</span><span class="sxs-lookup"><span data-stu-id="b8da4-149">Validation</span></span>

<dl>

[<span data-ttu-id="b8da4-150">ICE03</span><span class="sxs-lookup"><span data-stu-id="b8da4-150">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b8da4-151">ICE06</span><span class="sxs-lookup"><span data-stu-id="b8da4-151">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b8da4-152">ICE46</span><span class="sxs-lookup"><span data-stu-id="b8da4-152">ICE46</span></span>](ice46.md)  
</dl>

 

 



