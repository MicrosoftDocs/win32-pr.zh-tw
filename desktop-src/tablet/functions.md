---
description: 本章節包含 Tablet PC 的核心功能。
ms.assetid: 8f94a82c-de93-4649-a9b5-0adcbe01333d
title: 核心 Tablet PC 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb9e58300321f2b483cc062472950f5d252a292dc1380b3e5c030993ddbe6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967539"
---
# <a name="core-tablet-pc-functions"></a>核心 Tablet PC 功能

本章節包含 Tablet PC 的核心功能。

## <a name="in-this-section"></a>本節內容



| 函式                                                         | 描述                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddOneStroke**](addonestroke.md)                             | 將新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件加入至傳入的 [**InkDivider**](inkdivider-class.md) 物件。                                                                 |
| [**CallDivide**](calldivide.md)                                 | 從 [**InkDivider**](inkdivider-class.md) 物件中取出分析資訊。                                                                                                              |
| [**CallDivideResults**](calldivideresults.md)                   | 傳回 [**InkDivider**](inkdivider-class.md) 物件的分析結果。                                                                                                                    |
| [**CallDivideResultsStrokeIds**](calldivideresultsstrokeids.md) | 抓取筆墨分析所決定之對應單字、線條、段落或繪圖的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)屬性。 |
| [**CreateInkDivider**](createinkdivider.md)                     | 具現化 [**InkDivider**](inkdivider-class.md) 介面的執行，並傳回其控制碼。                                                                                      |
| [**DeleteInkDivider**](deleteinkdivider.md)                     | 刪除 [**InkDivider**](inkdivider-class.md) 物件，並釋放相關聯的資源。                                                                                                         |
| [**InvokeIDispatch**](invokeidispatch.md)                       | 叫用 IDispatch 介面的 helper 功能。                                                                                                                                           |
| [**RecognizerCoNtextSet**](recognizercontextset.md)             | 測試 [**InkDivider**](inkdivider-class.md) 物件是否可以使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 類別來分析文字。                                      |
| [**RemoveStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-removestrokes)                | 從 [**InkDivider**](inkdivider-class.md)移除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件。                                                                                           |
| [**SetLineHeight**](setlineheight.md)                           | 在 [**InkDivider**](inkdivider-class.md)物件上設定 [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)屬性。                                                                                 |
| [**SetLineRecoCallback**](setlinerecocallback.md)               | 設定要在行辨識期間使用的回呼函數。                                                                                                                                        |



 

 

 
