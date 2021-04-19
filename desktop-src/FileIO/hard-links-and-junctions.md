---
description: 描述永久連結和接合。
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: 永久連結和接合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987359"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="803d9-103">永久連結和接合</span><span class="sxs-lookup"><span data-stu-id="803d9-103">Hard Links and Junctions</span></span>

<span data-ttu-id="803d9-104">NTFS 檔案系統支援三種類型的檔案連結：永久連結、接合和符號連結。</span><span class="sxs-lookup"><span data-stu-id="803d9-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="803d9-105">本主題概述永久連結和連接。</span><span class="sxs-lookup"><span data-stu-id="803d9-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="803d9-106">如需符號連結的詳細資訊，請參閱 [建立符號連結](creating-symbolic-links.md)。</span><span class="sxs-lookup"><span data-stu-id="803d9-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="803d9-107">永久連結</span><span class="sxs-lookup"><span data-stu-id="803d9-107">Hard Links</span></span>

<span data-ttu-id="803d9-108">*硬式連結* 是檔案的檔案系統表示，其中有一個以上的路徑參考相同磁片區中的單一檔案。</span><span class="sxs-lookup"><span data-stu-id="803d9-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="803d9-109">若要建立硬式連結，請使用 [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) 函數。</span><span class="sxs-lookup"><span data-stu-id="803d9-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="803d9-110">對該檔案所做的任何變更都會立即顯示給應用程式，透過參考該檔案的永久連結來存取該檔案。</span><span class="sxs-lookup"><span data-stu-id="803d9-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="803d9-111">不過，目錄專案大小和屬性資訊只會針對進行變更的連結進行更新。</span><span class="sxs-lookup"><span data-stu-id="803d9-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="803d9-112">請注意，檔案上的屬性會反映到該檔案的每個永久連結，而該檔案的屬性變更會傳播到所有的永久連結。</span><span class="sxs-lookup"><span data-stu-id="803d9-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="803d9-113">例如，如果您重設永久連結上的 READONLY 屬性以刪除該特定的永久連結，且實際檔案有多個永久連結，則您需要從其中一個剩餘的永久連結重設檔案的 READONLY 位，以將檔案和所有剩餘的永久連結回復至唯讀狀態。</span><span class="sxs-lookup"><span data-stu-id="803d9-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="803d9-114">例如，在 C：和 D：是本機磁片磁碟機的系統中，而 Z：是對應到 fred 共用的網路磁碟機機 \\ \\ \\ ，則會允許下列參考作為硬連結：</span><span class="sxs-lookup"><span data-stu-id="803d9-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="803d9-115">C： \\ dira \\ethel.txt 連結到 c： \\ dirb \\ dirc \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="803d9-116">D： \\ dir1 \\tinker.txt 至 d： \\ dir2 \\ dirx \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="803d9-117">C： \\ diry \\ bob .bak 連結到 C： \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="803d9-118">以下不是：</span><span class="sxs-lookup"><span data-stu-id="803d9-118">The following are not:</span></span>

-   <span data-ttu-id="803d9-119">C： \\ dira 連結到 c： \\ dirb</span><span class="sxs-lookup"><span data-stu-id="803d9-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="803d9-120">C： \\ dira \\ethel.txt 連結至 D： \\ dirb \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="803d9-121">C： \\ dira \\ethel.txt 連結至 Z： \\ dirb \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="803d9-122">若要刪除永久連結，請使用 [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="803d9-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="803d9-123">您可以依任何順序刪除永久連結，而不考慮它們的建立順序。</span><span class="sxs-lookup"><span data-stu-id="803d9-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="803d9-124">接合</span><span class="sxs-lookup"><span data-stu-id="803d9-124">Junctions</span></span>

<span data-ttu-id="803d9-125">*連接* 點 (也稱為「*軟連結*」，) 與硬連結不同，因為它所參考的儲存物件是不同的目錄，而連接點可以連結位於同一部電腦上不同本機磁片區的目錄。</span><span class="sxs-lookup"><span data-stu-id="803d9-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="803d9-126">否則，聯接的運作方式與永久連結相同。</span><span class="sxs-lookup"><span data-stu-id="803d9-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="803d9-127">連接會透過重新 [分析點](reparse-points.md)來執行。</span><span class="sxs-lookup"><span data-stu-id="803d9-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="803d9-128">假設 [永久連結] 區段中的相同條件，則會允許下列參考做為連接：</span><span class="sxs-lookup"><span data-stu-id="803d9-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="803d9-129">C： \\ dira 連結到 c： \\ dirb \\ dirc</span><span class="sxs-lookup"><span data-stu-id="803d9-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="803d9-130">C： \\ dirx 連結至 D： \\ diry</span><span class="sxs-lookup"><span data-stu-id="803d9-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="803d9-131">以下不是：</span><span class="sxs-lookup"><span data-stu-id="803d9-131">The following are not:</span></span>

-   <span data-ttu-id="803d9-132">C： \\ dira \\one.txt 連結到 c： \\ dirb \\two.txt</span><span class="sxs-lookup"><span data-stu-id="803d9-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="803d9-133">C： \\ dir1 連結至 Z： \\ dir2</span><span class="sxs-lookup"><span data-stu-id="803d9-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="803d9-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="803d9-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="803d9-135">建立符號連結</span><span class="sxs-lookup"><span data-stu-id="803d9-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



