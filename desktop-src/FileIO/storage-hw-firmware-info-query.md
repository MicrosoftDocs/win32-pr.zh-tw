---
description: STORAGE_HW_FIRMWARE_INFO_QUERY 結構-此結構包含裝置固件的相關資訊。
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: 'STORAGE_HW_FIRMWARE_INFO_QUERY 結構 (Winioctl .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119396"
---
# <a name="storage_hw_firmware_info_query-structure"></a>儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢結構

此結構包含裝置固件的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 這應該設定為 sizeof (儲存體 \_ HW \_ 固件 \_ 資訊 \_ 查詢) 

</dd> <dt>

**大小**
</dt> <dd>

此結構的大小，表示為緩衝區。

</dd> <dt>

**旗標**
</dt> <dd>

與查詢相關聯的旗標。 以下是可以在這個成員中設定的旗標。



| 旗標                                             | 描述                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| 儲存體 \_ HW \_ 固件 \_ 要求 \_ 旗標 \_ 控制器 | 指出裝置手動/物件本身以外的要求目標。 |



 

</dd> <dt>

**已保留**
</dt> <dd>

保留供未來使用。

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

[**儲存體 \_ HW \_ 固件 \_ 插槽 \_ 資訊**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




