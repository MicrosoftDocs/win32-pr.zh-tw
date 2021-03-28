---
description: Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。
ms.assetid: c7d9e633-8c3d-4e77-811d-306cd785a7ad
title: HatchBrush 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d444fea500ce1e56e4c59420b913d5ff6cee965c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991334"
---
# <a name="hatchbrush-functions"></a>HatchBrush 函式

Windows GDI + 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI + 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您呼叫 GDI + 時，您都應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱 [Gdi + 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) c + + 類別包裝。

## <a name="hatchbrush-functions-and-corresponding-wrapper-methods"></a>HatchBrush 函式和對應的包裝函式方法



| 一般函數                                                                                                               | 包裝函式方法                                                                                                                                                                                   | 備註                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateHatchBrush (GpHatchStyle hatchstyle、ARGB forecol、ARGB backcol、GpHatch \* \* 筆刷) <br/> | [**HatchBrush：： HatchBrush (IN HatchStyle hatchStyle、const Color& 前景、const 色彩& 背景色 = Color () )**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-hatchbrush-hatchbrush(consthatchbrush_)) | 根據影線樣式、前景色彩和背景色彩來建立 [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) 物件。 |
| GpStatus WINGDIPAPI GdipGetHatchStyle (GpHatch \* 筆刷，GpHatchStyle \* hatchstyle) <br/>                                | [**HatchStyle HatchBrush：： GetHatchStyle () const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-gethatchstyle)                                                                                                 | 取得此影線筆刷的影線類型。                                                                                                  |
| GpStatus WINGDIPAPI GdipGetHatchForegroundColor (GpHatch \* 筆刷，ARGB \* forecol) <br/>                                 | [**Status HatchBrush：： GetForegroundColor (OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getforegroundcolor)                                                                    | 取得此影線筆刷的前景色彩。                                                                                             |
| GpStatus WINGDIPAPI GdipGetHatchBackgroundColor (GpHatch \* 筆刷，ARGB \* backcol) <br/>                                 | [**Status HatchBrush：： GetBackgroundColor (OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-hatchbrush-getbackgroundcolor)                                                                    | 取得此影線筆刷的背景色彩。                                                                                             |



 

 

 
