---
description: Windows GDI + 會公開由大約600函式組成的一般 API。 這些一般 API 函式是由 SolidBrush c + + 類別包裝。
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: SolidBrush 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395553"
---
# <a name="solidbrush-functions"></a>SolidBrush 函式

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議不要直接呼叫一般 API 中的函式。 每當您對 GDI + 進行呼叫時，我們建議您呼叫 c + + 包裝函式所提供的方法和函式來執行這項作業。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) c + + 類別包裝。

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>筆刷函數和對應的包裝函式方法



| 一般函數                                                                               | 包裝函式方法                                                                                       | 備註                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB 色彩、GpSolidFill \* \* 筆刷)**<br/>   | [**SolidBrush：： SolidBrush (const 色彩& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | 根據色彩建立 [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) 物件 |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* 筆刷，ARGB 色彩)**<br/>   | [**SolidBrush：： SetColor (const 色彩& Color)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | 設定此實心筆刷的色彩                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* 筆刷，ARGB \* 色彩)**<br/> | [**SolidBrush：： GetColor (OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | 取得這個實心筆刷的色彩                                                      |



 

 

 
