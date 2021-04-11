---
description: 此資料表包含要從指定的來原始目錄移動或複製到指定之目的地目錄的檔案清單。
ms.assetid: 9ba47bdc-90c8-444a-ba8b-71c723b54556
title: MoveFile 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2340626e745627c3c6146998c851a076d21ab81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695419"
---
# <a name="movefile-table"></a><span data-ttu-id="144ff-103">MoveFile 資料表</span><span class="sxs-lookup"><span data-stu-id="144ff-103">MoveFile Table</span></span>

<span data-ttu-id="144ff-104">此資料表包含要從指定的來原始目錄移動或複製到指定之目的地目錄的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="144ff-104">This table contains a list of files to be moved or copied from a specified source directory to a specified destination directory.</span></span>

<span data-ttu-id="144ff-105">MoveFile 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="144ff-105">The MoveFile table has the following columns.</span></span>



| <span data-ttu-id="144ff-106">Column</span><span class="sxs-lookup"><span data-stu-id="144ff-106">Column</span></span>       | <span data-ttu-id="144ff-107">類型</span><span class="sxs-lookup"><span data-stu-id="144ff-107">Type</span></span>                         | <span data-ttu-id="144ff-108">答案</span><span class="sxs-lookup"><span data-stu-id="144ff-108">Key</span></span> | <span data-ttu-id="144ff-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="144ff-109">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="144ff-110">FileKey</span><span class="sxs-lookup"><span data-stu-id="144ff-110">FileKey</span></span>      | [<span data-ttu-id="144ff-111">識別碼</span><span class="sxs-lookup"><span data-stu-id="144ff-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="144ff-112">Y</span><span class="sxs-lookup"><span data-stu-id="144ff-112">Y</span></span>   | <span data-ttu-id="144ff-113">N</span><span class="sxs-lookup"><span data-stu-id="144ff-113">N</span></span>        |
| <span data-ttu-id="144ff-114">元件\_</span><span class="sxs-lookup"><span data-stu-id="144ff-114">Component\_</span></span>  | [<span data-ttu-id="144ff-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="144ff-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="144ff-116">N</span><span class="sxs-lookup"><span data-stu-id="144ff-116">N</span></span>   | <span data-ttu-id="144ff-117">N</span><span class="sxs-lookup"><span data-stu-id="144ff-117">N</span></span>        |
| <span data-ttu-id="144ff-118">SourceName</span><span class="sxs-lookup"><span data-stu-id="144ff-118">SourceName</span></span>   | [<span data-ttu-id="144ff-119">Text</span><span class="sxs-lookup"><span data-stu-id="144ff-119">Text</span></span>](text.md)             | <span data-ttu-id="144ff-120">N</span><span class="sxs-lookup"><span data-stu-id="144ff-120">N</span></span>   | <span data-ttu-id="144ff-121">Y</span><span class="sxs-lookup"><span data-stu-id="144ff-121">Y</span></span>        |
| <span data-ttu-id="144ff-122">DestName</span><span class="sxs-lookup"><span data-stu-id="144ff-122">DestName</span></span>     | [<span data-ttu-id="144ff-123">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="144ff-123">Filename</span></span>](filename.md)     | <span data-ttu-id="144ff-124">N</span><span class="sxs-lookup"><span data-stu-id="144ff-124">N</span></span>   | <span data-ttu-id="144ff-125">Y</span><span class="sxs-lookup"><span data-stu-id="144ff-125">Y</span></span>        |
| <span data-ttu-id="144ff-126">SourceFolder</span><span class="sxs-lookup"><span data-stu-id="144ff-126">SourceFolder</span></span> | [<span data-ttu-id="144ff-127">識別碼</span><span class="sxs-lookup"><span data-stu-id="144ff-127">Identifier</span></span>](identifier.md) | <span data-ttu-id="144ff-128">N</span><span class="sxs-lookup"><span data-stu-id="144ff-128">N</span></span>   | <span data-ttu-id="144ff-129">Y</span><span class="sxs-lookup"><span data-stu-id="144ff-129">Y</span></span>        |
| <span data-ttu-id="144ff-130">DestFolder</span><span class="sxs-lookup"><span data-stu-id="144ff-130">DestFolder</span></span>   | [<span data-ttu-id="144ff-131">識別碼</span><span class="sxs-lookup"><span data-stu-id="144ff-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="144ff-132">N</span><span class="sxs-lookup"><span data-stu-id="144ff-132">N</span></span>   | <span data-ttu-id="144ff-133">N</span><span class="sxs-lookup"><span data-stu-id="144ff-133">N</span></span>        |
| <span data-ttu-id="144ff-134">選項</span><span class="sxs-lookup"><span data-stu-id="144ff-134">Options</span></span>      | [<span data-ttu-id="144ff-135">整數</span><span class="sxs-lookup"><span data-stu-id="144ff-135">Integer</span></span>](integer.md)       | <span data-ttu-id="144ff-136">N</span><span class="sxs-lookup"><span data-stu-id="144ff-136">N</span></span>   | <span data-ttu-id="144ff-137">N</span><span class="sxs-lookup"><span data-stu-id="144ff-137">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="144ff-138">資料行</span><span class="sxs-lookup"><span data-stu-id="144ff-138">Columns</span></span>

<dl> <dt>

<span data-ttu-id="144ff-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span><span class="sxs-lookup"><span data-stu-id="144ff-139"><span id="FileKey"></span><span id="filekey"></span><span id="FILEKEY"></span>FileKey</span></span>
</dt> <dd>

<span data-ttu-id="144ff-140">可唯一識別特定 MoveFile 記錄的主鍵。</span><span class="sxs-lookup"><span data-stu-id="144ff-140">Primary key that uniquely identifies a particular MoveFile record.</span></span>

</dd> <dt>

<span data-ttu-id="144ff-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="144ff-141"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="144ff-142">[元件資料表](component-table.md)中的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="144ff-142">External key into the [Component table](component-table.md).</span></span> <span data-ttu-id="144ff-143">如果未選取此索引鍵所參考的元件來進行安裝或移除，則不會在此 MoveFile 專案上採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="144ff-143">If the component referenced by this key is not selected for installation or removal, then no action is taken on this MoveFile entry.</span></span>

</dd> <dt>

<span data-ttu-id="144ff-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span><span class="sxs-lookup"><span data-stu-id="144ff-144"><span id="SourceName"></span><span id="sourcename"></span><span id="SOURCENAME"></span>SourceName</span></span>
</dt> <dd>

<span data-ttu-id="144ff-145">此資料行包含要移動或複製之來源檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="144ff-145">This column contains the localizable name of the source files to be moved or copied.</span></span> <span data-ttu-id="144ff-146">此資料行可以保留空白。</span><span class="sxs-lookup"><span data-stu-id="144ff-146">This column may be left blank.</span></span> <span data-ttu-id="144ff-147">請參閱 SourceFolder 資料行的描述。</span><span class="sxs-lookup"><span data-stu-id="144ff-147">See the description of the SourceFolder column.</span></span> <span data-ttu-id="144ff-148">此欄位必須包含長檔名，而且可能包含萬用字元 (\* 和？ ) 。</span><span class="sxs-lookup"><span data-stu-id="144ff-148">This field must contain a long file name and may contain wildcard characters (\* and ?).</span></span>

</dd> <dt>

<span data-ttu-id="144ff-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span><span class="sxs-lookup"><span data-stu-id="144ff-149"><span id="DestName"></span><span id="destname"></span><span id="DESTNAME"></span>DestName</span></span>
</dt> <dd>

<span data-ttu-id="144ff-150">此資料行包含在移動或複製原始檔案之後，提供給原始檔案的可當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="144ff-150">This column contains the localizable name to be given to the original file after it is moved or copied.</span></span> <span data-ttu-id="144ff-151">如果這個欄位是空白的，則會將目的地檔案的名稱與來源檔案相同。</span><span class="sxs-lookup"><span data-stu-id="144ff-151">If this field is blank, then the destination file is given the same name as the source file.</span></span>

</dd> <dt>

<span data-ttu-id="144ff-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span><span class="sxs-lookup"><span data-stu-id="144ff-152"><span id="SourceFolder"></span><span id="sourcefolder"></span><span id="SOURCEFOLDER"></span>SourceFolder</span></span>
</dt> <dd>

<span data-ttu-id="144ff-153">此資料行包含屬性的名稱，這個屬性的值會解析為來原始目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="144ff-153">This column contains the name of a property having a value that resolves to the full path to the source directory.</span></span> <span data-ttu-id="144ff-154">如果 [不完整] 資料行保留空白，則會假設 SourceFolder 資料行中命名的屬性包含原始程式檔本身的完整路徑 (包括檔案名) 。</span><span class="sxs-lookup"><span data-stu-id="144ff-154">If the SourceName column is left blank, then the property named in the SourceFolder column is assumed to contain the full path to the source file itself (including the file name).</span></span>

</dd> <dt>

<span data-ttu-id="144ff-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span><span class="sxs-lookup"><span data-stu-id="144ff-155"><span id="DestFolder"></span><span id="destfolder"></span><span id="DESTFOLDER"></span>DestFolder</span></span>
</dt> <dd>

<span data-ttu-id="144ff-156">屬性的名稱，這個屬性的值會解析為目的地目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="144ff-156">The name of a property whose value resolves to the full path to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="144ff-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>選項</span><span class="sxs-lookup"><span data-stu-id="144ff-157"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="144ff-158">指定操作模式的整數值。</span><span class="sxs-lookup"><span data-stu-id="144ff-158">Integer value specifying the operating mode.</span></span>



| <span data-ttu-id="144ff-159">常數</span><span class="sxs-lookup"><span data-stu-id="144ff-159">Constant</span></span>                     | <span data-ttu-id="144ff-160">十六進位</span><span class="sxs-lookup"><span data-stu-id="144ff-160">Hexadecimal</span></span> | <span data-ttu-id="144ff-161">Decimal</span><span class="sxs-lookup"><span data-stu-id="144ff-161">Decimal</span></span> | <span data-ttu-id="144ff-162">意義</span><span class="sxs-lookup"><span data-stu-id="144ff-162">Meaning</span></span>               |
|------------------------------|-------------|---------|-----------------------|
| <span data-ttu-id="144ff-163">(無)</span><span class="sxs-lookup"><span data-stu-id="144ff-163">(none)</span></span>                       | <span data-ttu-id="144ff-164">0x000</span><span class="sxs-lookup"><span data-stu-id="144ff-164">0x000</span></span>       | <span data-ttu-id="144ff-165">0</span><span class="sxs-lookup"><span data-stu-id="144ff-165">0</span></span>       | <span data-ttu-id="144ff-166">複製來源檔案。</span><span class="sxs-lookup"><span data-stu-id="144ff-166">Copy the source file.</span></span> |
| <span data-ttu-id="144ff-167">**msidbMoveFileOptionsMove**</span><span class="sxs-lookup"><span data-stu-id="144ff-167">**msidbMoveFileOptionsMove**</span></span> | <span data-ttu-id="144ff-168">0x001</span><span class="sxs-lookup"><span data-stu-id="144ff-168">0x001</span></span>       | <span data-ttu-id="144ff-169">1</span><span class="sxs-lookup"><span data-stu-id="144ff-169">1</span></span>       | <span data-ttu-id="144ff-170">移動原始檔。</span><span class="sxs-lookup"><span data-stu-id="144ff-170">Move the source file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="144ff-171">備註</span><span class="sxs-lookup"><span data-stu-id="144ff-171">Remarks</span></span>

<span data-ttu-id="144ff-172">如果在 \* MoveFile 資料表的 [未使用] 資料行中輸入 "" 萬用字元，並在 DestName 資料行中指定目的地檔案名，則所有移動或複製的檔案都會保留來源中的名稱。</span><span class="sxs-lookup"><span data-stu-id="144ff-172">If a "\*" wildcard is entered in the SourceName column of the MoveFile table and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="144ff-173">此資料表是由 [MoveFiles 動作](movefiles-action.md)處理。</span><span class="sxs-lookup"><span data-stu-id="144ff-173">This table is processed by the [MoveFiles action](movefiles-action.md).</span></span>

## <a name="validation"></a><span data-ttu-id="144ff-174">驗證</span><span class="sxs-lookup"><span data-stu-id="144ff-174">Validation</span></span>

<dl>

[<span data-ttu-id="144ff-175">ICE03</span><span class="sxs-lookup"><span data-stu-id="144ff-175">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="144ff-176">ICE06</span><span class="sxs-lookup"><span data-stu-id="144ff-176">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="144ff-177">ICE18</span><span class="sxs-lookup"><span data-stu-id="144ff-177">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="144ff-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="144ff-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="144ff-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="144ff-179">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="144ff-180">ICE85</span><span class="sxs-lookup"><span data-stu-id="144ff-180">ICE85</span></span>](ice85.md)  
</dl>

 

 



