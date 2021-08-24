---
description: 將非遮罩式插斷插入虛擬機器中。
ms.assetid: 897AD1B9-0EDD-4DCE-963D-D5DE03AF55A9
title: Msvm_ComputerSystem：： InjectNonMaskableInterrupt 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.InjectNonMaskableInterrupt
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9019492299d03b31001b60934e00dc40c41b4328e4809fe8e864ef378c30a89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694438"
---
# <a name="msvm_computersysteminjectnonmaskableinterrupt-method"></a>Msvm \_ ：： InjectNonMaskableInterrupt 方法

將非遮罩式插斷插入虛擬機器中。

## <a name="syntax"></a>語法


```C++
uint32 InjectNonMaskableInterrupt(
  [out] CIM_ConcreteJob Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)) 之物件的參考，以追蹤中斷插入的狀態。 如果工作已完成，此參考可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_**](msvm-computersystem.md)
</dt> </dl>

 

