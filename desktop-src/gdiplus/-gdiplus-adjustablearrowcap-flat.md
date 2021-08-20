---
description: Windows GDI+ 會公開由大約600個函式所組成的一般 API。 這些一般 API 函式是由 AdjustableArrowCap c + + 類別包裝。
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: AdjustableArrowCap 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52487252c5b684cc762248b35c0fe5f45e8e3759993ba3b99ab01343b84c412d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977828"
---
# <a name="adjustablearrowcap-functions"></a>AdjustableArrowCap 函式

Windows GDI+ 會公開一個包含大約600函式的一般 API，這些函式會在 Gdiplus.dll 中執行，並在 Gdiplusflat 中宣告。 GDI+ 一般 API 中的函式是由大約 40 c + + 類別的集合所包裝。 建議您不要直接呼叫一般 API 中的函式。 每當您對 GDI+ 進行呼叫時，您應該呼叫 c + + 包裝函式所提供的方法和函式。 Microsoft 產品支援服務將不會提供直接呼叫一般 API 的程式碼支援。 如需使用這些包裝函式方法的詳細資訊，請參閱[GDI+ 一般 API](-gdiplus-flatapi-flat.md)。

下列一般 API 函式是由 [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) c + + 類別包裝。

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>AdjustableArrowCap 函式和對應的包裝函式方法



| 一般函數                                                                                                          | 包裝函式方法                                                                                                                | 描述                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap (REAL height、REAL width、BOOL isFilled、GpAdjustableArrowCap \* \* cap)  | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | 使用指定的高度和寬度，建立可調整的箭號行端點。 可以填滿或 nonfilled 箭號行端點。 中間的內凹預設值為零。                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight (GpAdjustableArrowCap \* cap、REAL height)                            | [**AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | [**AdjustableArrowCap：： SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)方法會設定箭號端點的高度。 這是從箭號基底到其頂點的距離。                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight (GpAdjustableArrowCap \* cap、REAL \* height)                          | [**AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | [**AdjustableArrowCap：： GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)方法會取得箭號端點的高度。 高度是從箭號基底到其頂點的距離。                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth (GpAdjustableArrowCap \* 端點，真實寬度)                              | [**AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | [**AdjustableArrowCap：： SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)方法會設定箭號端點的寬度。 寬度是箭號基底端點之間的距離。                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth (GpAdjustableArrowCap \* 端點，真實 \* 寬度)                            | [**AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | [**AdjustableArrowCap：： GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)方法會取得箭號指標的寬度。 寬度是箭號基底端點之間的距離。                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* cap、REAL middleInset)                  | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | [**AdjustableArrowCap：： SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)方法會設定基底的中點向頂點移位的單位數。                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* cap、REAL \* middleInset) <br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | [**AdjustableArrowCap：： GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)方法會取得內凹的值。 中間的內凹是基底的中點向頂點移位的單位數。 |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState (GpAdjustableArrowCap \* cap，BOOL fillState) <br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | [**AdjustableArrowCap：： SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)方法會設定箭號端點的填滿狀態。 如果未填滿箭號端點，則只會繪製外框。                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState (GpAdjustableArrowCap \* cap，BOOL \* fillState) <br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | [**AdjustableArrowCap：： IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)方法會決定是否要填滿箭號端點。                                                                                               |



 

 

