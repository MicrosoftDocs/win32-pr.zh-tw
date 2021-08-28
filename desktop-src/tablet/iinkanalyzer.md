---
description: 提供對版面配置分析、書寫和繪製分類，以及手寫辨識的存取。
ms.assetid: 3a19db78-df14-43c2-9e3e-8cf674aa7b9c
title: 'IInkAnalyzer 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b37e6d72b87ac31bda7e6c9b0d6f9bf3d35af524eea201e446b50905447404b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939848"
---
# <a name="iinkanalyzer-interface"></a>IInkAnalyzer 介面

提供對版面配置分析、書寫和繪製分類，以及手寫辨識的存取。

## <a name="members"></a>成員

**IInkAnalyzer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IInkAnalyzer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IInkAnalyzer** 介面具有這些方法。



| 方法                                                                                                  | 描述                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**中止**](iinkanalyzer-abort.md)                                                                     | 取消目前的分析作業。<br/>                                                                                                                                           |
| [**AddStroke**](iinkanalyzer-addstroke.md)                                                             | 將單一筆劃的筆觸資料新增至 **IInkAnalyzer** ，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。<br/>                                              |
| [**AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)                                       | 將單一筆劃的筆觸資料新增至 **IInkAnalyzer** ，並將特定文化特性識別碼指派給筆劃。<br/>                                                             |
| [**AddStrokes**](iinkanalyzer-addstrokes.md)                                                           | 將多個筆劃的筆觸資料新增至 **IInkAnalyzer** ，並將使用中輸入執行緒的文化特性識別碼指派給筆劃。<br/>                                            |
| [**AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)                                     | 將多個筆劃的筆觸資料新增至 **IInkAnalyzer** ，並將指定的文化特性識別碼指派給筆觸。<br/>                                                        |
| [**AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)                       | 將多個筆劃的筆觸資料新增至自訂辨識器節點。<br/>                                                                                                                |
| [**AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)                         | 將單一筆觸的筆觸資料新增至自訂辨識器節點。<br/>                                                                                                                 |
| [**分析**](iinkanalyzer-analyze.md)                                                                 | 執行同步筆墨分析。<br/>                                                                                                                                                |
| [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)                                             | 執行非同步筆跡分析。<br/>                                                                                                                                               |
| [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md)                                                 | 清除 **IInkAnalyzer** 中的筆觸封包資料。<br/>                                                                                                                              |
| [**CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)                                           | 將具有無限區域的新分析提示節點加入至 **IInkAnalyzer**。<br/>                                                                                                      |
| [**CreateCoNtextNodes**](iinkanalyzer-createcontextnodes.md)                                           | 建立 [**ICoNtextNodes**](icontextnodes.md) 物件。<br/>                                                                                                                         |
| [**CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)                                   | 為 **IInkAnalyzer** 建立新的自訂辨識器節點。<br/>                                                                                                                    |
| [**DeleteAnalysisHint**](iinkanalyzer-deleteanalysishint.md)                                           | 從 **IInkAnalyzer** 中移除分析提示。<br/>                                                                                                                               |
| [**FindInkLeafNodes**](iinkanalyzer-findinkleafnodes.md)                                               | 抓取所有筆墨分葉節點。<br/>                                                                                                                                              |
| [**FindInkLeafNodesForStrokes**](iinkanalyzer-findinkleafnodesforstrokes.md)                           | 抓取包含指定筆劃的筆墨分葉節點。<br/>                                                                                                                  |
| [**FindLeafNodes**](iinkanalyzer-findleafnodes.md)                                                     | 抓取所有分葉節點。<br/>                                                                                                                                                  |
| [**FindNode**](iinkanalyzer-findnode.md)                                                               | 取得指定之全域唯一識別碼 (GUID) 的 [**ICoNtextNode**](icontextnode.md) 物件。<br/>                                                                      |
| [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md)                                                 | 抓取指定類型的所有 [**ICoNtextNode**](icontextnode.md) 物件。<br/>                                                                                          |
| [**FindNodesOfTypeForStrokes**](iinkanalyzer-findnodesoftypeforstrokes.md)                             | 抓取包含指定筆劃之指定型別的所有 [**ICoNtextNode**](icontextnode.md) 物件。<br/>                                                       |
| [**FindNodesOfTypeInSubTree**](iinkanalyzer-findnodesoftypeinsubtree.md)                               | 抓取指定之 **ICoNtextNode** 物件的子系之指定型別的所有 [**ICoNtextNode**](icontextnode.md)物件。<br/>                            |
| [**FindNodesWithCallBack**](iinkanalyzer-findnodeswithcallback.md)                                     | 抓取符合指定準則的所有 [**ICoNtextNode**](icontextnode.md) 物件。<br/>                                                                              |
| [**FindNodesWithCallBackInSubTree**](iinkanalyzer-findnodeswithcallbackinsubtree.md)                   | 抓取符合指定準則的所有 [**ICoNtextNode**](icontextnode.md) 物件，而且是指定之 **ICoNtextNode** 物件的子系。<br/>                 |
| [**GetAlternates**](iinkanalyzer-getalternates.md)                                                     | 針對所有與 **IInkAnalyzer** 相關聯的筆墨抓取10個分析替代項。<br/>                                                                                                |
| [**GetAlternatesForCoNtextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)                       | 抓取指定 [**ICoNtextNodes**](icontextnodes.md) 集合中節點的分析替代項。<br/>                                                                     |
| [**GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)                                 | 使用指定的筆觸識別碼抓取筆劃的分析替代項。<br/>                                                                                              |
| [**GetAnalysisHints**](iinkanalyzer-getanalysishints.md)                                               | 抓取所有附加至 **IInkAnalyzer** 的分析提示 [**ICoNtextNode**](icontextnode.md)物件。<br/>                                                        |
| [**GetAnalysisHintsByName**](iinkanalyzer-getanalysishintsbyname.md)                                   | 抓取所有附加至 **IInkAnalyzer** 並具有指定名稱的分析提示 [**ICoNtextNode**](icontextnode.md)物件。<br/>                       |
| [**GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)                                               | 抓取旗標，以控制 **IInkAnalyzer** 執行筆墨分析的方式。<br/>                                                                                                      |
| [**GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)                                                   | 抓取自上次分析作業之後變更的區域。<br/>                                                                                                            |
| [**GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)         | 抓取 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件的已排序集合。<br/>                                                                              |
| [**GetNodesFromTextRange**](iinkanalyzer-getnodesfromtextrange.md)                                     | 抓取 [**ICoNtextNode**](icontextnode.md) 物件的集合，這些物件與指定之內容節點的指定文字範圍有關。<br/>                             |
| [**GetRecognizedString**](iinkanalyzer-getrecognizedstring.md)                                         | 針對 **IInkAnalyzer** 中的整個內容節點樹狀結構，抓取辨識作業的最佳結果字串。<br/>                                                           |
| [**GetRootNode**](iinkanalyzer-getrootnode.md)                                                         | 捕獲 **IInkAnalyzer** 物件的內容樹狀結構的根 [**ICoNtextNode**](icontextnode.md) 。<br/>                                                                            |
| [**GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md)                                         | 抓取指定之筆劃的地區設定識別碼。<br/>                                                                                                                          |
| [**GetStrokeType**](iinkanalyzer-getstroketype.md)                                                     | 抓取指定之筆劃的型別。<br/>                                                                                                                                       |
| [**GetTextRangeFromNodes**](iinkanalyzer-gettextrangefromnodes.md)                                     | 在可辨識的字串中尋找對應于 [**ICoNtextNode**](icontextnode.md) 物件集合的文字範圍。<br/>                                                   |
| [**IsAnalyzing**](iinkanalyzer-isanalyzing.md)                                                         | 抓取值，指出 **IInkAnalyzer** 是否正在執行筆墨分析。<br/>                                                                                             |
| [**LoadResults**](iinkanalyzer-loadresults.md)                                                         | 將儲存的分析結果載入 **IInkAnalyzer** 中。<br/>                                                                                                                           |
| [**ModifyTopAlternate**](iinkanalyzer-modifytopalternate.md)                                           | 將目前的上方替代變更為指定的替代，並清除所有與替代物件相關聯之 [**ICoNtextNode**](icontextnode.md) 物件的確認類型。<br/> |
| [**ModifyTopAlternateWithConfirmation**](iinkanalyzer-modifytopalternatewithconfirmation.md)           | 將目前的上方替代變更為指定的 [**IAnalysisAlternate**](ianalysisalternate.md)。<br/>                                                                              |
| [**Reconcile**](iinkanalyzer-reconcile.md)                                                             | 判斷哪些部分的分析結果在背景筆墨分析期間已變更。<br/>                                                                                    |
| [**RemoveStroke**](iinkanalyzer-removestroke.md)                                                       | 從 **IInkAnalyzer** 中移除指定的筆觸。<br/>                                                                                                                           |
| [**RemoveStrokes**](iinkanalyzer-removestrokes.md)                                                     | 從 **IInkAnalyzer** 中移除指定的筆觸。<br/>                                                                                                                          |
| [**SaveResults**](iinkanalyzer-saveresults.md)                                                         | 儲存 **IInkAnalyzer** 的所有分析結果。<br/>                                                                                                                               |
| [**SaveResultsForNodes**](iinkanalyzer-saveresultsfornodes.md)                                         | 儲存與 **IInkAnalyzer** 相關聯之特定內容節點集合的分析結果。<br/>                                                                                |
| [**SaveResultsForStrokes**](iinkanalyzer-saveresultsforstrokes.md)                                     | 儲存與 **IInkAnalyzer** 相關聯之指定筆劃的分析結果。<br/>                                                                                             |
| [**搜尋**](iinkanalyzer-search.md)                                                                   | 提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。<br/>                                      |
| [**SearchWithLanguageId**](iinkanalyzer-searchwithlanguageid.md)                                       | 提供模糊、不區分大小寫片語的搜尋，以供分析的書寫筆劃和已分析的繪圖筆劃具有可辨識的類型。<br/>                                      |
| [**SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)                                               | 修改旗標，以控制 **IInkAnalyzer** 執行筆墨分析的方式。<br/>                                                                                                       |
| [**SetDirtyRegion**](iinkanalyzer-setdirtyregion.md)                                                   | 修改自上次分析作業之後變更的區域。<br/>                                                                                                             |
| [**SetHighestPriorityInkAnalysisRecognizer**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) | 將指定的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 移至 **IInkAnalyzer** 物件的筆跡辨識器清單中的第一個位置。<br/>                      |
| [**SetStrokeLanguageId**](iinkanalyzer-setstrokelanguageid.md)                                         | 變更指定之筆劃的地區設定識別碼。<br/>                                                                                                                           |
| [**SetStrokesLanguageId**](iinkanalyzer-setstrokeslanguageid.md)                                       | 變更指定之筆劃的地區設定識別碼。<br/>                                                                                                                          |
| [**SetStrokesType**](iinkanalyzer-setstrokestype.md)                                                   | 變更指定之筆劃的型別。<br/>                                                                                                                                        |
| [**SetStrokeType**](iinkanalyzer-setstroketype.md)                                                     | 變更指定之筆劃的型別。<br/>                                                                                                                                         |
| [**UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md)                                             | 更新指定筆劃的封包資料。<br/>                                                                                                                                |



 

## <a name="remarks"></a>備註

**IInkAnalyzer** 會使用筆觸封包資料來分析筆墨，而不會直接與 [**InkDisp 類別**](inkdisp-class.md) 或 [InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 物件互動。

若要在 **IInkAnalyzer** 中新增或移除筆觸以進行分析，請使用下列其中一種方法。

-   [**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
-   [**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
-   [**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md)
-   [**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md)

這些方法會更新中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) ，這是在下一次分析作業中分析筆劃的區域。

若要分析筆墨，請使用 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md) 或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md) 方法。 在分析期間， **IInkAnalyzer** 會執行版面配置分析、筆劃分類和手寫辨識。

若要變更版面配置分析和筆劃分類設定，請使用 [**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md) 屬性。

在分析期間， **IInkAnalyzer** 會收到許多事件，包括背景分析期間所產生的事件。 [**\_ IAnalysisProxyEvents**](-ianalysisproxyevents.md)支援 **IInkAnalyzer** 的資料 proxy 功能。 如需詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。 若要從事件處理常式內停止分析進程，請呼叫 [**IInkAnalyzer：： Abort 方法**](iinkanalyzer-abort.md)。

若要修改筆墨分析器用來辨識手寫的語言，請使用 [**IInkAnalyzer：： SetStrokeLanguageId 方法**](iinkanalyzer-setstrokelanguageid.md) 或 [**IInkAnalyzer：： SetStrokesLanguageId 方法**](iinkanalyzer-setstrokeslanguageid.md)。 若要修改筆墨分析器分類特定筆劃的方式，請使用 [**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md) 或 [**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)。

**IInkAnalyzer** 會載入所有已安裝筆跡辨識器的資訊。 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)會傳回包含每個可用 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)的 [**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)集合。 如果有一個以上的筆墨辨識器支援特定語言，請使用 [**IInkAnalyzer：： SetHighestPriorityInkAnalysisRecognizer 方法**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md) 來設定哪個筆墨辨識器會處理該語言的筆觸。

流量分析提示可以提供額外的內容給筆墨分析器，以改善辨識的精確度。 其他內容資訊可協助筆墨分析器限制可能的辨識結果數目。 例如，您可以藉由定義 factoids 和預期的單字，或將輸入結構化到辨識指南中，來縮小範圍。 如需有關將內容提供給筆墨分析器的詳細資訊，請參閱：

-   [**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
-   [**IInkAnalyzer：:D eleteAnalysisHint 方法**](iinkanalyzer-deleteanalysishint.md)
-   [**IInkAnalyzer：： GetAnalysisHints 方法**](iinkanalyzer-getanalysishints.md)
-   [**IInkAnalyzer：： GetAnalysisHintsByName 方法**](iinkanalyzer-getanalysishintsbyname.md)

筆墨分析器會以字串或 [**ICoNtextNode**](icontextnode.md) 物件的樹狀結構來表示分析結果。 若要存取可辨識的字串，請使用 [**IInkAnalyzer：： GetRecognizedString 方法**](iinkanalyzer-getrecognizedstring.md)。 若要存取內容節點樹狀結構的根目錄，請使用 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)。 筆墨分析器有下列方法可尋找特定的內容節點或文字。

-   [**IInkAnalyzer：： FindInkLeafNodes 方法**](iinkanalyzer-findinkleafnodes.md)
-   [**IInkAnalyzer：： FindInkLeafNodesForStrokes 方法**](iinkanalyzer-findinkleafnodesforstrokes.md)
-   [**IInkAnalyzer：： FindLeafNodes 方法**](iinkanalyzer-findleafnodes.md)
-   [**IInkAnalyzer：： FindNode 方法**](iinkanalyzer-findnode.md)
-   [**IInkAnalyzer：： FindNodesOfType 方法**](iinkanalyzer-findnodesoftype.md)
-   [**IInkAnalyzer：： FindNodesOfTypeForStrokes 方法**](iinkanalyzer-findnodesoftypeforstrokes.md)
-   [**IInkAnalyzer：： FindNodesOfTypeInSubTree 方法**](iinkanalyzer-findnodesoftypeinsubtree.md)
-   [**IInkAnalyzer：： FindNodesWithCallBack 方法**](iinkanalyzer-findnodeswithcallback.md)
-   [**IInkAnalyzer：： FindNodesWithCallBackInSubTree 方法**](iinkanalyzer-findnodeswithcallbackinsubtree.md)

若要使用替代分析結果，請使用下列其中一種方法。

-   [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)
-   [**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)
-   [**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)
-   [**IInkAnalyzer：： ModifyTopAlternate 方法**](iinkanalyzer-modifytopalternate.md)
-   [**IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法**](iinkanalyzer-modifytopalternatewithconfirmation.md)

若要儲存分析結果，請使用下列其中一種方法。

-   [**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)
-   [**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)
-   [**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)

若要載入儲存的結果，請使用 [**IInkAnalyzer：： LoadResults 方法**](iinkanalyzer-loadresults.md)。

如需使用 **IInkAnalyzer** 來分析筆墨的詳細資訊，請參閱 [筆墨分析總覽](ink-analysis-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**ICoNtextLink**](icontextlink.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

