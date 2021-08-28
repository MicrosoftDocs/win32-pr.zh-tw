---
title: 'IWMPMedia. isIdentical (VB 和 C ) '
description: IsIdentical 屬性 (\_ 在 C \ ) 的 get isIdentical 方法取得值，指出指定的媒體專案是否與目前的媒體專案相同。
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003578"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia. isIdentical (VB 和 c # ) 

**IsIdentical** 屬性 (c # 中的 **get \_ isIdentical** 方法 ) 取得值，指出指定的媒體專案是否與目前的媒體專案相同。


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>參數

*pIWMPMedia*

要與目前媒體專案比較之媒體專案的 **WMPLib IWMPMedia** 介面。

## <a name="property-value"></a>屬性值

表示兩個媒體專案是否相同的 **布林** 值。

## <a name="remarks"></a>備註

**IWMPMedia. isIdentical** 是 Visual Basic 中接受參數的屬性。 在 c # 中，它稱為 **IWMPMedia. get \_ isIdentical** 方法。

## <a name="examples"></a>範例

下列範例會使用 **isIdentical** 屬性 (c # 中的 **get \_ isIdentical** 方法 ) 檢查名為 newMedia 的媒體專案是否與目前的媒體專案相同。 如果兩者不同，則會播放新的媒體專案。 否則，目前的媒體會繼續播放不中斷的。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

End If
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





