---
title: 備份功能
description: 下列函式會搭配磁帶備份使用。
ms.assetid: 8c5f92f7-4918-475c-bc86-2b02291488d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312c7477c28f83b7c1c64073234799219346f89a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682762"
---
# <a name="backup-functions"></a><span data-ttu-id="222cf-103">備份功能</span><span class="sxs-lookup"><span data-stu-id="222cf-103">Backup Functions</span></span>

<span data-ttu-id="222cf-104">下列函式會搭配 [磁帶備份](tape-backup.md)使用。</span><span class="sxs-lookup"><span data-stu-id="222cf-104">The following functions are used with [tape backup](tape-backup.md).</span></span>



| <span data-ttu-id="222cf-105">函式</span><span class="sxs-lookup"><span data-stu-id="222cf-105">Function</span></span>                                           | <span data-ttu-id="222cf-106">描述</span><span class="sxs-lookup"><span data-stu-id="222cf-106">Description</span></span>                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="222cf-107">**BackupRead**</span><span class="sxs-lookup"><span data-stu-id="222cf-107">**BackupRead**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupread)                   | <span data-ttu-id="222cf-108">將與指定檔案或目錄相關聯的資料讀入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="222cf-108">Reads data associated with a specified file or directory into a buffer.</span></span>                                |
| [<span data-ttu-id="222cf-109">**BackupSeek**</span><span class="sxs-lookup"><span data-stu-id="222cf-109">**BackupSeek**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupseek)                   | <span data-ttu-id="222cf-110">在資料流程中向前搜尋。</span><span class="sxs-lookup"><span data-stu-id="222cf-110">Seeks forward in a data stream.</span></span>                                                                        |
| [<span data-ttu-id="222cf-111">**BackupWrite**</span><span class="sxs-lookup"><span data-stu-id="222cf-111">**BackupWrite**</span></span>](/windows/desktop/api/Winbase/nf-winbase-backupwrite)                 | <span data-ttu-id="222cf-112">從緩衝區將資料串流寫入至指定的檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="222cf-112">Writes a stream of data from a buffer to a specified file or directory.</span></span>                                |
| [<span data-ttu-id="222cf-113">**CreateTapePartition**</span><span class="sxs-lookup"><span data-stu-id="222cf-113">**CreateTapePartition**</span></span>](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) | <span data-ttu-id="222cf-114">重新格式化磁帶。</span><span class="sxs-lookup"><span data-stu-id="222cf-114">Reformats a tape.</span></span>                                                                                      |
| [<span data-ttu-id="222cf-115">**EraseTape**</span><span class="sxs-lookup"><span data-stu-id="222cf-115">**EraseTape**</span></span>](/windows/desktop/api/Winbase/nf-winbase-erasetape)                     | <span data-ttu-id="222cf-116">清除所有或部分磁帶。</span><span class="sxs-lookup"><span data-stu-id="222cf-116">Erases all or part of a tape.</span></span>                                                                          |
| [<span data-ttu-id="222cf-117">**GetTapeParameters**</span><span class="sxs-lookup"><span data-stu-id="222cf-117">**GetTapeParameters**</span></span>](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters)     | <span data-ttu-id="222cf-118">抓取描述磁帶或磁帶機的資訊。</span><span class="sxs-lookup"><span data-stu-id="222cf-118">Retrieves information that describes the tape or the tape drive.</span></span>                                       |
| [<span data-ttu-id="222cf-119">**GetTapePosition**</span><span class="sxs-lookup"><span data-stu-id="222cf-119">**GetTapePosition**</span></span>](/windows/desktop/api/Winbase/nf-winbase-gettapeposition)         | <span data-ttu-id="222cf-120">抓取磁帶的目前位址。</span><span class="sxs-lookup"><span data-stu-id="222cf-120">Retrieves the current address of the tape.</span></span>                                                             |
| [<span data-ttu-id="222cf-121">**GetTapeStatus**</span><span class="sxs-lookup"><span data-stu-id="222cf-121">**GetTapeStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-gettapestatus)             | <span data-ttu-id="222cf-122">判斷磁帶裝置是否已準備好處理磁帶命令。</span><span class="sxs-lookup"><span data-stu-id="222cf-122">Determines whether the tape device is ready to process tape commands.</span></span>                                  |
| [<span data-ttu-id="222cf-123">**PrepareTape**</span><span class="sxs-lookup"><span data-stu-id="222cf-123">**PrepareTape**</span></span>](/windows/desktop/api/Winbase/nf-winbase-preparetape)                 | <span data-ttu-id="222cf-124">準備要存取或移除的磁帶。</span><span class="sxs-lookup"><span data-stu-id="222cf-124">Prepares the tape to be accessed or removed.</span></span>                                                           |
| [<span data-ttu-id="222cf-125">**SetTapeParameters**</span><span class="sxs-lookup"><span data-stu-id="222cf-125">**SetTapeParameters**</span></span>](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)     | <span data-ttu-id="222cf-126">指定磁帶的區塊大小或設定磁帶裝置。</span><span class="sxs-lookup"><span data-stu-id="222cf-126">Specifies the block size of a tape or configures the tape device.</span></span>                                      |
| [<span data-ttu-id="222cf-127">**SetTapePosition**</span><span class="sxs-lookup"><span data-stu-id="222cf-127">**SetTapePosition**</span></span>](/windows/desktop/api/Winbase/nf-winbase-settapeposition)         | <span data-ttu-id="222cf-128">設定指定裝置上的磁帶位置。</span><span class="sxs-lookup"><span data-stu-id="222cf-128">Sets the tape position on the specified device.</span></span>                                                        |
| [<span data-ttu-id="222cf-129">**WriteTapemark**</span><span class="sxs-lookup"><span data-stu-id="222cf-129">**WriteTapemark**</span></span>](/windows/desktop/api/Winbase/nf-winbase-writetapemark)             | <span data-ttu-id="222cf-130">將指定數目的格式標記、setmarks、短格式標記或長標記寫入磁帶裝置。</span><span class="sxs-lookup"><span data-stu-id="222cf-130">Writes a specified number of filemarks, setmarks, short filemarks, or long filemarks to a tape device.</span></span> |



 

<span data-ttu-id="222cf-131">下列函式是針對使用 [單一實例存放區和 SIS 備份](single-instance-store-and-sis-backup.md)所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="222cf-131">The following functions are provided for working with [single-instance store and SIS backup](single-instance-store-and-sis-backup.md).</span></span>



| <span data-ttu-id="222cf-132">函式</span><span class="sxs-lookup"><span data-stu-id="222cf-132">Function</span></span>                                                          | <span data-ttu-id="222cf-133">描述</span><span class="sxs-lookup"><span data-stu-id="222cf-133">Description</span></span>                                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="222cf-134">**SisCreateBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="222cf-134">**SisCreateBackupStructure**</span></span>](siscreatebackupstructure.md)      | <span data-ttu-id="222cf-135">根據提供的資訊建立指定的 SIS 備份結構。</span><span class="sxs-lookup"><span data-stu-id="222cf-135">Creates the specified SIS backup structure based on the supplied information.</span></span>                      |
| [<span data-ttu-id="222cf-136">**SisCreateRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="222cf-136">**SisCreateRestoreStructure**</span></span>](siscreaterestorestructure.md)    | <span data-ttu-id="222cf-137">根據提供的資訊建立指定的 SIS 還原結構。</span><span class="sxs-lookup"><span data-stu-id="222cf-137">Creates the specified SIS restore structure based on the supplied information.</span></span>                     |
| [<span data-ttu-id="222cf-138">**SisCSFilesToBackupForLink**</span><span class="sxs-lookup"><span data-stu-id="222cf-138">**SisCSFilesToBackupForLink**</span></span>](siscsfilestobackupforlink.md)    | <span data-ttu-id="222cf-139">傳回描述指定 SIS 連結指向之通用存放區檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="222cf-139">Returns information describing the common-store files the specified SIS link points to.</span></span>            |
| [<span data-ttu-id="222cf-140">**SisFreeAllocatedMemory**</span><span class="sxs-lookup"><span data-stu-id="222cf-140">**SisFreeAllocatedMemory**</span></span>](sisfreeallocatedmemory.md)          | <span data-ttu-id="222cf-141">釋出 SIS API 函數所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="222cf-141">Frees memory allocated by SIS API functions.</span></span>                                                       |
| [<span data-ttu-id="222cf-142">**SisFreeBackupStructure**</span><span class="sxs-lookup"><span data-stu-id="222cf-142">**SisFreeBackupStructure**</span></span>](sisfreebackupstructure.md)          | <span data-ttu-id="222cf-143">釋出指定的 SIS 備份結構。</span><span class="sxs-lookup"><span data-stu-id="222cf-143">Frees the specified SIS backup structure.</span></span>                                                          |
| [<span data-ttu-id="222cf-144">**SisFreeRestoreStructure**</span><span class="sxs-lookup"><span data-stu-id="222cf-144">**SisFreeRestoreStructure**</span></span>](sisfreerestorestructure.md)        | <span data-ttu-id="222cf-145">釋出指定的 SIS 還原結構。</span><span class="sxs-lookup"><span data-stu-id="222cf-145">Frees the specified SIS restore structure.</span></span>                                                         |
| [<span data-ttu-id="222cf-146">**SisRestoredCommon StoreFile**</span><span class="sxs-lookup"><span data-stu-id="222cf-146">**SisRestoredCommon StoreFile**</span></span>](sisrestoredcommonstorefile.md) | <span data-ttu-id="222cf-147">報告已寫入一般存放區檔案的 SIS 架構。</span><span class="sxs-lookup"><span data-stu-id="222cf-147">Reports to the SIS architecture that a common-store file has been written.</span></span>                         |
| [<span data-ttu-id="222cf-148">**SisRestoredLink**</span><span class="sxs-lookup"><span data-stu-id="222cf-148">**SisRestoredLink**</span></span>](sisrestoredlink.md)                        | <span data-ttu-id="222cf-149">傳回指定的已還原 SIS 連結所指向的通用存放區檔案或檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="222cf-149">Returns the names of the common-store file or files pointed to by the specified restored SIS link.</span></span> |



 

<span data-ttu-id="222cf-150">以下是針對加密檔案的 [備份和還原](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files)所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="222cf-150">The following functions are provided for working with [backup and restore of encrypted files](/windows/desktop/FileIO/backup-and-restore-of-encrypted-files).</span></span>



| <span data-ttu-id="222cf-151">函式</span><span class="sxs-lookup"><span data-stu-id="222cf-151">Function</span></span>                                                | <span data-ttu-id="222cf-152">描述</span><span class="sxs-lookup"><span data-stu-id="222cf-152">Description</span></span>                                                                                |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="222cf-153">**CloseEncryptedFileRaw**</span><span class="sxs-lookup"><span data-stu-id="222cf-153">**CloseEncryptedFileRaw**</span></span>](/windows/desktop/api/winbase/nf-winbase-closeencryptedfileraw) | <span data-ttu-id="222cf-154">關閉以 [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)開啟的加密檔案。</span><span class="sxs-lookup"><span data-stu-id="222cf-154">Close an encrypted file opened with [**OpenEncryptedFileRaw**](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa).</span></span> |
| [<span data-ttu-id="222cf-155">**OpenEncryptedFileRaw**</span><span class="sxs-lookup"><span data-stu-id="222cf-155">**OpenEncryptedFileRaw**</span></span>](/windows/desktop/api/winbase/nf-winbase-openencryptedfilerawa)   | <span data-ttu-id="222cf-156">開啟加密的檔案，並存取加密格式的資料。</span><span class="sxs-lookup"><span data-stu-id="222cf-156">Open an encrypted file with access to data in encrypted format.</span></span>                            |
| [<span data-ttu-id="222cf-157">**ReadEncryptedFileRaw**</span><span class="sxs-lookup"><span data-stu-id="222cf-157">**ReadEncryptedFileRaw**</span></span>](/windows/desktop/api/winbase/nf-winbase-readencryptedfileraw)   | <span data-ttu-id="222cf-158">讀取加密的檔案，以加密格式保留其資料。</span><span class="sxs-lookup"><span data-stu-id="222cf-158">Read an encrypted file leaving its data in encrypted format.</span></span>                               |
| [<span data-ttu-id="222cf-159">**WriteEncryptedFileRaw**</span><span class="sxs-lookup"><span data-stu-id="222cf-159">**WriteEncryptedFileRaw**</span></span>](/windows/desktop/api/winbase/nf-winbase-writeencryptedfileraw) | <span data-ttu-id="222cf-160">撰寫加密的檔案，以加密格式保留其資料。</span><span class="sxs-lookup"><span data-stu-id="222cf-160">Write an encrypted file leaving its data in encrypted format.</span></span>                              |



 

 

 