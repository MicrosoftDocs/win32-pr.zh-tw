---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: 07408bce-88c7-43ef-b437-7b2ce37fca91
title: PathIterator 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfe78e422873ff65bf1908ba766723b61843661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972153"
---
# <a name="pathiterator-functions"></a>PathIterator 函式

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**GraphicsPathIterator**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator) c + + 類別包裝。

## <a name="graphicspathiterator-functions-and-corresponding-wrapper-methods"></a>GraphicsPathIterator 函式和對應的包裝函式方法



| 一般函數                                                                                                                                                    | 包裝函式方法                                                                                                                                                                                                     | 備註                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreatePathIter (GpPathIterator \* \* Iterator，GpPath \* path) <br/>                                                                    | [**GraphicsPathIterator：： GraphicsPathIterator (在 const GraphicsPath \* path)**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspathiterator-graphicspathiterator(constgraphicspathiterator_))<br/>                                                      | 建立新的 [**GraphicsPathIterator**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator) 物件，並將其與 GraphicsPath 物件建立關聯。                                    |
| GpStatus WINGDIPAPI GdipDeletePathIter (GpPathIterator \* iterator) <br/>                                                                                     | GraphicsPathIterator：： ~ GraphicsPathIterator ()  <br/>                                                                                                                                                          | 釋放 [**GraphicsPathIterator**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator) 物件所使用的資源。                                                                |
| GpStatus WINGDIPAPI GdipPathIterNextSubpath (GpPathIterator \* iterator、int \* RESULTCOUNT、int \* startIndex、INT \* endIndex、BOOL \* isClosed) <br/>          | [**INT GraphicsPathIterator：： NextSubpath (OUT INT \* startIndex、OUT INT \* ENDINDEX、OUT BOOL \* isClosed)**](/previous-versions//ms535463(v=vs.85))<br/>           | 取得下一個子路徑的開始索引和結束索引 (圖) 在此反覆運算器的關聯路徑中。                                                                   |
| GpStatus WINGDIPAPI GdipPathIterNextSubpathPath (GpPathIterator \* iterator、INT \* ResultCount、GpPath \* path、BOOL \* isClosed) <br/>                         | [**INT GraphicsPathIterator：： NextSubpath (OUT const GraphicsPath \* path，OUT BOOL \* isClosed)**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextsubpath(outconstgraphicspath_outbool))<br/>                                     | Getsthe 下圖 (從此 iterator 相關路徑) 的子路徑。                                                                                                             |
| GpStatus WINGDIPAPI GdipPathIterNextPathType (GpPathIterator \* iterator、int \* RESULTCOUNT、BYTE \* pathType、INT \* startIndex、int \* endIndex) <br/>         | [**INT GraphicsPathIterator：： NextPathType (OUT BYTE \* pathType、OUT int \* STARTINDEX、out INT \* endIndex)**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-nextpathtype)<br/>         | 取得具有相同型別之資料點的下一個群組之開始索引和結束索引。                                                                      |
| GpStatus WINGDIPAPI GdipPathIterNextMarker (GpPathIterator \* iterator、int \* RESULTCOUNT、int \* startIndex、int \* endIndex) <br/>                            | [**INT GraphicsPathIterator：： NextMarker (OUT INT \* startIndex、OUT INT \* endIndex)**](/previous-versions//ms535465(v=vs.85))<br/>                                           | 取得此反覆運算器的關聯路徑中，下一個標記分隔區段的開始索引和結束索引。                                                           |
| GpStatus WINGDIPAPI GdipPathIterNextMarkerPath (GpPathIterator \* iterator、INT \* ResultCount、GpPath \* path) <br/>                                           | [**INT GraphicsPathIterator：： NextMarker (OUT const GraphicsPath \* path)**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspathiterator-nextmarker(outconstgraphicspath))<br/>                                                                     | 取得此 iterator 相關路徑的下一個標記分隔區段。                                                                                                      |
| GpStatus WINGDIPAPI GdipPathIterGetCount (GpPathIterator \* iterator，INT \* count) <br/>                                                                      | [**INT GraphicsPathIterator：： GetCount () const**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-getcount)<br/>                                                                                                     | 傳回路徑中的資料點數目。                                                                                                                                  |
| GpStatus WINGDIPAPI GdipPathIterGetSubpathCount (GpPathIterator \* iterator，INT \* count) <br/>                                                               | [**INT GraphicsPathIterator：： GetSubpathCount () const**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-getsubpathcount)<br/>                                                                                       | 傳回路徑中 (也稱為「圖形) 的子路徑數目。                                                                                                               |
| GpStatus WINGDIPAPI GdipPathIterIsValid (GpPathIterator \* iterator，BOOL \* 有效) <br/>                                                                      | 未由包裝函式方法呼叫。<br/>                                                                                                                                                                          | 此函數會傳遞布林值，指出 *iterator* 參數所指定的路徑反覆運算器是否有效。 Output 參數 *valid* 會接收結果。 |
| GpStatus WINGDIPAPI GdipPathIterHasCurve (GpPathIterator \* iterator，BOOL \* hasCurve) <br/>                                                                  | [**BOOL GraphicsPathIterator：： HasCurve () const**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-hascurve)<br/>                                                                                                    | 判斷路徑是否有任何曲線。                                                                                                                                     |
| GpStatus WINGDIPAPI GdipPathIterRewind (GpPathIterator \* iterator) <br/>                                                                                     | [**VOID GraphicsPathIterator：：倒轉 ()**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-rewind)<br/>                                                                                                              | 將此反覆運算器倒轉至其關聯路徑的開頭。                                                                                                                  |
| GpStatus WINGDIPAPI GdipPathIterEnumerate (GpPathIterator \* iterator、INT \* ResultCount、GpPointF \* points、BYTE \* types、INT count) <br/>                   | [**INT GraphicsPathIterator：：列舉 (OUT PointF \* 點、OUT BYTE \* 類型、IN INT count)**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-enumerate)<br/>                                   | 將路徑的資料點複製到 [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) 陣列，並將路徑的點類型複製到 **位元組** 陣列。                                   |
| GpStatus WINGDIPAPI GdipPathIterCopyData (GpPathIterator \* iterator、INT \* ResultCount、GpPointF \* points、BYTE \* types、Int startIndex、int endIndex) <br/> | [**Int GraphicsPathIterator：： CopyData (OUT PointF \* points，OUT BYTE \* TYPES In INT STARTINDEX In int endIndex)**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspathiterator-copydata)<br/> | 將路徑的資料點子集複製到 PointF 陣列，並將路徑的點類型子集複製到 **位元組** 陣列。                                                  |



 

 

 
