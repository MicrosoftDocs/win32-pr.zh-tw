---
description: 包含裝置大小的相關資訊。 這會從 IOCTL \_ 儲存體 \_ 讀取 \_ 容量控制程式代碼傳回。
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: 'STORAGE_READ_CAPACITY 結構 (Ntddstor .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: 3a138f6594e241c96526ebf6955c61374aa0f48a5aa66f364ef82c1591b64594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404969"
---
# <a name="storage_read_capacity-structure"></a>儲存體 \_ 讀取 \_ 容量結構

包含裝置大小的相關資訊。 這會從 [**IOCTL \_ 儲存體 \_ 讀取 \_ 容量**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) 控制程式代碼傳回。

## <a name="syntax"></a>語法


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

此結構的版本。 呼叫端必須將這個成員設定為 `sizeof(STORAGE_READ_CAPACITY)` 。

</dd> <dt>

**大小**
</dt> <dd>

傳回的資料大小。

</dd> <dt>

**BlockLength**
</dt> <dd>

每個區塊的位元組數目。

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

磁片上的區塊總數。

</dd> <dt>

**DiskLength**
</dt> <dd>

磁片大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

標頭檔 Ntddstor 可在 Windows 驅動程式套件 (WDK) 中取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                              |
| 最低支援的伺服器<br/> | Windowsserver 2008、Windows server 2003 SP1<br/>                          |
| 標頭<br/>                   | <dl> <dt>Ntddstor。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ 儲存體 \_ 讀取 \_ 容量**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




