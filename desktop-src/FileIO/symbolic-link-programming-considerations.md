---
description: 使用符號連結的程式設計考慮。
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: " (本機檔案系統的程式設計考慮) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "106981750"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="84154-103"> (本機檔案系統的程式設計考慮) </span><span class="sxs-lookup"><span data-stu-id="84154-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="84154-104">使用符號連結時，請記住下列程式設計考慮：</span><span class="sxs-lookup"><span data-stu-id="84154-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="84154-105">符號連結可以指向不存在的目標。</span><span class="sxs-lookup"><span data-stu-id="84154-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="84154-106">建立符號連結時，作業系統不會查看目標是否存在。</span><span class="sxs-lookup"><span data-stu-id="84154-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="84154-107">如果應用程式嘗試開啟不存在的目標，則會傳回 **錯誤 \_ \_ \_** 檔案。</span><span class="sxs-lookup"><span data-stu-id="84154-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="84154-108">符號連結是重新分析點。</span><span class="sxs-lookup"><span data-stu-id="84154-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="84154-109">如需詳細資訊，請參閱 [判斷目錄是否為裝載的資料夾](determining-whether-a-directory-is-a-volume-mount-point.md)。</span><span class="sxs-lookup"><span data-stu-id="84154-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="84154-110">最多可 (63 重新分析點，因此會) 特定路徑中允許的符號連結。</span><span class="sxs-lookup"><span data-stu-id="84154-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="84154-111">**Windows Server 2003 和 WINDOWS XP：** 在任何指定的路徑上，都有31個重新分析點的限制。</span><span class="sxs-lookup"><span data-stu-id="84154-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84154-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="84154-112">Related topics</span></span>

<dl> <span data-ttu-id="84154-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="84154-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="84154-114">永久連結和接合</span><span class="sxs-lookup"><span data-stu-id="84154-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



