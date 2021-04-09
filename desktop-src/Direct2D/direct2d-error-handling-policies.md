---
title: Direct2D 錯誤處理原則
description: 本主題說明 Direct2D 錯誤處理原則。 包含以下幾節。
ms.assetid: b5fa327a-a315-46fa-aa78-8a5733faae01
keywords:
- Direct2D，錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc930e7ee9e5b73b5f676103f45ffe25e4d4e61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933523"
---
# <a name="direct2d-error-handling-policies"></a>Direct2D 錯誤處理原則

本主題說明 Direct2D 錯誤處理原則。 包含以下幾節。

-   [使用 HRESULT](#use-of-hresult)
-   [批次函數的傳回值](#return-value-of-batched-functions)
-   [輸入無效](#invalid-input)
    -   [Output 指標](#output-pointer)
    -   [必要參數](#required-parameter)
-   [NaN 和排序不正確的輸入矩形](#nan-and-poorly-ordered-input-rects)
    -   [NaN 作為輸入](#nan-as-input)
    -   [排序不正確的輸入矩形](#poorly-ordered-input-rects)

## <a name="use-of-hresult"></a>使用 HRESULT

如果函式未批次處理，而且可能有運行時失敗，則應該傳回 **HRESULT** 以表示失敗。 執行時間失敗是在設計階段無法避免的任何失敗，例如記憶體不足。

## <a name="return-value-of-batched-functions"></a>批次函數的傳回值

Direct2D 中的批次函式是在呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) 時，以單一單位處理的函式。 它們是 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 **EndDraw** 之間的繪圖命令，或 [**GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)上的命令。 針對這些函式，會在批次完成時回報錯誤。 在 **EndDraw** 以繪製命令之後，以及在 **關閉** **GeometrySink** 之後，會傳回錯誤。

如果已設定錯誤狀態，RenderTargets 停止繪圖，但是應用程式可以呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 來重設錯誤狀態並繼續繪製。

**Get** 和 **Set** 函數沒有傳回值。 但是，如果 **Set** 函數有不正確輸入，debug 層會產生訊息。 在此情況下，不會設定任何錯誤狀態，且 **set** 函數不會執行任何動作。

## <a name="invalid-input"></a>輸入無效

Direct2D 會在指標無效或 **為 Null** 時，取值會導致存取違規的輸出指標和必要參數。

### <a name="output-pointer"></a>Output 指標

Direct2D 會在輸入函式時，對輸出指標進行取值，並立即將其指派給 **Null** 。 如果呼叫端傳入 **Null** 做為傳回值的指標，這會造成存取違規。 這項原則也適用于指標的陣列。 針對其他輸出參數（例如結構），會在稍後進行取值，而且會導致存取違規。 不過，有一些方法會有選擇性的輸出指標 (也就是 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)、 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)) 不會造成存取違規。

### <a name="required-parameter"></a>必要參數

如果將 **Null** 傳遞給任何需要有效值的函式，則函式會提早對錯誤指標進行取值，而導致存取違規。 對於選擇性的輸入參數， **Null** 是有效的值，會產生一些合理的預設值。

## <a name="nan-and-poorly-ordered-input-rects"></a>NaN 和排序不正確的輸入矩形

在 Direct2D 中，會將 NaN 視為有效的輸入，且排序不正確的輸入矩形。

### <a name="nan-as-input"></a>NaN 作為輸入

NaN 會被視為有效的輸入，不過它通常會導致包含 NaN 未繪製的基本類型。 Direct2D API 不會提供 NaN 的明確篩選來驗證輸入。

### <a name="poorly-ordered-input-rects"></a>排序不正確的輸入矩形

排序不正確的輸入矩形會進行排序，以便正確地指定頂端、左方和右下角。 針對輸出，空的矩形看起來像這樣： {無限大、無限大、FloatMax、FloatMax}。

 

 