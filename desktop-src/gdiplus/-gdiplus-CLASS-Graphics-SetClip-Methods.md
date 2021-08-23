---
description: 本主題列出 Graphics 類別的 SetClip 方法。 如需圖形類別之方法的完整清單，請參閱圖形。
ms.assetid: e8348373-da79-4d33-8bea-d594985493d4
title: SetClip 方法
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 616a78aa7dd251e888bba1186a3583c5d7f62d188dcc6313560f651ec6558827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037186"
---
# <a name="graphicssetclip-methods"></a>SetClip 方法

本主題列出 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 類別的 SetClip 方法。 如需 **圖形** 類別之方法的完整清單，請參閱 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetClip (HRGN、CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))                     | [**Graphics：： SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inhrgn_incombinemode))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為本身與 GDI 區域組合的區域。<br/>                                                                                                                                                                                                          |
| [**SetClip (Rect&、CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))   | [**Graphics：： SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrect__incombinemode))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為本身與矩形組合的區域。<br/>                                                                                                                                                                                          |
| [**SetClip (RectF&、CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode)) | [**Graphics：： SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstrectf__incombinemode))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為本身與矩形組合的區域。<br/>                                                                                                                                                                                         |
| [**SetClip (Region \* ，CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))               | [**Graphics：： SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為其本身和區域物件所指定 [**之區域組合**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region)的區域。<br/>                                                                                                                                      |
| [**SetClip (Graphics \* ，CombineMode)**](/previous-versions//ms535823(v=vs.85))                  | [**Graphics：： SetClip**](/previous-versions//ms535823(v=vs.85))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為本身與另一個 **圖形** 物件裁剪區域組合的區域。<br/>                                                                                                                                                                       |
| [**SetClip (GraphicsPath \* 、CombineMode)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))           | [**Graphics：： SetClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstgraphicspath_incombinemode))方法會將這個 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的裁剪區域更新為本身與圖形路徑所指定之區域組合的區域。 如果路徑中的圖未封閉，則此方法會將非封閉圖視為連接圖形起始點和結束點的直線封閉。<br/> |



 

 
