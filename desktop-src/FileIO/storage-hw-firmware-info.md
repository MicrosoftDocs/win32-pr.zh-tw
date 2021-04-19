---
description: 此結構包含裝置固件的相關資訊。
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: 'STORAGE_HW_FIRMWARE_INFO 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985691"
---
# <a name="storage_hw_firmware_info-structure"></a>儲存體 \_ HW \_ 固件 \_ 資訊結構

此結構包含裝置固件的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 這應該設定為 sizeof (儲存體 \_ HW \_ 固件 \_ 資訊) 

</dd> <dt>

**大小**
</dt> <dd>

此結構的大小，表示為包含位置的緩衝區。

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

指出此固件支援升級。

</dd> <dt>

**Reserved0**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**SlotCount**
</dt> <dd>

裝置上的固件插槽數目。 這是插槽陣列的維度。

> [!Note]  
> 某些裝置可以儲存1個以上的固件映射（如果有一個以上的固件插槽）。

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

包含目前作用中/正在執行之固件映射的固件位置。

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

暫止啟用的固件插槽。

</dd> <dt>

**FirmwareShared**
</dt> <dd>

指出此固件同時適用于裝置和控制器/介面卡，例如 NVMe SSD。

</dd> <dt>

**已保留**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

影像承載的對齊（以位元組數為單位）。 最大值為頁面 \_ 大小。 傳輸大小是此大小的其中一種。 某些通訊協定需要的磁區大小至少為磁區。 當此值設定為0時，表示此值無效。

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

映射裝載大小上限，這會用於單一命令。

</dd> <dt>

**位置**
</dt> <dd>

包含裝置上每個插槽的位置資訊，其類型為 [**儲存體 \_ HW \_ 固件 \_ 位置 \_ 資訊**](storage-hw-firmware-slot-info.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Winioctl (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_啟用 IOCTL 儲存體 \_ 固件 \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**儲存體 \_ HW \_ 固件 \_ 啟動**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**IOCTL \_ 儲存體 \_ 固件 \_ 下載**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**儲存體 \_ HW \_ 固件 \_ 下載**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**IOCTL \_ 儲存體 \_ 固件 \_ 取得 \_ 資訊**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




