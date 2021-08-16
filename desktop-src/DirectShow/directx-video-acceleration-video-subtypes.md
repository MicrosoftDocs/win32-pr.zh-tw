---
description: 使用 DirectX Video 加速 (DXVA) 的解碼器會使用下列子類型。
ms.assetid: 031b076b-cdfa-407f-8efa-391bce3075ef
title: 'DirectX Video 加速影片子類型 (Dshow .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a2197d504929e001e07fb1ac107dbd7b13b1f443e43ec8ed90232372b08f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016146"
---
# <a name="directx-video-acceleration-video-subtypes"></a>DirectX Video 加速影片子類型

使用 DirectX Video 加速 (DXVA) 的解碼器會使用下列子類型。 AI44 和 IA44 是以每圖元的位元組值為8的表面。 有4個位的 I 和 4 *位。**I* 表示在16個專案的 YUV 調色板中的索引。 *代表 4* 位的透明資訊 (也稱為每圖元 Alpha) 。 因此，AI44 和 IA44 表面允許16種不同的透明度值，或256不同的圖元標記法。 使用 AI44 時，Alpha 會儲存在 hi 半形，在 IA44 中，Alpha 會儲存在 lo 位元組內。 這兩種格式對於 DVD 子圖片和 Line21 與 Teletext 影像都很有用。 Microsoft 偏好使用 AI44 版本，因為使用此格式可讓您更輕鬆地產生文字。

| Subtype            | 描述                                                 |
|--------------------|-------------------------------------------------------------|
| MEDIASUBTYPE \_ AI44 | 適用于子圖片和文字覆迭。 請參閱先前的描述。 |
| MEDIASUBTYPE \_ IA44 | 適用于子圖片和文字覆迭。 請參閱先前的描述。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片子類型](video-subtypes.md)
</dt> </dl>

 

 




