---
description: PatchFiles 動作會查詢 Patch 資料表，以判斷要套用的修補程式。 PatchFiles 動作也會執行檔案的位元組並存修補。
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: PatchFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849338"
---
# <a name="patchfiles-action"></a><span data-ttu-id="3e443-104">PatchFiles 動作</span><span class="sxs-lookup"><span data-stu-id="3e443-104">PatchFiles Action</span></span>

<span data-ttu-id="3e443-105">PatchFiles 動作會查詢 [Patch 資料表](patch-table.md) ，以判斷要套用的修補程式。</span><span class="sxs-lookup"><span data-stu-id="3e443-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="3e443-106">PatchFiles 動作也會執行檔案的位元組並存修補。</span><span class="sxs-lookup"><span data-stu-id="3e443-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3e443-107">順序限制</span><span class="sxs-lookup"><span data-stu-id="3e443-107">Sequence Restrictions</span></span>

<span data-ttu-id="3e443-108">如果未安裝要修補的檔案，則 PatchFiles 動作必須在安裝檔案的 [InstallFiles 動作](installfiles-action.md) 之後。</span><span class="sxs-lookup"><span data-stu-id="3e443-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="3e443-109">先前安裝的檔案可能會在動作順序中的任何時間點進行修補。</span><span class="sxs-lookup"><span data-stu-id="3e443-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="3e443-110">[DuplicateFiles 動作](duplicatefiles-action.md)必須位於 PatchFiles 動作之後，以防止複製未修補的檔案版本。</span><span class="sxs-lookup"><span data-stu-id="3e443-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3e443-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="3e443-111">ActionData Messages</span></span>



| <span data-ttu-id="3e443-112">欄位</span><span class="sxs-lookup"><span data-stu-id="3e443-112">Field</span></span> | <span data-ttu-id="3e443-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="3e443-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="3e443-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3e443-114">\[1\]</span></span> | <span data-ttu-id="3e443-115">已修補之檔案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e443-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="3e443-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="3e443-116">\[2\]</span></span> | <span data-ttu-id="3e443-117">保存修補過之檔案的目錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e443-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="3e443-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="3e443-118">\[3\]</span></span> | <span data-ttu-id="3e443-119">修補程式的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3e443-119">Size of patch in bytes.</span></span>                       |



 

 

 



