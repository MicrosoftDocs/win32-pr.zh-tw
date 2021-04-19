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
# <a name="disk-partition-types"></a>磁碟分割類型

下表將識別磁片驅動程式所使用的有效磁碟分割類型。



| 常數/值                                                                                                                                                                                                                                      | Description                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**分割 \_ 區\_未使用的專案**</dt> <dt>0x00</dt> </dl> | 未使用的專案分割。<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**分割 \_ 區擴充**</dt> <dt>0x05</dt> </dl>              | 擴充的資料分割。<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**分割 \_ 區FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | FAT12 檔案系統分割區。<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**分割 \_ 區FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | FAT16 檔案系統分區。<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**分割 \_ 區FAT32**</dt> <dt>0x0B</dt> </dl>                       | FAT32 檔案系統分區。<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**分割 \_ 區IFS**</dt> <dt>0x07</dt> </dl>                             | IFS 資料分割。<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**分割 \_ 區LDM**</dt> <dt>0x42</dt> </dl>                             | 邏輯磁片管理員 (LDM) 磁碟分割。<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**分割 \_ 區NTFT**</dt> <dt>0x80</dt> </dl>                          | NTFT 分割區。<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <dt>**有效 \_NTFT**</dt> <dt>0xC0</dt> </dl>                                      | 有效的 NTFT 分割區。<br/> 資料分割類型程式碼的最高位表示分割區是 NTFT 鏡像或等量陣列的一部分。<br/> |



## <a name="remarks"></a>備註

有幾個宏可協助您偵測分割區類型： **IsContainerPartition**、 **IsFTPartition** 和 **IsRecognizedPartition**。 如需詳細資訊，請參閱 WinIoCtl。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>WinIoCtl (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**分割區 \_ 資訊， \_ 例如**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**分割區 \_ 資訊 \_ MBR**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**設定資料 \_ 分割 \_ 資訊**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




