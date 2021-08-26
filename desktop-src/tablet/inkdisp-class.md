---
description: InkDisp 類別-表示筆墨空間內所收集的筆墨筆劃。
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: 'InkDisp 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 928bda8af246b41bab2c285a5292155917ba8903c6dd71c20177dbf906c64924
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939158"
---
# <a name="inkdisp-class"></a>InkDisp 類別

表示筆墨空間內所收集的筆墨筆劃。

**InkDisp** 具有下列類型的成員：

-   [事件](#events)
-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="events"></a>事件

**InkDisp** 類別具有這些事件。



| 事件                                    | 描述                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [**InkAdded**](inkdisp-inkadded.md)     | 在將筆劃加入至 **InkDisp** 物件時發生。<br/>     |
| [**InkDeleted**](inkdisp-inkdeleted.md) | 從 **InkDisp** 物件中刪除筆劃時發生。<br/> |



 

### <a name="interfaces"></a>介面

**InkDisp** 類別會定義這些介面。



| 介面    | 描述                                                       |
|:-------------|:------------------------------------------------------------------|
| **IInkDisp** | 這個物件會實 **IInkDisp** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkDisp** 類別有這些方法。



| 方法                                                                   | 描述                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddStrokesAtRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | 將筆劃集合插入 **InkDisp** 物件中指定的矩形。<br/>                                                                                                       |
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | 指出 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) 是否可轉換為 **InkDisp** 物件。<br/>                                                                                       |
| [**剪輯**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | 移除矩形外筆劃或筆劃集合的部分。<br/>                                                                                                       |
| [**ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | 將 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合複製到剪貼簿。<br/>                                                                                                           |
| [**ClipboardCopyWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | 將已知矩形內所包含的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件複製到剪貼簿。<br/>                                                               |
| [**ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | 將 [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) 從剪貼簿複製到 **InkDisp** 物件。<br/>                                                                                               |
| [**複製**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | 建立重複的 **InkDisp** 物件。<br/>                                                                                                                                                   |
| [**CreateStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | 從點或封包資料建立筆劃。<br/>                                                                                                                                              |
| [**CreateStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | 建立這個 **InkDisp** 物件的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。<br/>                                                                                                |
| [**DeleteStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | 從 **InkDisp** 物件中刪除筆劃。<br/>                                                                                                                                             |
| [**DeleteStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | 從 **InkDisp** 物件中刪除筆劃。<br/>                                                                                                                                              |
| [**ExtractStrokes 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | 從 **InkDisp** 物件中解壓縮筆劃，並傳回新的 **InkDisp** 物件，其中包含已解壓縮的筆劃。<br/>                                                                       |
| [**ExtractWithRectangle 方法**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | 從現有的 **InkDisp 類別** 物件剪下或複製筆劃，然後將其貼入新的 **InkDisp 類別** 物件，方法是使用已知的矩形來判斷要解壓縮哪些筆觸。<br/> |
| [**GetBoundingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | 抓取 **InkDisp** 物件中所有筆劃的周框方塊。<br/>                                                                                                               |
| [**HitTestCircle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | 抓取完全在已知圓形內部或交集的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。<br/>                                                  |
| [**HitTestWithLasso**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | 抓取折線選取區域內的筆觸。<br/>                                                                                                                                   |
| [**HitTestWithRectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | 抓取指定矩形內所包含的筆劃。<br/>                                                                                                                    |
| [**載入**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | 使用已知的二進位資料填入新的 **InkDisp** 物件。<br/>                                                                                                                                |
| [**NearestPoint**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | 抓取最接近已知點之 **InkDisp** 物件內的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ，並選擇性地提供其他資訊。<br/>                       |
| [**儲存**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | 將筆墨轉換成指定的格式，並傳回二進位資料。<br/>                                                                                                                       |



 

### <a name="properties"></a>屬性

**InkDisp** 類別具有這些屬性。



| 屬性                                                                           | 存取類型           | 描述                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | 唯讀<br/>  | 取得要與筆墨一起保存的 [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) 集合。<br/>                             |
| [**髒**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | 讀取/寫入<br/> | 取得或設定值，這個值會指出自上一次儲存筆墨之後， **InkDisp** 物件是否已修改。<br/> |
| [**ExtendedProperties**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | 唯讀<br/>  | 取得應用程式定義資料的集合。<br/>                                                                             |
| [**中風**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | 唯讀<br/>  | 取得 **InkDisp** 物件中所包含的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。<br/>                             |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

> [!Note]  
> 這個物件的第一個具現化會導致 GDI+ 也會具現化。 副作用是，如果您在迴圈中使用單一筆墨物件，並在迴圈中建立和終結它，您將會導致 GDI+ 的具現化。 這可能會導致應用程式效能降低。 若要避免這種情況，請在應用程式使用筆墨時隨時保留筆墨物件的單一實例。

 

**InkDisp** 物件是筆劃 (點) 資料的容器。 筆劃資料（或畫筆所收集的點）會放入 **InkDisp** 物件中。 [**筆劃**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)屬性包含 **InkDisp** 物件內所有筆劃的資料。

[**InkCollector**](inkcollector-class.md)物件、 [**InkOverlay**](inkoverlay-class.md)物件和 [InkPicture](inkpicture-control-reference.md)控制項會收集輸入裝置的點，並將它們放入 **InkDisp** 物件中。 這些物件基本上是做為將筆墨分配至一或多個不同 **InkDisp** 物件的來源，這些物件可作為保存分散式筆墨的容器。

筆墨空間是 tablet 內容座標所對應的虛擬座標空間。 此空間已固定為 HIMETRIC 座標系統。 在筆墨空間座標中，從0到1的移動等於1個 HIMETRIC 單位。 此對應可讓您輕鬆地建立多個 **InkDisp** 物件的關聯。

[**InkRenderer**](inkrenderer-class.md)物件會管理筆墨與顯示視窗之間的對應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                           |
| 標頭<br/>                   | <dl> <dt>Msinkaut (也需要 Msinkaut \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkStrokeDisp 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**IInkTablet 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

