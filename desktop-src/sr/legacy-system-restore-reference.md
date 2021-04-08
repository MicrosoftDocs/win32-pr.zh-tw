---
title: 舊版系統還原參考
description: 本檔說明舊版系統還原所使用的儲存機制的執行詳細資料。 它並不適用于 Windows Vista 上的系統還原執行。
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839343"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="3550a-104">舊版系統還原參考</span><span class="sxs-lookup"><span data-stu-id="3550a-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="3550a-105">\[此資訊只適用于 Windows XP Service Pack 2 (SP2) 。\]</span><span class="sxs-lookup"><span data-stu-id="3550a-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="3550a-106">本檔說明舊版系統還原所使用的儲存機制的執行詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3550a-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="3550a-107">它並不適用于 Windows Vista 上的系統還原執行。</span><span class="sxs-lookup"><span data-stu-id="3550a-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="3550a-108">系統還原存放庫結構</span><span class="sxs-lookup"><span data-stu-id="3550a-108">System Restore Repository Structure</span></span>

<span data-ttu-id="3550a-109">Windows XP （含 SP2）包含下列資料夾中系統還原的儲存機制：% SYSTEMDRIVE% \\ 系統磁碟區資訊。</span><span class="sxs-lookup"><span data-stu-id="3550a-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="3550a-110">此存放庫包含還原點的資訊，基本上是系統的快照集。</span><span class="sxs-lookup"><span data-stu-id="3550a-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="3550a-111">存放庫的結構如下：</span><span class="sxs-lookup"><span data-stu-id="3550a-111">The repository is structured as follows:</span></span>

<span data-ttu-id="3550a-112">**系統磁碟區資訊**    \*\* \_ 還原 {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **rp \* n** \*     \*\* \_ restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n-1*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="3550a-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="3550a-113">若要判斷 \_ 要使用哪一個 restore {*GUID*} 資料夾，請閱讀下列檔案中指定的 **GUID** ： SYSTEMROOT% \\ System32 \\ restore \\MachineGUID.txt。</span><span class="sxs-lookup"><span data-stu-id="3550a-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="3550a-114">在每個 \_ restore {*GUID*} 資料夾中，driver .config 檔案 \_ 包含的資訊來自于定義如下的 **sr-iov \_ 持續 \_** 設定結構：</span><span class="sxs-lookup"><span data-stu-id="3550a-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="3550a-115">每個 RP *n* 資料夾中包含的檔案</span><span class="sxs-lookup"><span data-stu-id="3550a-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="3550a-116">每個 RP *n* 資料夾都包含快照集資料夾，其中包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="3550a-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="3550a-117">登錄 hive 的快照</span><span class="sxs-lookup"><span data-stu-id="3550a-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="3550a-118">包含 WMI 存放庫快照集的存放庫資料夾</span><span class="sxs-lookup"><span data-stu-id="3550a-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="3550a-119">COM + 資料庫的快照集</span><span class="sxs-lookup"><span data-stu-id="3550a-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="3550a-120">IIS 資料庫的快照集</span><span class="sxs-lookup"><span data-stu-id="3550a-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="3550a-121">每個 RP *n* 資料夾都包含一個 rp .log 檔案，其中包含來自 [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) 結構之還原點的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="3550a-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="3550a-122">每個 RP *n* 資料夾都可能包含用來追蹤還原點變更的檔案。</span><span class="sxs-lookup"><span data-stu-id="3550a-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="3550a-123">第一個檔案的名稱為 change .log，下一個檔案的名稱為 change .log。</span><span class="sxs-lookup"><span data-stu-id="3550a-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="3550a-124">每個變更記錄檔都包含下列結構：</span><span class="sxs-lookup"><span data-stu-id="3550a-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="3550a-125">**變更 \_ 記錄 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="3550a-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="3550a-126">[**變更 \_記錄 \_ 專案**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="3550a-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="3550a-127">[**變更 \_記錄 \_ 專案**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="3550a-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="3550a-128">...</span><span class="sxs-lookup"><span data-stu-id="3550a-128">...</span></span>
-   <span data-ttu-id="3550a-129">[**變更 \_記錄 \_ 專案**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="3550a-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="3550a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="3550a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3550a-131">舊版系統還原結構</span><span class="sxs-lookup"><span data-stu-id="3550a-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




