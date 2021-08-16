---
title: IWMPCdromBurn burnProgress 屬性
description: BurnProgress 屬性會取得完成百分比的 CD 燒錄進度。
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- burnProgress 屬性 Windows Media Player
- burnProgress 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，burnProgress 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b8e468bc57bb40d990c0b2aeaffc23e184ef2ffa04ab85c9f60cf0d6bced57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332062"
---
# <a name="iwmpcdromburnburnprogress-property"></a>IWMPCdromBurn：： burnProgress 屬性

**BurnProgress** 屬性會取得完成百分比的 CD 燒錄進度。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a>屬性值

作為進度值的 **system.object** 。 進度值的範圍是從0到100。

## <a name="remarks"></a>備註

進度值代表整個燒錄流程的完成百分比，包括任何預備作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11<br/>                                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





