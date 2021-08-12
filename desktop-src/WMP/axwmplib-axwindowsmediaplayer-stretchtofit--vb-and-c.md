---
title: AxWindowsMediaPlayer. stretchToFit 屬性
description: stretchToFit 屬性會取得或設定值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- stretchToFit 屬性 Windows Media Player
- stretchToFit 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，stretchToFit 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3090889207e0631fbc2f35613398b4c979f4c907cfe240e9f0a7374c74b00b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581508"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>AxWindowsMediaPlayer. stretchToFit 屬性

stretchToFit 屬性會取得或設定值，指出當影片視窗大於影片影像的尺寸時，Windows Media Player 控制項所顯示的影片是否會自動調整大小以符合影片視窗。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>屬性值

System.string 值，指出影片是否將延展以符合視窗。 預設值為 false。

## <a name="remarks"></a>備註

當 **stretchToFit** 設定為 true 時，Windows Media Player 控制項會維持影片的原始外觀比例。 如果影片的長寬比與影片視窗的外觀比例不相符，則可能會在影片影像的頂端和底部或左邊和右邊出現黑色遮罩區域。

這個屬性只適用于內嵌在網頁中的 Windows Media Player 控制項。

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

 

 





