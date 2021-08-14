---
title: IWMPMedia2 Error 屬性
description: 如果媒體專案有錯誤條件，錯誤屬性會取得 IWMPErrorItem 介面。
ms.assetid: 57dc8aef-5f22-43da-87bc-fdc0c8ebe49b
keywords:
- Error 屬性 Windows Media Player
- Error 屬性 Windows Media Player，IWMPMedia2 介面
- IWMPMedia2 介面 Windows Media Player，Error 屬性
topic_type:
- apiref
api_name:
- IWMPMedia2.Error
- IWMPMedia2.get_Error
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c841e52f2a5adda5a2098f591b141aa334ee5138c1a5cc7d6eff9b54dca5e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331968"
---
# <a name="iwmpmedia2error-property"></a>IWMPMedia2：： Error 屬性

如果媒體專案有錯誤條件， **錯誤** 屬性會取得 **IWMPErrorItem** 介面。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public IWMPErrorItem Error {get;}
```


```VB

Public ReadOnly Property Error As IWMPErrorItem
```





## <a name="property-value"></a>屬性值

**WMPLib IWMPErrorItem** 介面，可讓您存取錯誤狀況的相關資訊。

## <a name="remarks"></a>備註

如果無法播放媒體專案，這個屬性會取得 **IWMPErrorItem** 介面，其中包含所發生問題的相關資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPErrorItem (VB 和 c # )**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPMedia2 介面 (VB 和 c # )**](iwmpmedia2--vb-and-c.md)
</dt> </dl>

 

 





