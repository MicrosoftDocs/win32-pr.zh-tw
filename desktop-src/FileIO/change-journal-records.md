---
description: 新增、刪除和修改檔案、目錄和其他 NTFS 檔案系統物件時，NTFS 檔案系統會在資料流程中輸入變更日誌記錄，電腦上的每個磁片區都會有一個記錄。
ms.assetid: c41aa3a8-c8d8-4bf2-9bbb-d6a6a556c5e4
title: 變更日誌記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56580a28c01ca164af4598cb290a37c8e36828f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988408"
---
# <a name="change-journal-records"></a><span data-ttu-id="a212a-103">變更日誌記錄</span><span class="sxs-lookup"><span data-stu-id="a212a-103">Change Journal Records</span></span>

<span data-ttu-id="a212a-104">新增、刪除和修改檔案、目錄和其他 NTFS 檔案系統物件時，NTFS 檔案系統會在資料流程中輸入變更日誌記錄，電腦上的每個磁片區都會有一個記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-104">As files, directories, and other NTFS file system objects are added, deleted, and modified, the NTFS file system enters change journal records in streams, one for each volume on the computer.</span></span> <span data-ttu-id="a212a-105">每個記錄都會指出變更的類型與變更的物件。</span><span class="sxs-lookup"><span data-stu-id="a212a-105">Each record indicates the type of change and the object changed.</span></span> <span data-ttu-id="a212a-106">特定記錄之資料流程開頭的位移，稱為特定記錄 (USN) 的更新序號。</span><span class="sxs-lookup"><span data-stu-id="a212a-106">The offset from the beginning of the stream for a particular record is called the update sequence number (USN) for the particular record.</span></span> <span data-ttu-id="a212a-107">新記錄會附加到資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="a212a-107">New records are appended to the end of the stream.</span></span>

<span data-ttu-id="a212a-108">NTFS 檔案系統可能會刪除舊的記錄來節省空間。</span><span class="sxs-lookup"><span data-stu-id="a212a-108">The NTFS file system may delete old records to conserve space.</span></span> <span data-ttu-id="a212a-109">如果所需的記錄已刪除，則索引服務會藉由重新編制磁片區索引來復原，如同沒有變更日誌存在一樣。</span><span class="sxs-lookup"><span data-stu-id="a212a-109">If needed records have been deleted, the indexing service recovers by re-indexing the volume, as it does when no change journal exists.</span></span>

<span data-ttu-id="a212a-110">變更日誌只會記錄檔案變更的事實，以及變更的原因 (例如，寫入作業、截斷、延長、刪除等) 。</span><span class="sxs-lookup"><span data-stu-id="a212a-110">The change journal logs only the fact of a change to a file and the reason for the change (for example, write operations, truncation, lengthening, deletion, and so on).</span></span> <span data-ttu-id="a212a-111">它不會記錄足夠的資訊來允許反轉變更。</span><span class="sxs-lookup"><span data-stu-id="a212a-111">It does not record enough information to allow reversing the change.</span></span>

<span data-ttu-id="a212a-112">此外，相同檔案的多個變更可能只會將一個原因旗標新增至目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-112">In addition, multiple changes to the same file may result in only one reason flag being added to the current record.</span></span> <span data-ttu-id="a212a-113">如果相同類型的變更發生一次以上，NTFS 檔案系統就不會在第一次之後針對變更寫入新記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-113">If the same kind of change occurs more than once, the NTFS file system does not write a new record for the changes after the first.</span></span> <span data-ttu-id="a212a-114">例如，數個不含中間關閉和重新開啟作業的寫入作業，只會產生一個變更記錄，其中有原因旗標 USN \_ 原因 \_ 資料 \_ 覆寫設定。</span><span class="sxs-lookup"><span data-stu-id="a212a-114">For example, several write operations with no intervening close and reopen operations result in only one change record with the reason flag USN\_REASON\_DATA\_OVERWRITE set.</span></span>

<span data-ttu-id="a212a-115">為了說明變更日誌的運作方式，假設使用者以下列順序存取檔案：</span><span class="sxs-lookup"><span data-stu-id="a212a-115">To illustrate how the change journal works, suppose a user accesses a file in the following order:</span></span>

1.  <span data-ttu-id="a212a-116">寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="a212a-116">Writes to the file.</span></span>
2.  <span data-ttu-id="a212a-117">設定檔案的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="a212a-117">Sets the time stamp for the file.</span></span>
3.  <span data-ttu-id="a212a-118">寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="a212a-118">Writes to the file.</span></span>
4.  <span data-ttu-id="a212a-119">截斷檔案。</span><span class="sxs-lookup"><span data-stu-id="a212a-119">Truncates the file.</span></span>
5.  <span data-ttu-id="a212a-120">寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="a212a-120">Writes to the file.</span></span>
6.  <span data-ttu-id="a212a-121">關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="a212a-121">Closes the file.</span></span>

<span data-ttu-id="a212a-122">在此情況下，NTFS 檔案系統會在變更日誌中採取下列動作 (其中 \| 指出) 的位 or 運算。</span><span class="sxs-lookup"><span data-stu-id="a212a-122">In this case, the NTFS file system takes the following actions in the change journal (where \| indicates a bitwise OR operation).</span></span>



| <span data-ttu-id="a212a-123">事件</span><span class="sxs-lookup"><span data-stu-id="a212a-123">Event</span></span>                                 | <span data-ttu-id="a212a-124">NTFS 檔案系統動作</span><span class="sxs-lookup"><span data-stu-id="a212a-124">NTFS file system action</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a212a-125">初始寫入操作</span><span class="sxs-lookup"><span data-stu-id="a212a-125">Initial write operation</span></span><br/>    | <span data-ttu-id="a212a-126">NTFS 檔案系統會寫入新的 USN 記錄，並 \_ 設定 usn 原因的 \_ 資料 \_ 覆寫原因旗標。</span><span class="sxs-lookup"><span data-stu-id="a212a-126">The NTFS file system writes a new USN record with the USN\_REASON\_DATA\_OVERWRITE reason flag set.</span></span> <span data-ttu-id="a212a-127">如需可能原因旗標的詳細資訊，請參閱 [**USN \_ 記錄**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) 結構。</span><span class="sxs-lookup"><span data-stu-id="a212a-127">For more information on possible reason flags, see the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) structure.</span></span><br/>                                                     |
| <span data-ttu-id="a212a-128">檔案時間戳記的設定</span><span class="sxs-lookup"><span data-stu-id="a212a-128">Setting of file time stamp</span></span><br/> | <span data-ttu-id="a212a-129">NTFS 檔案系統會寫入新的 USN 記錄，其中包含旗標設定 USN \_ 原因 \_ 資料 \_ 覆寫 \| usn \_ 原因 \_ 基本 \_ 資訊 \_ 變更。</span><span class="sxs-lookup"><span data-stu-id="a212a-129">The NTFS file system writes a new USN record with the flag setting USN\_REASON\_DATA\_OVERWRITE \| USN\_REASON\_BASIC\_INFO\_CHANGE.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="a212a-130">第二個寫入操作</span><span class="sxs-lookup"><span data-stu-id="a212a-130">Second write operation</span></span><br/>     | <span data-ttu-id="a212a-131">NTFS 檔案系統不會寫入新的 USN 記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-131">The NTFS file system does not write a new USN record.</span></span> <span data-ttu-id="a212a-132">因為 \_ \_ \_ 現有記錄已設定 USN 原因數據覆寫，所以不會對記錄進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="a212a-132">Because USN\_REASON\_DATA\_OVERWRITE is already set for the existing record, no changes are made to the record.</span></span><br/>                                                                                           |
| <span data-ttu-id="a212a-133">檔案截斷</span><span class="sxs-lookup"><span data-stu-id="a212a-133">File truncation</span></span><br/>            | <span data-ttu-id="a212a-134">NTFS 檔案系統會寫入新的 USN 記錄，其中包含旗標設定 USN \_ 原因 \_ 資料 \_ 覆寫 \| usn 原因 \_ \_ 基本 \_ 資訊 \_ 變更 \| usn \_ 原因 \_ 資料 \_ 截斷。</span><span class="sxs-lookup"><span data-stu-id="a212a-134">The NTFS file system writes a new USN record with the flag setting USN\_REASON\_DATA\_OVERWRITE \| USN\_REASON\_BASIC\_INFO\_CHANGE \| USN\_REASON\_DATA\_TRUNCATION.</span></span><br/>                                                                                           |
| <span data-ttu-id="a212a-135">第三個寫入操作</span><span class="sxs-lookup"><span data-stu-id="a212a-135">Third write operation</span></span><br/>      | <span data-ttu-id="a212a-136">NTFS 檔案系統不會寫入新的 USN 記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-136">The NTFS file system does not write a new USN record.</span></span> <span data-ttu-id="a212a-137">因為 \_ \_ \_ 現有記錄已設定 USN 原因數據覆寫，所以不會對記錄進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="a212a-137">Because USN\_REASON\_DATA\_OVERWRITE is already set for the existing record, no changes are made to the record.</span></span><br/>                                                                                           |
| <span data-ttu-id="a212a-138">關閉操作</span><span class="sxs-lookup"><span data-stu-id="a212a-138">Close operation</span></span><br/>            | <span data-ttu-id="a212a-139">如果使用者進行變更是檔案的唯一使用者，則 NTFS 檔案系統會以下列旗標設定寫入新的 USN 記錄： USN \_ 原因 \_ 資料 \_ 覆寫 \| usn \_ 原因 \_ 基本 \_ 資訊 \_ 變更 \| USN \_ 原因 \_ 資料 \_ 截斷 \| usn \_ 原因 \_ 關閉。</span><span class="sxs-lookup"><span data-stu-id="a212a-139">If the user making changes is the only user of the file, the NTFS file system writes a new USN record with the following flag setting: USN\_REASON\_DATA\_OVERWRITE \| USN\_REASON\_BASIC\_INFO\_CHANGE \| USN\_REASON\_DATA\_TRUNCATION \| USN\_REASON\_CLOSE.</span></span><br/> |



 

<span data-ttu-id="a212a-140">變更日誌會在檔案的第一次開頭和最後一個結尾之間累積一系列的記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-140">The change journal accumulates a series of records between the first opening and last closing of a file.</span></span> <span data-ttu-id="a212a-141">每一筆記錄都有新的原因旗標設定，表示已發生新的變更類型。</span><span class="sxs-lookup"><span data-stu-id="a212a-141">Each record has a new reason flag set, indicating that a new kind of change has occurred.</span></span> <span data-ttu-id="a212a-142">記錄的順序會提供檔案的部分歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-142">The sequence of records gives a partial history of the file.</span></span> <span data-ttu-id="a212a-143">最後一筆記錄會在檔案關閉時建立，並新增 USN \_ 原因 \_ 關閉旗標。</span><span class="sxs-lookup"><span data-stu-id="a212a-143">The final record, created when the file is closed, adds the USN\_REASON\_CLOSE flag.</span></span> <span data-ttu-id="a212a-144">此記錄代表檔案變更的摘要，但是與先前記錄不同的是，不會指出變更的順序。</span><span class="sxs-lookup"><span data-stu-id="a212a-144">This record represents a summary of changes to the file, but unlike the prior records, gives no indication of the order of the changes.</span></span>

<span data-ttu-id="a212a-145">下次存取和變更檔案的使用者會產生具有單一原因旗標的新 USN 記錄。</span><span class="sxs-lookup"><span data-stu-id="a212a-145">The next user to access and change the file generates a new USN record with a single reason flag.</span></span>

 

 




