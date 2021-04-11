---
description: Master file 資料表 (MFT) 儲存從 NTFS 磁碟分割取出檔案所需的資訊。
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: '主要檔案資料表 (開發人員注意事項) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936075"
---
# <a name="master-file-table"></a><span data-ttu-id="5a2c7-103">主檔案資料表</span><span class="sxs-lookup"><span data-stu-id="5a2c7-103">Master File Table</span></span>

<span data-ttu-id="5a2c7-104">\[本檔僅適用于 NTFS 磁片區的第3版。\]</span><span class="sxs-lookup"><span data-stu-id="5a2c7-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="5a2c7-105">Master file 資料表 (MFT) 儲存從 NTFS 磁碟分割取出檔案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="5a2c7-106">檔案可以有一或多個 MFT 記錄，而且可以包含一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="5a2c7-107">在 NTFS 中，檔案參考是基底檔案記錄的 MFT 區段參考。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="5a2c7-108">如需詳細資訊，請參閱 [**MFT \_ 區段 \_ 參考**](mft-segment-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="5a2c7-109">此 MFT 包含檔案記錄區段;上述的前16個會保留給特殊檔案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="5a2c7-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="5a2c7-110">0： MFT ($Mft) </span><span class="sxs-lookup"><span data-stu-id="5a2c7-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="5a2c7-111">5：根目錄 (\\) </span><span class="sxs-lookup"><span data-stu-id="5a2c7-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="5a2c7-112">6：磁片區叢集設定檔 ($Bitmap) </span><span class="sxs-lookup"><span data-stu-id="5a2c7-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="5a2c7-113">8：叢集檔案 ($BadClus 不正確) </span><span class="sxs-lookup"><span data-stu-id="5a2c7-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="5a2c7-114">每個檔案記錄區段的開頭都是檔案記錄區段標頭。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="5a2c7-115">如需詳細資訊，請參閱檔案 [**\_ 記錄 \_ 區段 \_ 標頭**](file-record-segment-header.md)。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="5a2c7-116">每個檔案記錄區段後面都有一或多個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="5a2c7-117">每個屬性的開頭都是屬性記錄標頭。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="5a2c7-118">如需詳細資訊，請參閱 [**屬性 \_ 記錄 \_ 標頭**](attribute-record-header.md)。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="5a2c7-119">屬性記錄包含屬性類型 (例如 $DATA 或 $BITMAP) 、選擇性名稱和屬性值。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="5a2c7-120">「使用者資料流程」（attribute）是一種屬性，也就是所有的資料流程。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="5a2c7-121">屬性清單會以 0xFFFFFFFF ($END) 終止。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="5a2c7-122">以下是一些範例屬性。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="5a2c7-123">$Mft 檔案包含未命名的 $DATA 屬性，也就是依序排列的 MFT 記錄區段順序。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="5a2c7-124">$Mft 檔案包含未命名的 $BITMAP 屬性，指出正在使用的 MFT 記錄。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="5a2c7-125">$Bitmap 檔案包含未命名的 $DATA 屬性，指出使用中的叢集。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="5a2c7-126">$BadClus 檔案包含名為 $BAD 的 $DATA 屬性，其中包含對應至每個錯誤叢集的專案。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="5a2c7-127">當檔案記錄區段中沒有空間可供儲存屬性時，會配置額外的檔案記錄區段，並將其插入至第一個 (或基底) 檔案記錄區段（位於稱為屬性清單的屬性中）。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="5a2c7-128">[屬性] 清單指出可以找到與檔案相關聯的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="5a2c7-129">這包括基底檔案記錄中的所有屬性（attribute 清單本身除外）。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="5a2c7-130">如需詳細資訊，請參閱 [**屬性 \_ 清單 \_ 專案**](attribute-list-entry.md)。</span><span class="sxs-lookup"><span data-stu-id="5a2c7-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="5a2c7-131">與此 MFT 相關的結構包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5a2c7-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="5a2c7-132">**屬性 \_ 清單 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="5a2c7-133">**屬性 \_ 記錄 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="5a2c7-134">**檔案名 \_**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="5a2c7-135">**檔案 \_ 記錄 \_ 區段 \_ 標題**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="5a2c7-136">**MFT \_ 區段 \_ 參考**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="5a2c7-137">**多 \_ 磁區 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="5a2c7-138">**標準 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="5a2c7-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="5a2c7-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="5a2c7-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5a2c7-140">[NTFS 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5a2c7-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
