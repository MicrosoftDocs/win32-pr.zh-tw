---
description: 此結構包含裝置上某個位置的相關資訊。
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: 'STORAGE_HW_FIRMWARE_SLOT_INFO 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001343"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊結構

此結構包含裝置上某個位置的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 這應該設定為 sizeof (儲存體 \_ HW \_ 固件插槽 \_ 的 \_ 資訊) 

</dd> <dt>

**大小**
</dt> <dd>

此結構的大小。

</dd> <dt>

**SlotNumber**
</dt> <dd>

此位置的插槽號碼。

</dd> <dt>

**ReadOnly**
</dt> <dd>

指出此位置是否為唯讀。

</dd> <dt>

**Reserved0**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**Reserved1**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**修訂**
</dt> <dd>

此位置上的固件修訂。

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

[**儲存體 \_ HW \_ 固件 \_ 資訊**](storage-hw-firmware-info.md)
</dt> <dt>

[**儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




