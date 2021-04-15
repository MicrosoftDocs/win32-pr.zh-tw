---
description: 本節包含筆墨分析中所使用之介面和類別的相關資訊。 筆墨分析類別和介面不符合自動化規範。
ms.assetid: 712908e1-2d1d-4e42-8c80-71354b03d318
title: 筆墨分析類別和介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1c157a08a4b7366c20a712c120265320ab4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510907"
---
# <a name="ink-analysis-classes-and-interfaces"></a>筆墨分析類別和介面

本節包含筆墨分析中所使用之介面和類別的相關資訊。 筆墨分析類別和介面不符合自動化規範。

## <a name="classes"></a>類別



| 類別                                    | 描述                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------|
| [**AnalysisRegion**](analysisregion.md) | 實行 [**IAnalysisRegion**](ianalysisregion.md) 介面。<br/> |
| [**InkAnalyzer**](inkanalyzer.md)       | 實行 [**IInkAnalyzer**](iinkanalyzer.md) 介面。<br/>       |



 

## <a name="interfaces"></a>介面



| 介面                                                    | 描述                                                                                                                                                                                                      |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAnalysisAlternate**](ianalysisalternate.md)             | 表示 [**ICoNtextNode**](icontextnode.md) 物件的可能手寫辨識字組相符專案。<br/>                                                                                        |
| [**IAnalysisAlternates**](ianalysisalternates.md)           | 包含物件的集合，這些物件會執行 [**IAnalysisAlternate**](ianalysisalternate.md) 介面，且為筆跡分析的結果。<br/>                                               |
| [**IAnalysisRegion**](ianalysisregion.md)                   | 公開代表檔區域之區域的方法和屬性。<br/>                                                                                                                    |
| [**IAnalysisStatus**](ianalysisstatus.md)                   | 藉由描述分析是否成功完成，以及是否發生任何警告，來表示筆墨分析作業的狀態。<br/>                                                  |
| [**IAnalysisWarning**](ianalysiswarning.md)                 | 表示筆墨分析作業期間發生的警告或錯誤。<br/>                                                                                                                           |
| [**IAnalysisWarnings**](ianalysiswarnings.md)               | 包含物件的集合，這些物件會執行 [**IAnalysisWarning**](ianalysiswarning.md) 介面，且為筆跡分析作業的結果。<br/>                                      |
| [**ICoNtextLink**](icontextlink.md)                         | 表示兩個 [**ICoNtextNode**](icontextnode.md) 物件之間的關聯性。<br/>                                                                                                                   |
| [**ICoNtextLinks**](icontextlinks.md)                       | 包含物件的集合，這些物件會執行 [**ICoNtextLink**](icontextlink.md) 介面。<br/>                                                                                                   |
| [**ICoNtextNode**](icontextnode.md)                         | 代表物件樹狀結構中建立為筆跡分析一部分的節點。<br/>                                                                                                                      |
| [**ICoNtextNodes**](icontextnodes.md)                       | 包含物件的集合，這些物件會執行 [**ICoNtextNode**](icontextnode.md) 介面，且為筆跡分析作業的結果。<br/>                                              |
| [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)     | 提供手寫辨識器的存取權，以搭配筆墨分析使用。<br/>                                                                                                                                 |
| [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)   | 包含物件的集合，這些物件會執行 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 介面，以及表示辨識手寫、物件或手勢的能力。<br/> |
| [**IInkAnalyzer**](iinkanalyzer.md)                         | 提供對版面配置分析、書寫和繪製分類，以及手寫辨識的存取。<br/>                                                                                                  |
| [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) | 公開方法，以評估 [**ICoNtextNode**](icontextnode.md) 物件是否符合或失敗指定的條件。<br/>                                                                              |



 

## <a name="return-values"></a>傳回值

Tablet PC COM 程式庫中的方法會傳回 **HRESULT** 值。 除非另有說明，否則此表描述 **HRESULT** 值的意義。



| HRESULT 值                                   | Description                                                                              |
|-------------------------------------------------|------------------------------------------------------------------------------------------|
| S \_ 確定<br/>                                | 成功。<br/>                                                                      |
| E \_ 指標<br/>                           | 輸入或輸出參數的至少一個指標 () 無效。<br/> |
| E \_ INVALIDARG<br/>                        | 成員嘗試傳入不正確引數。<br/>                              |
| E \_ 筆墨 \_ 例外狀況<br/>                    | 發生例外狀況。<br/>                                                           |
| E \_ OUTOFMEMORY<br/>                       | 系統無法配置記憶體來完成操作。<br/>                      |
| E \_ 失敗<br/>                              | 發生未指定的失敗。<br/>                                                 |
| E \_ INVALIDOPERATION<br/>                  | 成員嘗試使用不正確作業。<br/>                                 |
| TPC \_ E \_ 無效 \_ 模式<br/>                | 成員嘗試使用不正確模式。<br/>                                      |
| TPC \_ E \_ 不正確設定 \_<br/>       | 成員嘗試使用不正確設定。<br/>                             |
| TPC \_ E \_ 不正確封 \_ 包 \_ 描述<br/> | 成員嘗試使用不正確封包描述。<br/>                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




