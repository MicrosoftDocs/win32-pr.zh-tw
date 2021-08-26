---
description: UOPValid 方法會抓取值，指出指定的使用者作業 (UOP) 目前是否有效。
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: 'UOPValid 方法 (區段 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078668"
---
# <a name="uopvalid-method"></a>UOPValid 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`UOPValid`方法會抓取值，指出指定的使用者作業 (UOP) 目前是否有效。

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

指定使用者作業 (UOP) 為整數。



| 值 | 描述                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md)、 [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**停止**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md)、 [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [](showmenu-method.md)參數值為 2 (DVD \_ 功能表標題的 ShowMenu \_)                                                                                                                                        |
| 11    | [](showmenu-method.md)參數值為 3 (DVD \_ 功能表 \_ 根目錄) 的 ShowMenu                                                                                                                                        |
| 12    | [](showmenu-method.md)參數值為 4 (DVD \_ 功能表子圖片的 ShowMenu \_)                                                                                                                                   |
| 13    | [](showmenu-method.md)參數值為 5 (DVD \_ 功能表 \_ 音訊) 的 ShowMenu                                                                                                                                       |
| 14    | [](showmenu-method.md)參數值為 6 (DVD \_ 功能表角度的 ShowMenu \_)                                                                                                                                        |
| 15    | [](showmenu-method.md)參數值為 7 (DVD \_ 功能表章節的 ShowMenu \_)                                                                                                                                      |
| 16    | [**繼續**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md)、 [**SelectRightButton**](selectrightbutton-method.md)、 [**SelectUpperButton**](selectupperbutton-method.md)、 [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**暫停**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md)、 [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | 選取影片模式喜好設定。                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回布林值，指出 UOP 控制項是否允許指定的作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>區段。h</dt> </dl> |



 

 




