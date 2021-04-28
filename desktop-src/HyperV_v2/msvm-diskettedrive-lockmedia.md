---
description: Msvm_DisketteDrive 類別的 LockMedia 方法-鎖定或釋放媒體。
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Msvm_DisketteDrive 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111972"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a>Msvm DisketteDrive 類別的 LockMedia 方法 \_

鎖定或釋放媒體。

## <a name="syntax"></a>語法


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*鎖定* \[在\]
</dt> <dd>

**true** 表示鎖定媒體; **false** 表示釋放媒體。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回下列其中一個值：

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)
</dt> </dl>

 

 




