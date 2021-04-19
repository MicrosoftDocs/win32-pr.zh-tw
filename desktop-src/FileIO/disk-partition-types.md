---
description: 磁片驅動程式所使用的有效磁碟分割類型。
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: '磁碟分割類型 (WinIoCtl .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983836"
---
# <a name="disk-partition-types"></a><span data-ttu-id="9de2c-103">磁碟分割類型</span><span class="sxs-lookup"><span data-stu-id="9de2c-103">Disk Partition Types</span></span>

<span data-ttu-id="9de2c-104">下表將識別磁片驅動程式所使用的有效磁碟分割類型。</span><span class="sxs-lookup"><span data-stu-id="9de2c-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="9de2c-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="9de2c-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="9de2c-106">Description</span><span class="sxs-lookup"><span data-stu-id="9de2c-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="9de2c-107"><dt>**分割 \_ 區\_未使用的專案**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="9de2c-108">未使用的專案分割。</span><span class="sxs-lookup"><span data-stu-id="9de2c-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="9de2c-109"><dt>**分割 \_ 區擴充**</dt> <dt>0x05</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="9de2c-110">擴充的資料分割。</span><span class="sxs-lookup"><span data-stu-id="9de2c-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="9de2c-111"><dt>**分割 \_ 區FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="9de2c-112">FAT12 檔案系統分割區。</span><span class="sxs-lookup"><span data-stu-id="9de2c-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="9de2c-113"><dt>**分割 \_ 區FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="9de2c-114">FAT16 檔案系統分區。</span><span class="sxs-lookup"><span data-stu-id="9de2c-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="9de2c-115"><dt>**分割 \_ 區FAT32**</dt> <dt>0x0B</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="9de2c-116">FAT32 檔案系統分區。</span><span class="sxs-lookup"><span data-stu-id="9de2c-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="9de2c-117"><dt>**分割 \_ 區IFS**</dt> <dt>0x07</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="9de2c-118">IFS 資料分割。</span><span class="sxs-lookup"><span data-stu-id="9de2c-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="9de2c-119"><dt>**分割 \_ 區LDM**</dt> <dt>0x42</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="9de2c-120">邏輯磁片管理員 (LDM) 磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="9de2c-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="9de2c-121"><dt>**分割 \_ 區NTFT**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="9de2c-122">NTFT 分割區。</span><span class="sxs-lookup"><span data-stu-id="9de2c-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="9de2c-123"><dt>**有效 \_NTFT**</dt> <dt>0xC0</dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="9de2c-124">有效的 NTFT 分割區。</span><span class="sxs-lookup"><span data-stu-id="9de2c-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="9de2c-125">資料分割類型程式碼的最高位表示分割區是 NTFT 鏡像或等量陣列的一部分。</span><span class="sxs-lookup"><span data-stu-id="9de2c-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9de2c-126">備註</span><span class="sxs-lookup"><span data-stu-id="9de2c-126">Remarks</span></span>

<span data-ttu-id="9de2c-127">有幾個宏可協助您偵測分割區類型： **IsContainerPartition**、 **IsFTPartition** 和 **IsRecognizedPartition**。</span><span class="sxs-lookup"><span data-stu-id="9de2c-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="9de2c-128">如需詳細資訊，請參閱 WinIoCtl。</span><span class="sxs-lookup"><span data-stu-id="9de2c-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de2c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de2c-129">Requirements</span></span>



| <span data-ttu-id="9de2c-130">需求</span><span class="sxs-lookup"><span data-stu-id="9de2c-130">Requirement</span></span> | <span data-ttu-id="9de2c-131">值</span><span class="sxs-lookup"><span data-stu-id="9de2c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9de2c-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9de2c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9de2c-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9de2c-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="9de2c-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9de2c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9de2c-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9de2c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9de2c-136">標頭</span><span class="sxs-lookup"><span data-stu-id="9de2c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de2c-137"><dt>WinIoCtl (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="9de2c-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de2c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de2c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de2c-139">**分割區 \_ 資訊， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="9de2c-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="9de2c-140">**分割區 \_ 資訊 \_ MBR**</span><span class="sxs-lookup"><span data-stu-id="9de2c-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="9de2c-141">**設定資料 \_ 分割 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="9de2c-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




