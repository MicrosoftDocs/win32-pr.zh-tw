---
description: Msvm_DiskDrive 類別的 reset 方法-要求重設。
ms.assetid: 1c1de976-fa2b-4401-baa3-e5e0ed23f6ff
title: Msvm_DiskDrive 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c49c3e5ba0f71868e26ad18e8b0afe2f8602f2e5aa4abaec3ade43a67269c81e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130508"
---
# <a name="reset-method-of-the-msvm_diskdrive-class"></a>Msvm DiskDrive 類別的 Reset 方法 \_

要求重設。

## <a name="syntax"></a>語法


```mof
uint32 Reset();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 




