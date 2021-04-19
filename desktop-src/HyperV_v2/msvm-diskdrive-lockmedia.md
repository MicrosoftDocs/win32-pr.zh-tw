---
description: 鎖定或解除鎖定媒體。
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Msvm_DiskDrive 類別的 LockMedia 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986018"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a>Msvm DiskDrive 類別的 LockMedia 方法 \_

鎖定或解除鎖定媒體。

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

這個方法會傳回下列其中一個值：

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

[**Msvm \_ DiskDrive**](msvm-diskdrive.md)
</dt> </dl>

 

 




