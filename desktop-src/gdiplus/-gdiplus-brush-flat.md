---
description: Windows GDI+ 會公開由大約600個函式所組成的一般 API。 這些一般 API 函式是由筆刷 c + + 類別包裝。
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: '筆刷函數 (GDI+) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afdec5667dfcfe4b83e54af3fc0b88fcef991494e36f1e4788062029d1d6e29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888338"
---
# <a name="brush-functions-gdi"></a>筆刷函數 (GDI+) 

Windows GDI+ 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI+ 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您對 GDI+ 進行呼叫時，您應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱[GDI+ 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) c + + 類別包裝。

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>筆刷函數和對應的包裝函式方法



| 一般函數                                                                        | 包裝函式方法                                          | 描述                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* 筆刷，GpBrush \* \* cloneBrush)           | [**筆刷：： Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | [**Brush：： Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)方法會根據此筆刷建立新的 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)物件。 |
| GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* 筆刷)                                  | 虛擬 ~ 筆刷 ()                                         | 清除 [**筆刷**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) 物件所使用的資源。                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* 筆刷，GpBrushType \* 類型) <br/> | [**筆刷：： GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | [**Brush：： GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype)方法會取得此筆刷的型別。                                                      |



 

 

 




