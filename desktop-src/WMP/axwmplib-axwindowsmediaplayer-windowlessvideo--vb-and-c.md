---
title: AxWindowsMediaPlayer. windowlessVideo 屬性
description: WindowlessVideo 屬性會取得或設定值，這個值表示 Windows Media Player 控制項是否以無視窗模式呈現影片。
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessVideo 屬性 Windows Media Player
- windowlessVideo 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，windowlessVideo 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996107"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>AxWindowsMediaPlayer. windowlessVideo 屬性

WindowlessVideo 屬性會取得或設定值，這個值表示 Windows Media Player 控制項是否以無視窗模式呈現影片。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>屬性值

System.string 值，指出 Windows Media Player 控制項是否以無視窗模式呈現影片。 預設值為 false。

## <a name="remarks"></a>備註

根據預設，內嵌的 Windows Media Player 控制項會在用戶端區域內的它自己的視窗中呈現影片。 當 **windowlessVideo** 設定為 true 時，Windows Media Player 物件會直接在工作區中轉譯影片，因此您可以套用特殊效果或以文字將影片分層。

在 Windows Vista 中，以無視窗模式轉譯影片可能會降低效能。

Netscape Navigator 不支援取得這個屬性的值。 在 Netscape Navigator 中設定這個屬性的值可能會產生非預期的結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





