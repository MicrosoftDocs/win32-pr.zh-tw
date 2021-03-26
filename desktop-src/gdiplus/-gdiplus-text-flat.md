---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: 70d35c08-08d9-46a6-a6df-76d989551866
title: 文字函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36890179a975c35e2f09aaeecaec0d9f0e5844a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972837"
---
# <a name="text-functions"></a>文字函數

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。 下列一般 API 函式是由 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 文字 c + + 類別所包裝。

## <a name="text-functions-and-corresponding-wrapper-methods"></a>文字函數和對應的包裝函式方法



| 一般函數                                                                                                                                                                                                                                                                   | 包裝函式方法                                                                                                                                                                                                                                                                                                                                                                        | 備註                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipDrawString ( GpGraphics \* graphics、GDIPCONST WCHAR \* STRING、INT LENGTH、GDIPCONST GpFont \* Font-family、GDIPCONST RECTF \* layoutRect、GDIPCONST GpStringFormat \* stringFormat、GDIPCONST GpBrush \* 筆刷 ) <br/>                                         | [**狀態圖形： const WCHAR string 中的:D rawString ( （以 const 字型格式）（以 const 字型字型而言），在 const \* \* RectF &layoutRect 中，const StringFormat StringFormat 的 Const \* 筆刷 \* 筆刷 )**](/previous-versions//ms535991(v=vs.85))<br/>                                                                                      | 根據字型、版面配置矩形和格式繪製字串。                                                                                                                                                 |
| GpStatus WINGDIPAPI GdipMeasureString ( GpGraphics \* graphics、GDIPCONST WCHAR \* STRING、INT LENGTH、GDIPCONST GpFont \* Font-family、GDIPCONST RECTF \* layoutRect、GDIPCONST GpStringFormat \* STRINGFORMAT、RectF \* boundingBox、int \* codepointsFitted、int \* linesFilled ) <br/> | [**狀態圖形：： MeasureString ( IN const WCHAR \* string，INT length，Const font-family，in Const \* RectF &layoutRect，const StringFormat \* StringFormat，out RECTF \* boundingBox，out int \* CODEPOINTSFITTED = 0，out int \* linesFilled = 0 ) const**](/previous-versions//ms535831(v=vs.85))<br/> | 以指定的字型、格式和版面配置矩形來測量字串的範圍。                                                                                                                            |
| GpStatus WINGDIPAPI GdipMeasureCharacterRanges ( GpGraphics \* graphics、GDIPCONST WCHAR \* STRING、INT LENGTH、GDIPCONST GpFont \* Font-family、GDIPCONST RectF &LayoutRect、GDIPCONST GPSTRINGFORMAT \* stringFormat、INT regionCount、GpRegion \* \* 區域 ) <br/>                  | [**狀態圖形：： MeasureCharacterRanges ( IN const WCHAR \* string （int length） in Const font-family，in Const \* RectF &layoutRect，const StringFormat \* STRINGFORMAT，in INT RegionCount，OUT Region Region \* ) const**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges)<br/>                                  | 取得一組區域，其中每個區域都會將字串內的字元位置範圍界限。                                                                                                                        |
| GpStatus WINGDIPAPI GdipDrawDriverString ( GpGraphics \* graphics、GDIPCONST UINT16 \* TEXT、INT LENGTH、GDIPCONST GpFont \* Font-family、GDIPCONST GpBrush \* 筆刷、GDIPCONST PointF \* 位置、INT flags、GDIPCONST GpMatrix \* matrix ) <br/>                                     | [**狀態圖形：:D rawDriverString ( const UINT16 文字（以 INT 長度為限），在 const 字型字型的 const 字型字型中，在 const \* \* PointF 位置的 const 位置中， \* \* INT 旗標的 const 矩陣 \* 矩陣 )**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawdriverstring)<br/>                                                                           | 在指定的位置繪製字元。 方法可讓用戶端完整控制文字的外觀。 方法會假設用戶端已經設定要套用的格式和配置。 |
| GpStatus WINGDIPAPI GdipMeasureDriverString ( GpGraphics \* graphics、GDIPCONST UINT16 \* TEXT、INT LENGTH、GDIPCONST GpFont \* Font-family、GDIPCONST POINTF \* 位置、INT flags、GDIPCONST GpMatrix \* matrix、RectF \* boundingBox ) <br/>                                        | [**狀態圖形：： MeasureDriverString ( IN const UINT16 \* text，int length，Const font-family，in Const \* PointF \* 位置，INT flags，in const MATRIX \* matrix，OUT RectF \* boundingBox ) const**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-measuredriverstring)<br/>                                                        | 測量指定字元及其對應位置的周框方塊。                                                                                                                         |



 

 

 
