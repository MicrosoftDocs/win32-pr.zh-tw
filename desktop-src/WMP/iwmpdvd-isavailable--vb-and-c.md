---
title: 'IWMPDVD. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法會取得值，這個值表示指定的資訊類型是否可用或是否可以執行指定的動作。
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999640"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD. isAvailable (VB 和 c # ) 

**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>參數

*bstrItem*

System.string，這是下列其中一個值。



| 值      | 描述                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| 上一步       | 探索 **IWMPDVD** 的方法是否可用。                                   |
| Dvd        | 探索是否已載入 DVD。                                                          |
| dvdDecoder | 探索系統上是否已安裝 DVD 解碼器。                                     |
| resume     | 探索 IWMPDVD 的 **resume** 方法是否可用。                                 |
| titleMenu  | 探索 **IWMPDVD. titleMenu** 方法是否可用。                              |
| topMenu    | 探索 **IWMPDVD. topMenu** 方法是否可用。 通常稱為根功能表。 |



 

## <a name="property-value"></a>屬性值

**System.Boolean**

**布林值**，指出指定的資訊類型是否可用，或是否可以執行指定的動作。

## <a name="remarks"></a>備註

Windows Media Player 的 DVD 功能將無法在未安裝 DVD 解碼器的電腦上運作。 您可以在 c ) # 中呼叫 **isAvailable** 屬性 (**get \_ isAvailable** 方法，並傳入 **system.string** 值 "dvdDecoder" 來判斷是否有可用的解碼器。

每個 DVD 的撰寫方式不同。 DVD 播放和流覽期間可用的方法取決於 DVD 的編寫方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPDVD 介面 (VB 和 c # )**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. back (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD 繼續 (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. topMenu (VB 和 c # )**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





