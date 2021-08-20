---
description: 停用實體 GPU 以進行虛擬化。
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Msvm_Synthetic3DService 類別的 DisableGPUForVirtualization 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f156ee160f9ae158c36b1c7a237f746d6577906cc5e254a183308d5bec122a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150034"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a>Msvm Synthetic3DService 類別的 DisableGPUForVirtualization 方法 \_

停用實體 GPU 以進行虛擬化。

## <a name="syntax"></a>語法


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PhysicalGPU* \[在\]
</dt> <dd>

代表要停用之實體 GPU 的 [**Msvm \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) 類別實例的參考。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ Synthetic3DService**](msvm-synthetic3dservice.md)
</dt> </dl>

 

