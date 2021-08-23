---
description: 重設虛擬裝置。
ms.assetid: e4eb3952-a58e-4acd-85df-205d6ed23133
title: Msvm_EmulatedEthernetPort 類別的 Reset 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1860738c08ad5711a610e76b17d2e19e7d062d67501d17ecfbc74de8e0f1117e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525038"
---
# <a name="reset-method-of-the-msvm_emulatedethernetport-class"></a>Msvm EmulatedEthernetPort 類別的 Reset 方法 \_

重設虛擬裝置。

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

[**Msvm \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md)
</dt> </dl>

 

 




