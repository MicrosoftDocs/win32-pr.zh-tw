---
title: 'BFT 常數 (Ntdsbcli) '
description: BFT 常數會當做位旗標使用，以識別 Active Directory Domain Services 備份中的不同檔案類型。
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934220"
---
# <a name="bft-constants"></a><span data-ttu-id="6e09d-103">BFT 常數</span><span class="sxs-lookup"><span data-stu-id="6e09d-103">BFT Constants</span></span>

<span data-ttu-id="6e09d-104">BFT 常數會當做位旗標使用，以識別 Active Directory Domain Services 備份中的不同檔案類型。</span><span class="sxs-lookup"><span data-stu-id="6e09d-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="6e09d-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT \_ 記錄檔 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="6e09d-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-106">0x20</span><span class="sxs-lookup"><span data-stu-id="6e09d-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-107">檔案屬於記錄檔目錄。</span><span class="sxs-lookup"><span data-stu-id="6e09d-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT \_ 資料庫 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="6e09d-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-109">0x40</span><span class="sxs-lookup"><span data-stu-id="6e09d-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-110">檔案屬於資料庫目錄。</span><span class="sxs-lookup"><span data-stu-id="6e09d-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="6e09d-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-112">0x80</span><span class="sxs-lookup"><span data-stu-id="6e09d-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-113">指定的路徑是目錄，而不是檔案名。</span><span class="sxs-lookup"><span data-stu-id="6e09d-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ 記錄檔**</span><span class="sxs-lookup"><span data-stu-id="6e09d-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-115">0x21</span><span class="sxs-lookup"><span data-stu-id="6e09d-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-116">指定隸屬于記錄檔目錄中的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="6e09d-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ 記錄檔 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="6e09d-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-118">0x22</span><span class="sxs-lookup"><span data-stu-id="6e09d-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-119">檔案是記錄檔目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="6e09d-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ 檢查點 \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="6e09d-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-121">0x23</span><span class="sxs-lookup"><span data-stu-id="6e09d-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-122">檔案是檢查點目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="6e09d-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**</span><span class="sxs-lookup"><span data-stu-id="6e09d-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-124">0x44</span><span class="sxs-lookup"><span data-stu-id="6e09d-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-125">檔案是屬於資料庫目錄的目錄服務資料庫。</span><span class="sxs-lookup"><span data-stu-id="6e09d-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ 修補 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="6e09d-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-127">0x25</span><span class="sxs-lookup"><span data-stu-id="6e09d-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-128">檔案是屬於記錄檔目錄的修補檔案。</span><span class="sxs-lookup"><span data-stu-id="6e09d-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e09d-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ 不明**</span><span class="sxs-lookup"><span data-stu-id="6e09d-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6e09d-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="6e09d-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="6e09d-131">無法辨識該檔案。</span><span class="sxs-lookup"><span data-stu-id="6e09d-131">The file cannot be recognized.</span></span> <span data-ttu-id="6e09d-132">檔案不會與已知的檔案名和檔案類型一致。</span><span class="sxs-lookup"><span data-stu-id="6e09d-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e09d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e09d-133">Requirements</span></span>



| <span data-ttu-id="6e09d-134">需求</span><span class="sxs-lookup"><span data-stu-id="6e09d-134">Requirement</span></span> | <span data-ttu-id="6e09d-135">值</span><span class="sxs-lookup"><span data-stu-id="6e09d-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e09d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e09d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6e09d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6e09d-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="6e09d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e09d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6e09d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6e09d-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="6e09d-140">標頭</span><span class="sxs-lookup"><span data-stu-id="6e09d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e09d-141"><dt>Ntdsbcli。h</dt></span><span class="sxs-lookup"><span data-stu-id="6e09d-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





