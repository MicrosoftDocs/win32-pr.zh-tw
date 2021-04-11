---
description: MoveFiles 動作會在使用者的電腦上尋找現有的檔案，並將這些檔案移動或複製到新的位置。
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: MoveFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852748"
---
# <a name="movefiles-action"></a><span data-ttu-id="45324-103">MoveFiles 動作</span><span class="sxs-lookup"><span data-stu-id="45324-103">MoveFiles Action</span></span>

<span data-ttu-id="45324-104">MoveFiles 動作會在使用者的電腦上尋找現有的檔案，並將這些檔案移動或複製到新的位置。</span><span class="sxs-lookup"><span data-stu-id="45324-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="45324-105">如果已指定連結至專案的元件要安裝在本機或從來源執行，則 [MoveFiles] 動作會查詢 [MoveFile 資料表](movefile-table.md) ，並在該處移動指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="45324-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="45324-106">順序限制</span><span class="sxs-lookup"><span data-stu-id="45324-106">Sequence Restrictions</span></span>

<span data-ttu-id="45324-107">MoveFiles 動作必須在 [InstallValidate](installvalidate-action.md) 動作之後，以及在 [InstallFiles](installfiles-action.md) 動作之前。</span><span class="sxs-lookup"><span data-stu-id="45324-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="45324-108">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="45324-108">ActionData Messages</span></span>



| <span data-ttu-id="45324-109">欄位</span><span class="sxs-lookup"><span data-stu-id="45324-109">Field</span></span> | <span data-ttu-id="45324-110">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="45324-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="45324-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="45324-111">\[1\]</span></span> | <span data-ttu-id="45324-112">已移動之檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45324-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="45324-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="45324-113">\[6\]</span></span> | <span data-ttu-id="45324-114">已安裝檔案的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="45324-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="45324-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="45324-115">\[9\]</span></span> | <span data-ttu-id="45324-116">保存移動檔案之目錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="45324-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="45324-117">備註</span><span class="sxs-lookup"><span data-stu-id="45324-117">Remarks</span></span>

<span data-ttu-id="45324-118">MoveFiles 資料表包含名為 "options" 的資料行，以指定要移動或複製的來源檔案。</span><span class="sxs-lookup"><span data-stu-id="45324-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="45324-119">移動的原始程式檔會在複製到新位置之後刪除。</span><span class="sxs-lookup"><span data-stu-id="45324-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="45324-120">如需確切的語法，請參閱 [MoveFile 資料表](movefile-table.md)。</span><span class="sxs-lookup"><span data-stu-id="45324-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="45324-121">MoveFile 資料表的 SourceFolder 和 DestFolder 資料行是屬性名稱，其值應解析為完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45324-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="45324-122">這些屬性可以是 [目錄](directory-table.md) 資料表中的任何目錄專案、任何預先定義的資料夾屬性 ([**FavoritesFolder**](favoritesfolder.md)（例如) ），或是 [AppSearch](appsearch-table.md) 資料表中任何專案所設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="45324-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="45324-123">這些屬性可能包含特定檔案的完整路徑，包含檔案名。</span><span class="sxs-lookup"><span data-stu-id="45324-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="45324-124">例如，您可以撰寫 AppSearch 資料表來搜尋特定的檔案，並將屬性設定為該檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45324-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="45324-125">在此範例中，MoveFile 資料表中的 [未占] 資料行可以保留空白，表示 SourceFolder 屬性中的值包含完整檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="45324-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="45324-126">分號是轉換、來源和修補程式的清單分隔符號，不應該用於檔案名或路徑中。</span><span class="sxs-lookup"><span data-stu-id="45324-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="45324-127">MoveFiles 動作不會作用於 MoveFile 資料表中的專案，其中 SourceFolder 或 DestFolder 屬性不會評估為完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45324-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="45324-128">MoveFiles 動作會嘗試移動或複製來原始目錄中的所有檔案，而這些檔案符合 MoveFiles 資料表的 [失敗的資料行] 中所指定的名稱。</span><span class="sxs-lookup"><span data-stu-id="45324-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="45324-129">[未通過] 資料行中的名稱可以包含 \* 或？</span><span class="sxs-lookup"><span data-stu-id="45324-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="45324-130">允許移動或複製檔群組的萬用字元。</span><span class="sxs-lookup"><span data-stu-id="45324-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="45324-131">例如，[未使用的資料行] 可能包含 " \* .xls" 的專案，而 MoveFiles 動作則會將每個 Microsoft Excel 活頁簿從來原始目錄移動或複製到目的地。</span><span class="sxs-lookup"><span data-stu-id="45324-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="45324-132">您可以在 MoveFile 資料表的 DestName 資料行中，指定要提供給目的地檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="45324-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="45324-133">如果此資料行保留空白，目的地檔案名會保留原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="45324-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="45324-134">如果在 \* [MoveFile 資料表](movefile-table.md) 的 [未使用] 資料行中輸入 "" 萬用字元，並在 DestName 資料行中指定目的地檔案名，則所有移動或複製的檔案都會保留來源中的名稱。</span><span class="sxs-lookup"><span data-stu-id="45324-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="45324-135">卸載產品時，不會刪除 MoveFiles 動作所移動或複製的檔案。</span><span class="sxs-lookup"><span data-stu-id="45324-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



