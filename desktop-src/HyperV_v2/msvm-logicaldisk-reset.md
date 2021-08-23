---
description: Msvm_LogicalDisk 類別的 reset 方法-要求重設。
ms.assetid: 544bd327-572d-4f0e-bc73-a68113222af0
title: Msvm_LogicalDisk 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 148fe50877fd3add3b2005edce4c96ac519c2e1677a9e0895272538d703a74f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521798"
---
# <a name="reset-method-of-the-msvm_logicaldisk-class"></a>Msvm LogicalDisk 類別的 Reset 方法 \_

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

[**Msvm \_ LogicalDisk**](msvm-logicaldisk.md)
</dt> </dl>

 

 




