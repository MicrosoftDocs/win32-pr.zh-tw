---
description: 包含 USB 裝置的序號。 它是由 IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號控制項程式 \_ 代碼所使用。
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997314"
---
# <a name="media_serial_number_data-structure"></a>媒體 \_ 序號 \_ \_ 資料結構

包含 USB 裝置的序號。 它是由 [**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號 \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) 控制項程式碼所使用。

## <a name="syntax"></a>語法


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

**SerialNumberData** 字串的大小（以位元組為單位）。

</dd> <dt>

**結果**
</dt> <dd>

要求的狀態。

</dd> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> <dt>

**SerialNumberData**
</dt> <dd>

裝置的序號。

</dd> </dl>

## <a name="remarks"></a>備註

**媒體 \_ 序號 \_ \_ 資料** 結構沒有可用的標頭檔。 在您的原始程式碼中，將結構定義包含在此頁面的頂端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>          |
| 最低支援的伺服器<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ 儲存體 \_ 取得 \_ 媒體 \_ 序號 \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




