---
description: 本主題討論使用筆墨分析資料 proxy 功能時的事件詳細資料。
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: 資料 Proxy 事件流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432540"
---
# <a name="data-proxy-event-flow"></a>資料 Proxy 事件流程

本主題討論使用筆墨分析資料 proxy 功能時的事件詳細資料。

## <a name="data-proxy-event-flow-overview"></a>資料 Proxy 事件流程總覽

在 [**InkAnalyzer**](inkanalyzer.md)的資料 proxy 使用方式中，假設整合 InkAnalyzer 的應用程式已經有現有的檔模型，其想要將分析的結果 proxy。 也假設應用程式將會有來自任何先前分析作業的結果，而這些結果是在儲存于其檔模型時所要建立的。 可能也會有可能以 **ImageNode** 或 **TextWordNode**[**CoNtextNode**](icontextnode.md)形式新增至 **InkAnalyzer** 的非筆墨內容，可能會以筆墨標注。

資料 proxy 系統的關鍵是讓應用程式使用 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md)將 [**CoNtextNode**](icontextnode.md)標示為「部分擴展」。 當此旗標為 true 時， [**InkAnalyzer**](inkanalyzer.md) 會假設有關于該 **CoNtextNode** 的三件事：

-   [**CoNtextNode**](icontextnode.md)的位置是正確的。
-   [**CoNtextNode**](icontextnode.md)的類型正確。
-   該 [**CoNtextNode**](icontextnode.md) 的所有其他資訊都會儲存在其他位置。

根據這三個規則，如果 [**InkAnalyzer**](inkanalyzer.md) 需要 [**CoNtextNode**](icontextnode.md) 的其他相關資訊，則會引發 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件並參考問題中的 **CoNtextNode** 。 如此一來，應用程式就有機會在該 **CoNtextNode** 上設定所有已知資訊，讓 **InkAnalyzer** 更詳細地查看它。 處理 **PopulateCoNtextNode** 事件之後，有問題的 **CoNtextNode** 必須具有有效的位置屬性、設定的正確子節點數目（如果它是容器 **CoNtextNode** 或已設定正確的筆觸）（如果它是筆墨分葉 **CoNtextNode** [**）。**](icontextnode-setstrokes.md) 若無法正確設定此位置和子節點或筆劃資訊，將會導致 **InvalidOperation** 例外狀況。 容器 **CoNtextNode** 的子節點本身可以設定為部分擴展，在這種情況下，如果 **InkAnalyzer** 判斷目前的分析作業需要這些事件，則會引發更 **PopulateCoNtextNode** 的事件。

下表描述在 [**InkAnalyzer**](inkanalyzer.md)使用 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)事件時，何時會引發此事件。

[**InkAnalyzer**](inkanalyzer.md)計算出某些結果之後，就會回頭查看應用程式以更新結果。 第一個引發的事件是 [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) 事件。 此事件只是表示 **InkAnalyzer** 物件的樹狀結構狀態即將變更的應用程式。 這可讓應用程式有機會在任何具有儲存于其他位置之狀態的 [**CoNtextNodes**](icontextnodes.md)上，將 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md)旗標設定為 true。 然後， **InkAnalyzer** 會引發一連串的 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件來判斷資料的目前狀態。 一旦 determiend，就會 compelted 對帳作業，以判斷仍能套用的背景結果。

若要將結果套用至 [**InkAnalyzer**](inkanalyzer.md) ，會引發一連串的樹狀目錄修改事件。 樹狀目錄修改事件會逐步描述更新結果所需的所有變更。 這些事件的目的是要在 sucession 中處理，而不需中斷或取消。 如果在處理樹狀目錄修改事件期間，透過 [**Abort**](iinkanalyzer-abort.md) 方法) 取消分析作業 (， **InkAnalyzer** 的狀態將會無效，而且可能需要重新分析整個檔。

下表說明在 InkAnalyzer 的使用期間，何時引發樹狀修改事件。 這些資料表會參考下列事件流程圖所示的時間戳記。

![iimage 顯示應用程式 ui 和背景分析器之間的流程](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>加入筆劃



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1、T5 和 T9<br/> | \[在 AddStroke 的呼叫內 () \] \[ Tree 探索事件\]<br/> | 引發的 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)事件<br/> | 可能會產生 n 個 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md)事件，取決於存在的 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md)值設定為 true 的未 **分類**[**CoNtextNodes**](icontextnodes.md)數目。<br/> |
| T1、T5 和 T9<br/> | \[樹狀修改事件\]<br/>                                  | 引發的 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)事件<br/>   | 呼叫 [**AddStroke**](iinkanalyzer-addstroke.md)方法的結果只會引發一個 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md)事件。 所有筆劃都會加入相同的非分類 [**CoNtextNode**](icontextnode.md)。<br/>                      |



 

### <a name="deleting-a-stroke"></a>刪除筆劃



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2、T6 和 T10<br/> | \[在 [**RemoveStroke**](iinkanalyzer-removestroke.md)的呼叫內 () \] \[ Tree 探索事件\]<br/> | [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 引發的事件<br/> | 可能會有數個 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件，這取決於所刪除之筆劃的相關 [**CoNtextNodes**](icontextnodes.md) 數目是否為 true 的 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) 值。<br/> |
| T2、T6 和 T10<br/> | \[樹狀修改事件\]<br/>                                                                          | [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 引發的事件<br/> | 根據所刪除的筆墨內容和目前的分析結構，可能會產生任意數量的 [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 事件。<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>呼叫 BackgroundAnalyze 方法



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[在 [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)的呼叫內 () \] \[ Tree 探索事件\]<br/> | [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 引發的事件<br/> | 可能會產生 n 個 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件，視樹狀結構中有多少 [**CoNtextNodes**](icontextnodes.md) 的 [**PartiallyPopulated**](icontextnode-createpartiallypopulatedsubnode.md) 值為 true， (目前分析作業) 所需的每個 [**CoNtextNode**](icontextnode.md) 一個事件。<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>呼叫 BackgroundAnalyze 之後 () 傳回



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 至 T7<br/>   | \[從 BG 執行緒引發的事件\]<br/> | 引發的活動事件<br/> | 在這段背景分析期間，將會引發數個活動事件。<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>當 IntermediateResults 就緒時



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 至 T8<br/>   | \[從 BG 執行緒引發的事件，表示第一個協調作業的開頭\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) 引發的事件<br/>         | 只會引發一個 [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) 事件。 此事件會在檢查 [**InkAnalyzer**](inkanalyzer.md)的狀態之前引發，讓應用程式有機會在任何節點上設定 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) 值，或執行任何所需的本機檔鎖定。<br/> |
| T7 至 T8<br/>   | \[樹系探索事件\]<br/>                                                              | [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 引發的事件<br/>                   | 根據筆墨內容，可能會產生 n 個 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件數目。<br/>                                                                                                                                                                                                                                               |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) 引發的事件<br/>                     | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) 事件數目。<br/>                                                                                                                                                                                                                                                 |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 引發的事件<br/>                   | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 事件數目。<br/>                                                                                                                                                                                                                                               |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) 事件數目。<br/>                                                                                                                                                                                                                               |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) 事件數目。<br/>                                                                                                                                                                                                                                         |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | 根據筆墨內容，可能會產生 n 個 [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) 事件數目。<br/>                                                                                                                                                                                                                                                     |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) 事件數目。<br/>                                                                                                                                                                                                                                           |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) 事件數目。<br/>                                                                                                                                                                                                                                       |
| T7 至 T8<br/>   | \[樹狀修改事件\]<br/>                                                             | [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) 引發的事件<br/> | 根據筆墨內容，可能會產生 n 個 [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) 事件數目。 在此 [**協調**](iinkanalyzer-reconcile.md)期間內引發所有其他 [**CoNtextNode**](icontextnode.md)修改事件之後，就會將 **CoNtextNodePropertiesUpdated** 排程為引發。<br/>              |
| T7 至 T8<br/>   | \[事件表示第一個協調作業的結束\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) 引發的事件<br/>                        | 每個分析作業只會引發一個 [**IntermediateResults**](-ianalysisevents-intermediateresults.md) 事件。<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>處理 IntermediateResults 之後



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 至 T11<br/>  | \[從 BG 執行緒引發的事件\]<br/> | [**活動**](-ianalysisevents-activity.md) 引發的事件<br/> | 在這段背景分析期間，將會引發數個 [**活動**](-ianalysisevents-activity.md) 事件。<br/> |



 

### <a name="when-final-results-are-ready"></a>當最終結果就緒時



| 時間戳記 | 事件種類或用途 | 產生的事件 | 註解                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 至 T12<br/> | \[從 BG 執行緒引發的事件，表示第二個調解作業的開頭\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) 引發的事件<br/>         | 只會引發一個 [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) 事件。 此事件會在檢查 [**InkAnalyzer**](inkanalyzer.md)的狀態之前引發，讓應用程式有機會在任何節點上設定 [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) 值，或執行任何所需的本機檔鎖定。<br/> |
| T11 至 T12<br/> | \[樹系探索事件\]<br/>                                                               | [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 引發的事件<br/>                   | 根據筆墨內容，可能會產生任意數量的 [**PopulateCoNtextNode**](-ianalysisproxyevents-populatecontextnode.md) 事件。<br/>                                                                                                                                                                                                                                             |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) 引發的事件<br/>                     | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) 事件。<br/>                                                                                                                                                                                                                                               |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 引發的事件<br/>                   | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) 事件。<br/>                                                                                                                                                                                                                                             |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) 事件。<br/>                                                                                                                                                                                                                             |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md) 事件。<br/>                                                                                                                                                                                                                                       |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | 根據筆墨內容，可能會產生任意數量的 [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md) 事件。<br/>                                                                                                                                                                                                                                                   |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md) 事件。<br/>                                                                                                                                                                                                                                         |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md) 事件。<br/>                                                                                                                                                                                                                                     |
| T11 至 T12<br/> | \[樹狀修改事件\]<br/>                                                              | [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) 引發的事件<br/> | 根據筆墨內容，可能會產生任意數量的 [**CoNtextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) 事件。 在此 [**協調**](iinkanalyzer-reconcile.md)期間內引發所有其他 [**CoNtextNode**](icontextnode.md)修改事件之後，就會將 **CoNtextNodePropertiesUpdated** 排程為引發。<br/>            |
| T11 至 T12<br/> | \[事件表示第二個調解作業的結束\]<br/>                            | [**結果**](-ianalysisevents-results.md) 引發的事件<br/>                                                | 每個分析作業只會引發一個 [**結果**](-ianalysisevents-results.md) 事件。<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




