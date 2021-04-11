---
description: 表示從筆墨到顯示視窗的對應管理。 使用 InkRenderer 物件在視窗中顯示筆墨。 您也可以使用它來調整筆劃的位置並調整其大小。
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: 'InkRenderer 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195321"
---
# <a name="inkrenderer-class"></a>InkRenderer 類別

表示從筆墨到顯示視窗的對應管理。 使用 **InkRenderer** 物件在視窗中顯示筆墨。 您也可以使用它來調整筆劃的位置並調整其大小。

**InkRenderer** 具有下列類型的成員：

-   [介面](#interfaces)
-   [方法](#methods)

### <a name="interfaces"></a>介面

**InkRenderer** 類別會定義這些介面。



| 介面        | 描述                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkRenderer** | 這個物件會實 **IInkRenderer** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkRenderer** 類別有這些方法。



| 方法                                                                     | 描述                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | 在裝置內容上繪製筆觸。<br/>                                                                                                            |
| [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | 在指定的 windows 裝置內容上繪製筆劃。<br/>                                                                                       |
| [**GetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | 抓取用來呈現筆墨的物件轉換。<br/>                                                                                   |
| [**GetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | 抓取用來呈現筆墨的視圖轉換。<br/>                                                                                      |
| [**InkSpaceToPixel**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | 將筆墨空間座標中的位置轉換成圖元空間。<br/>                                                                            |
| [**InkSpaceToPixelFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | 將筆墨空間座標中的點陣列轉換成圖元空間。<br/>                                                                          |
| [**Measure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | 計算裝置內容上的矩形，如果它們是使用 **InkRenderer** 物件繪製，則會包含筆劃集合。<br/> |
| [**MeasureStroke**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | 計算裝置內容上的矩形，如果它們是使用 **InkRenderer** 物件繪製，則會包含筆劃。<br/>                |
| [**移動**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | 將翻譯套用至筆墨空間座標的視圖轉換。<br/>                                                                         |
| [**PixelToInkSpace**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | 將圖元座標中的位置轉換成筆墨空間。<br/>                                                                                  |
| [**PixelToInkSpaceFromPoints**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | 將圖元空間座標中的點陣列轉換成筆墨空間。<br/>                                                                          |
| [**旋轉**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | 將旋轉套用至視圖轉換。<br/>                                                                                                     |
| [**ScaleTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | 調整 X 和 Y 維度中的 view 轉換。<br/>                                                                                           |
| [**SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | 設定用來呈現筆墨的物件轉換。<br/>                                                                                         |
| [**SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | 設定用來呈現筆墨的視圖轉換。<br/>                                                                                           |



 

## <a name="remarks"></a>備註

也可以透過 **InkRenderer** 物件來進行列印。

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**轉譯器屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[**InkDrawingAttributes 類別**](inkdrawingattributes-class.md)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

