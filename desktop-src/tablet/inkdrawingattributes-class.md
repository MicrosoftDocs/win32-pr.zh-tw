---
description: 代表繪製時要套用至筆墨的屬性。
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: 'InkDrawingAttributes 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320139"
---
# <a name="inkdrawingattributes-class"></a>InkDrawingAttributes 類別

代表繪製時要套用至筆墨的屬性。

**InkDrawingAttributes** 具有下列類型的成員：

-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="interfaces"></a>介面

**InkDrawingAttributes** 類別會定義這些介面。



| 介面                 | 描述                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkDrawingAttributes** | 這個物件會實 **IInkDrawingAttributes** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkDrawingAttributes** 類別有這些方法。



| 方法                         | 描述                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**克隆**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | 建立重複的 [**InkDisp**](inkdisp-class.md)、 **InkDrawingAttributes** 或 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件。<br/> |



 

### <a name="properties"></a>屬性

**InkDrawingAttributes** 類別具有這些屬性。



| 屬性                                                                           | 存取類型           | Description                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**效果**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | 讀取/寫入<br/> | 取得或設定值，這個值會指定沿著筆墨邊緣的前景和背景色彩是否經過混合，以增加筆墨筆劃的平滑。<br/> |
| [**色彩**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | 讀取/寫入<br/> | 取得或設定使用這個 **InkDrawingAttributes** 物件繪製的筆墨色彩。<br/>                                                                                    |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | 唯讀<br/>  | 取得儲存在 **InkDrawingAttributes** 物件中之應用程式定義資料的集合。<br/>                                                                |
| [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | 讀取/寫入<br/> | 取得或設定值，這個值會指定是否將筆墨轉譯為一連串的曲線，而不是畫筆取樣點之間的線條。<br/>                                    |
| [**高度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | 讀取/寫入<br/> | 取得或設定使用這個 **InkDrawingAttributes** 物件繪製筆墨時，畫筆的高度。<br/>                                                                        |
| [**IgnorePressure**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | 讀取/寫入<br/> | 取得或設定值，這個值會指定是否會在 tablet 介面上增加畫筆提示的壓力，以自動放大繪圖筆墨。<br/>                     |
| [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | 讀取/寫入<br/> | 取得或設定在使用這個 **InkDrawingAttributes** 物件繪製筆墨時，要使用 (球或矩形) 的畫筆提示。<br/>                                                       |
| [**RasterOperation**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | 讀取/寫入<br/> | 取得或設定畫筆色彩如何在繪製筆墨時，與顯示上現有的背景色彩互動。<br/>                                                    |
| [**透明度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | 讀取/寫入<br/> | 取得或設定繪製筆墨的透明度值。 值的範圍從零 (完全不透明) 至 255 (完全透明) 。<br/>                                               |
| [**寬度**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | 讀取/寫入<br/> | 取得或設定使用這個 **InkDrawingAttributes** 物件繪製筆墨時畫筆的寬度。<br/>                                                                         |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

這些繪圖屬性可以與筆劃或游標相關聯，並指定色彩、寬度和透明度等設定。

若要指定筆劃的繪圖屬性，請使用 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)屬性。 若要指定筆劃集合內所有筆劃的繪製屬性，請呼叫 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合的 [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)方法。

每個 [**InkCollector**](inkcollector-class.md) 物件、 [**InkOverlay**](inkoverlay-class.md) 物件和 [InkPicture](inkpicture-control-reference.md) 控制項都可以針對相同的資料指標指定一組不同的繪圖屬性。 您可以使用 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件的 [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)屬性來取得或設定資料指標的繪製屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DrawingAttributes 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

**DrawingAttributes 屬性**
</dt> <dt>

**DrawingAttributes 屬性**
</dt> <dt>

[**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**
</dt> <dt>

**System.windows.controls.inkcanvas.defaultdrawingattributes 屬性**
</dt> <dt>

[**ModifyDrawingAttributes 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**InkDisp 類別**](inkdisp-class.md)
</dt> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

