---
title: IWMPCdromBurn 標籤屬性
description: Label 屬性會取得 CD 磁片區標籤字串。
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- label 屬性 Windows Media Player
- label 屬性 Windows Media Player，IWMPCdromBurn 介面
- IWMPCdromBurn 介面 Windows Media Player，label 屬性
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001592"
---
# <a name="iwmpcdromburnlabel-property"></a>IWMPCdromBurn：： label 屬性

*Label* 屬性會取得 CD 磁片區標籤字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a>屬性值

表示磁片區標籤字串的 **system.string** 。

## <a name="remarks"></a>備註

由於 CD 標籤的儲存方式，CD 的標籤可能會比指定的磁片區標籤字串的長度還要短。 如果字串的長度超過 CD 標籤的最大長度，則會將文字截斷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromBurn 介面 (VB 和 c # )**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





