---
title: 預設值
description: 預設值
ms.assetid: fb2ccd8b-eda2-414a-870c-85b658f40eb9
keywords:
- 視覺效果，預設
- 自訂視覺效果，預設
- 視覺效果、橫條圖預設值
- 自訂視覺效果，橫條圖預設值
- 視覺效果、Wave 預設值
- 自訂視覺效果，Wave 預設值
- 視覺效果，轉譯函數
- 自訂視覺效果，轉譯函數
- 轉譯函數，預設
- 視覺效果，GetPresetTitle 函式
- 自訂視覺效果，GetPresetTitle 函式
- GetPresetTitle 函式
- 列舉，視覺效果預設
- 視覺效果，列舉
- 自訂視覺效果，列舉
- 視覺效果、資源標頭和字串
- 自訂視覺效果、資源標頭和字串
- 視覺效果中的預設值，橫條圖預設
- 視覺效果中的預設值，Wave 預設
- 視覺效果中的預設值，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e024427d19da0a30f54d9ebc0590feedb8d0f97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183357"
---
# <a name="presets"></a>預設值

預設會提供一種方式，讓來自相同視覺效果的不同效果。 例如，您可以建立一個程式碼區塊所產生的光暈效果，但使用預設值來判斷光暈的色彩。 您的預設名稱可能是紅色、綠色和藍色。

Wizard 會為它產生的程式碼定義兩個預設值。 其中一個稱為橫條圖，另一個稱為 Wave。 [橫條圖] 預設會顯示在音訊頻譜中顯示活動的橫條，並使用波形資料。 Wave 預設值會顯示 wiggling 線，以顯示波形的音訊電源。

如果您變更任何預設資訊，您也必須變更所產生程式碼的下列部分。

## <a name="render-function"></a>Render 函數

**IWMPEffects：： Render** 函式位於檔案 *名稱*.cpp 中，其中 *專案* 名稱是您在執行嚮導時所選擇的專案名稱。

轉譯 **函數中產生的程式** 代碼會使用 switch 語句，在兩個預設值之間進行選擇。 目前的預設值是使用者在 Windows Media Player 中選取的任何內容。 如果您想要變更特定預設值所執行的程式碼，或加入或減去預設值，請據以修改 switch 語句。

這兩個預設值是由預設列和 **預設 \_ 範圍** 列舉所定義。 **\_** 將呼叫預設值的選項是由 m nPreset 所定義 \_ 。

## <a name="getpresettitle"></a>GetPresetTitle

**IWMPEffects：： GetPresetTitle** 函式位於檔案 *名稱*.cpp 中，其中 *專案* 名稱是您在執行嚮導時所選擇的專案名稱。

**GetPresetTitle** 函數會設定預設列舉和字串資源之間的關聯性。 預設會由嚮導產生列舉預設 **列和 \_ 預設** **\_ 範圍** ，並使用字串資源識別碼 \_ BARSPRESETNAME 和 id \_ SCOPEPRESETNAME。

如果您加入、減去或變更預設值，則需要變更列舉和字串資源。

## <a name="preset-enumerations"></a>預設列舉值

預設的列舉是在檔案 *名稱*.h 中定義，其中 *專案* 名稱是您在執行嚮導時所選擇的專案名稱。

列舉會定義目前的兩個預設值和計數。 如果您加入或減少預設值或變更列舉，請務必變更此列舉，使預設值的計數和順序正確無誤。 這個列舉是用來確保您會在 **轉譯函數中呼叫正確的預設** 值。

## <a name="resource-header"></a>資源標頭

您必須在資源 .h 標頭檔中設定預設名稱的資源。 目前的預設值定義為：


```C++
#define IDS_BARSPRESETNAME              102
#define IDS_SCOPEPRESETNAME             103
```



如果您新增或減少預設值，您必須變更資源標頭和其數目。

## <a name="resource-strings"></a>資源字串

預設的實際名稱會定義在資源檔 *專案* 名稱的 .dll 中 *，其中，專案名稱* 是您在執行嚮導時所選擇的專案名稱。 您可以手動編輯此檔案，或使用 Microsoft Visual C++ 隨附的資源編輯器。

產生的名稱是視覺效果的名稱加上特定的預設值。 產生之程式碼的資源檔會將它們定義為：


```C++
IDS_BARSPRESETNAME      "projectname Bars"
IDS_SCOPEPRESETNAME     "projectname Wave"
```



其中 *專案名稱是* 您在執行嚮導時所選擇的專案名稱。 這是您將變更預設預設名稱的位置，而這就是 Windows Media Player 將其參考及顯示的方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**執行您的程式碼**](implementing-your-code.md)
</dt> </dl>

 

 




