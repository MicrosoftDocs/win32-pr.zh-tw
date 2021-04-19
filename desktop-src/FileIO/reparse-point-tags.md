---
description: 每個重新分析點都有一個識別碼標記，如此您就可以有效率地區分不同類型的重新分析點，而不需要檢查重新分析點中的使用者定義資料。
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: 重新分析點標記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985022"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="d813a-103">重新分析點標記</span><span class="sxs-lookup"><span data-stu-id="d813a-103">Reparse Point Tags</span></span>

<span data-ttu-id="d813a-104">每個重新分析點都有一個識別碼標記，如此您就可以有效率地區分不同類型的重新分析點，而不需要檢查重新分析點中的使用者定義資料。</span><span class="sxs-lookup"><span data-stu-id="d813a-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="d813a-105">系統會使用一組預先定義的標記，以及保留給 Microsoft 的標記範圍。</span><span class="sxs-lookup"><span data-stu-id="d813a-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="d813a-106">如果您在設定重新分析點時使用任何保留的標記，則作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="d813a-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="d813a-107">未包含在這些範圍中的標記不會保留，而且可供您的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="d813a-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="d813a-108">當您設定重新分析點時，您必須標記要放置在重新分析點中的資料。</span><span class="sxs-lookup"><span data-stu-id="d813a-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="d813a-109">建立重新分析點之後，如果新資料的標記不符合現有資料的標記，新的設定作業就會失敗。</span><span class="sxs-lookup"><span data-stu-id="d813a-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="d813a-110">如果標記相符，則設定作業會覆寫現有的重新分析點。</span><span class="sxs-lookup"><span data-stu-id="d813a-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="d813a-111">若要取出重新分析點標記，請使用 [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) 函數。</span><span class="sxs-lookup"><span data-stu-id="d813a-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="d813a-112">如果 **dwFileAttributes** 成員包含 **檔案屬性重新 \_ \_ 分析 \_ 點** 屬性，則 **dwReserved0** 成員會指定重新分析點。</span><span class="sxs-lookup"><span data-stu-id="d813a-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="d813a-113">標記內容</span><span class="sxs-lookup"><span data-stu-id="d813a-113">Tag Contents</span></span>

<span data-ttu-id="d813a-114">重新分析標記會儲存為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="d813a-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="d813a-115">Bits 會定義某些屬性，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="d813a-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="d813a-116">低16位會決定重新分析點的種類。</span><span class="sxs-lookup"><span data-stu-id="d813a-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="d813a-117">高16位具有保留給未來使用的12個位，以及代表標記的特定屬性和重新分析點所代表之資料的4個位。</span><span class="sxs-lookup"><span data-stu-id="d813a-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="d813a-118">下表描述這些位。</span><span class="sxs-lookup"><span data-stu-id="d813a-118">The following table describes these bits.</span></span>



| <span data-ttu-id="d813a-119">bit</span><span class="sxs-lookup"><span data-stu-id="d813a-119">Bit</span></span> | <span data-ttu-id="d813a-120">Description</span><span class="sxs-lookup"><span data-stu-id="d813a-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d813a-121">M</span><span class="sxs-lookup"><span data-stu-id="d813a-121">M</span></span>   | <span data-ttu-id="d813a-122">Microsoft 位。</span><span class="sxs-lookup"><span data-stu-id="d813a-122">Microsoft bit.</span></span> <span data-ttu-id="d813a-123">如果設定此位，則標記是由 Microsoft 所擁有。</span><span class="sxs-lookup"><span data-stu-id="d813a-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="d813a-124">所有其他標記都必須使用零來表示此位。</span><span class="sxs-lookup"><span data-stu-id="d813a-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="d813a-125">R</span><span class="sxs-lookup"><span data-stu-id="d813a-125">R</span></span>   | <span data-ttu-id="d813a-126">保護所有非 Microsoft 標記都必須是零。</span><span class="sxs-lookup"><span data-stu-id="d813a-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="d813a-127">N</span><span class="sxs-lookup"><span data-stu-id="d813a-127">N</span></span>   | <span data-ttu-id="d813a-128">名稱代理位。</span><span class="sxs-lookup"><span data-stu-id="d813a-128">Name surrogate bit.</span></span> <span data-ttu-id="d813a-129">如果設定此位，則檔案或目錄代表系統中的另一個命名實體。</span><span class="sxs-lookup"><span data-stu-id="d813a-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="d813a-130">下列宏有助測試標記：</span><span class="sxs-lookup"><span data-stu-id="d813a-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="d813a-131">**IsReparseTagMicrosoft**</span><span class="sxs-lookup"><span data-stu-id="d813a-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="d813a-132">**IsReparseTagNameSurrogate**</span><span class="sxs-lookup"><span data-stu-id="d813a-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="d813a-133">如果已設定相關聯的位，每個宏都會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d813a-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="d813a-134">以下是 Microsoft 預先定義的重新分析標記值;它們定義于 WinNT 中：</span><span class="sxs-lookup"><span data-stu-id="d813a-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="d813a-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="d813a-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="d813a-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="d813a-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="d813a-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="d813a-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="d813a-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="d813a-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="d813a-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="d813a-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="d813a-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="d813a-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="d813a-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="d813a-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="d813a-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="d813a-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="d813a-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="d813a-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="d813a-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="d813a-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="d813a-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="d813a-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="d813a-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="d813a-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="d813a-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="d813a-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="d813a-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="d813a-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="d813a-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="d813a-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="d813a-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="d813a-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="d813a-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="d813a-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="d813a-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="d813a-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="d813a-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="d813a-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="d813a-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="d813a-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="d813a-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="d813a-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="d813a-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="d813a-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="d813a-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="d813a-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="d813a-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="d813a-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="d813a-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="d813a-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="d813a-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="d813a-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="d813a-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="d813a-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="d813a-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="d813a-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="d813a-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="d813a-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="d813a-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="d813a-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="d813a-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="d813a-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="d813a-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="d813a-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="d813a-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="d813a-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="d813a-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="d813a-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="d813a-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="d813a-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="d813a-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="d813a-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="d813a-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="d813a-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="d813a-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="d813a-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="d813a-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="d813a-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="d813a-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="d813a-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="d813a-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="d813a-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="d813a-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="d813a-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="d813a-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="d813a-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="d813a-178">為了確保標記的唯一性，Microsoft 提供了散發新標記的機制。</span><span class="sxs-lookup"><span data-stu-id="d813a-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="d813a-179">如需詳細資訊，請參閱可 [安裝的檔案系統 (IFS) 套件](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx)。</span><span class="sxs-lookup"><span data-stu-id="d813a-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



