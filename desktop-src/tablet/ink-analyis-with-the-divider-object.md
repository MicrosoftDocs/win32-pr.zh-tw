---
description: 分隔物件提供版面配置分析功能，可將筆劃分類並群組為不同的結構化元素。
ms.assetid: 9e4ed24f-4451-431c-9f0f-2f1c4f5e5084
title: 使用分隔物件的筆墨分析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d036428bbe32c42e6419c2218e6196a0b89a892137e55d141d5553d360c0a652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939551"
---
# <a name="ink-analysis-with-the-divider-object"></a>使用分隔物件的筆墨分析

[分隔](/previous-versions/ms583616(v=vs.100))物件提供版面配置分析功能，可將筆劃分類並群組為不同的結構化元素。

## <a name="divider-object"></a>分隔物件

當您新增或移除筆劃時， [分割](/previous-versions/ms583616(v=vs.100)) 物件會分析筆劃。 您可以藉由呼叫分隔物件的[除法](/previous-versions/ms568936(v=vs.100))方法，在[DivisionResult](/previous-versions/ms583620(v=vs.100))物件中取出分析筆劃的目前分類和群組。

[分割](/previous-versions/ms583616(v=vs.100))物件所分析的筆觸會保留在分隔物件的 [[筆劃](/previous-versions/ms582090(v=vs.100))] 屬性中。 因為 [筆劃](/previous-versions/ms552701(v=vs.100)) 集合是筆墨資料的參考，而不是實際資料本身，所以筆劃集合的父 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件變更可能會使筆劃集合無效。 如需筆墨資料的詳細資訊，請參閱 [筆墨資料](ink-data.md)。

[分割](/previous-versions/ms583616(v=vs.100))物件會使用辨識器內容來改善其辨識區段的分析，並產生手寫元素的辨識文字。 如果未將辨識器內容指派給分割區物件的 [RecognizerCoNtext](/previous-versions/ms582089(v=vs.100)) 屬性，或未安裝辨識器，則配置分析功能會執行辨識區段分割，而且沒有任何文字與 [DivisionResult](/previous-versions/ms583620(v=vs.100)) 物件相關聯。 如需筆跡辨識的詳細資訊，請參閱 [筆跡](ink-recognition.md)辨識。

## <a name="divisionresult-object"></a>DivisionResult 物件

每個[DivisionResult](/previous-versions/ms583620(v=vs.100))物件都會在呼叫[除法](/previous-versions/ms568936(v=vs.100))方法時，記錄[分界線](/previous-versions/ms583616(v=vs.100))物件所包含之筆劃的版面配置分析。 DivisionResult 物件也會儲存分析中所使用之筆劃的複本。

[DivisionResult](/previous-versions/ms583620(v=vs.100))物件會依結構化元素類型來分組分析結果。 DivisionResult 物件的 [**ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) 方法會在 [DivisionUnits](/previous-versions/ms583625(v=vs.100)) 集合中傳回指定類型的所有結構化元素集合。 [InkDivisionType](/previous-versions/ms552251(v=vs.100))列舉會定義版面配置分析可辨識的元素類型。

下表描述 [InkDivisionType](/previous-versions/ms552251(v=vs.100)) 列舉中的元素類型。



| 名稱                 | 描述                                                                      |
|----------------------|----------------------------------------------------------------------------------|
| 區段<br/>   | 辨識區段。<br/>                                                |
| 折線圖<br/>      | 包含一或多個辨識區段的手寫行。<br/> |
| Paragraph<br/> | 包含一或多行手寫的筆劃區塊。<br/>    |
| 繪圖<br/>   | 非文字的筆墨。<br/>                                                 |



 

下圖顯示 [DivisionResult](/previous-versions/ms583620(v=vs.100)) 物件辨識的不同元素類型範例。

![divisionresult 物件辨識的不同元素類型圖例](images/5f2ab955-1f74-4b71-b3ba-8d1ca23e0578.gif)

## <a name="divisionunits-collection-and-divisionunit-objects"></a>DivisionUnits 集合和 DivisionUnit 物件

每個 [DivisionUnits](/previous-versions/ms583625(v=vs.100)) 集合都是單一結構專案類型的版面配置分析結果複本。 [DivisionUnit](/previous-versions/ms583624(v=vs.100))物件代表 DivisionUnits 集合中的個別元素。 每個結構專案都有組成專案的筆劃參考。 如果已安裝辨識器，手寫元素就會有可用的辨識文字。 行和辨識區段專案也包含可將元素的筆觸從垂直旋轉為水準的旋轉矩陣。

[筆墨分割範例](ink-divider-sample.md)主題示範如何使用具有[筆墨](/previous-versions/ms583670(v=vs.100))物件的[分界線](/previous-versions/ms583616(v=vs.100))物件來執行筆墨版面配置分析。

如需使用筆墨分析的詳細資訊，請參閱 [分割物件](the-divider-object.md)。

 

