---
description: 如果影片的大小不符合輸出維度，這些旗標會指定如何轉譯影片來源。
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: '調整旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001120"
---
# <a name="resize-flags"></a>調整旗標

\[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

如果影片的大小不符合輸出維度，這些旗標會指定如何轉譯影片來源。



| 常數/值                                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_STRETCH**</dt> <dt>0</dt> </dl>                                                                          | 影像會伸展以符合兩個維度中的目標框架大小，而不會保留長寬比。<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_裁剪**</dt> <dt>1</dt> </dl>                                                                                   | 影像未調整大小。 如果影像小於目標框架，周圍區域會是黑色。 如果影像大於目標框架，則會裁剪影像。<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | 影像會調整大小以配合一個維度的目標框架，同時保留外觀比例。 如果影像中的寬度和高度比例與目標框架中的比率不符，則會建立黑邊。<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | 影像會調整大小以填滿整個目標框架，同時保留外觀比例。 這個模式不會建立黑邊，而是沿著兩側或在頂端和底部裁剪影像。<br/>                 |



## <a name="remarks"></a>備註

下列影像顯示這些旗標的效果。

![調整旗標](images/stretch14.png)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




