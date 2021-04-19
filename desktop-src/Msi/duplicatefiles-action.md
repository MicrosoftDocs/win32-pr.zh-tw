---
description: DuplicateFiles 動作會複製 InstallFiles 動作所安裝的檔案。 重複的檔案可以複製到具有不同名稱的相同目錄，或複製到具有原始名稱的不同目錄。
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: DuplicateFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980321"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="1d67d-104">DuplicateFiles 動作</span><span class="sxs-lookup"><span data-stu-id="1d67d-104">DuplicateFiles Action</span></span>

<span data-ttu-id="1d67d-105">DuplicateFiles 動作會複製 [InstallFiles](installfiles-action.md) 動作所安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="1d67d-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="1d67d-106">重複的檔案可以複製到具有不同名稱的相同目錄，或複製到具有原始名稱的不同目錄。</span><span class="sxs-lookup"><span data-stu-id="1d67d-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1d67d-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="1d67d-107">Sequence Restrictions</span></span>

<span data-ttu-id="1d67d-108">DuplicateFiles 動作必須晚于 [InstallFiles 動作](installfiles-action.md)。</span><span class="sxs-lookup"><span data-stu-id="1d67d-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="1d67d-109">DuplicateFiles 動作也必須在 [PatchFiles 動作](patchfiles-action.md) 之後，以防止複製未修補的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="1d67d-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1d67d-110">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="1d67d-110">ActionData Messages</span></span>



| <span data-ttu-id="1d67d-111">欄位</span><span class="sxs-lookup"><span data-stu-id="1d67d-111">Field</span></span> | <span data-ttu-id="1d67d-112">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="1d67d-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="1d67d-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1d67d-113">\[1\]</span></span> | <span data-ttu-id="1d67d-114">重複檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d67d-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="1d67d-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="1d67d-115">\[6\]</span></span> | <span data-ttu-id="1d67d-116">重複檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="1d67d-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="1d67d-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="1d67d-117">\[9\]</span></span> | <span data-ttu-id="1d67d-118">保存重複檔案之目錄的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d67d-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1d67d-119">備註</span><span class="sxs-lookup"><span data-stu-id="1d67d-119">Remarks</span></span>

<span data-ttu-id="1d67d-120">只有當連結到該專案的元件是在本機安裝時，DuplicateFiles 動作才會處理 [DuplicateFile 資料表](duplicatefile-table.md) 專案。</span><span class="sxs-lookup"><span data-stu-id="1d67d-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="1d67d-121">如需詳細資訊，請參閱 [元件表格](component-table.md)。</span><span class="sxs-lookup"><span data-stu-id="1d67d-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="1d67d-122">DestFolder 欄位中的字串是屬性名稱，其值應解析為完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1d67d-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="1d67d-123">這個屬性可以是 [目錄](directory-table.md) 資料表中的任何目錄專案、任何預先定義的資料夾屬性 ([**CommonFilesFolder**](commonfilesfolder.md)（例如) ），或是 [AppSearch](appsearch-table.md) 資料表中任何專案所設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d67d-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="1d67d-124">如果 **DestFolder** 屬性未評估為有效的路徑，則 DuplicateFiles 動作不會對該專案執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="1d67d-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="1d67d-125">如果 DuplicateFile 資料表的 DestName 資料行中之目的地檔案的名稱保留空白，則目的地檔案名將會與原始檔案名稱相同。</span><span class="sxs-lookup"><span data-stu-id="1d67d-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="1d67d-126">DuplicateFiles 動作所安裝的檔案會在適當時由 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作移除。</span><span class="sxs-lookup"><span data-stu-id="1d67d-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



