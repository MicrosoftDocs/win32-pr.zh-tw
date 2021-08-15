---
title: UILess 模式總覽
description: UILess 模式總覽
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- 文字服務架構 (TSF) 、UILessMode
- TSF (文字服務架構) ，UILessMode
- 啟用 TSF 的應用程式，UILessMode
- UILessMode
- 文字服務架構 (TSF) ，候選清單 UIElement
- TSF (文字服務架構) ，候選清單 UIElement
- 啟用 TSF 的應用程式，候選清單 UIElement
- 候選清單 UIElement
- 文字服務架構 (TSF) 、UIElement 提示
- TSF (文字服務架構) ，UIElement 提示
- 啟用 TSF 的應用程式，UIElement 提示
- UIElement 提示
- 文字服務架構 (TSF) 、預先定義的 UI 元素
- TSF (文字服務架構) ，預先定義的 UI 元素
- 啟用 TSF 的應用程式，預先定義的 UI 元素
- 預先定義的 UI 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdac8e43cc8342c50a6d232b801af0c65315fd407b9f413f2b5fdcb7074282fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949853"
---
# <a name="uiless-mode-overview"></a>UILess 模式總覽

## <a name="how-to-create-uilessmode"></a>如何建立 UILessMode

**使無 UI 的執行緒：** 應用程式可透過 [**ITfThreadMgrEx：： ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) 與 ITF AE UIELEMENTENABLEDONLY，讓 UI 更少執行緒 \_ \_ 。 使用這個旗標啟動 ThreadMgr 時，只會線上程上啟動可控制其 UI 元素的秘訣。 應用程式需要執行 [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) 介面，並將介面告知執行緒管理員。 [**ITfUIElementSink：： BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) 會在提示顯示其 UI 時呼叫。 應用程式可能會在 pbShow 參數中傳回 **TRUE** ，以允許提示在應用程式不需要繪製時顯示提示的原始 UI。 如果應用程式不允許提示的 UI，它會在 pbShow 中傳回 **FALSE** (請參閱下圖) 。 應用程式可以從 *pElement* 參數取得一些資訊，藉此繪製 UI。 它可能是候選清單、語言列專案或秘訣的自訂 UI。 應用程式可以透過 QIing [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) 介面來知道 UI 的種類。 當 UI 變更時，會呼叫 [**ITfUIElementSink：： UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) 。 此應用程式可以比較 pElement->GetGUID () 的 GUID，以瞭解該元素目前是否由應用程式繪製。

**讓 UI 更不感知提示：** 如果應用程式想要在不想要允許提示 UI 的應用程式（例如遊戲應用程式或全螢幕應用程式）下執行，則秘訣應支援較不模式的 UI。 若要以 UI 較不清楚，提示必須執行 [**ITfTextInputProcessorEx**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) 介面。 如果未執行這個介面，則不會在 UI 較低模式的執行緒下啟用提示。 此外，提示必須先呼叫 [**ITFUIElementMgr：： BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) ，才能在螢幕上顯示可見的 UI。 這個方法會呼叫 [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) 來通知應用程式。 應用程式會決定是否可顯示。 當提示呼叫 BeginUIElement () 時，提示必須具有對應 UI 的 [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) 介面。 應用程式會將介面 QI，以取得其他 UI 特定介面，以取得詳細資訊來繪製 UI。 System 預先定義 [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) and [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) for TIP。 當提示想要在 UI less 模式執行緒下顯示候選清單時，提示必須建立 **ITfCandidateListUIElement** 介面的實例，並呼叫 **ITFUIElementMgr：： BeginUIElement**。 呼叫 [**ITfTextInputProcessorEx：： ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) 時，秘訣已經知道執行緒的 UI 較小，因此可以消除額外的自訂 UI。 當然，它可以執行自己的介面，它可以從 QIed 並嘗試發出通知。 因此秘訣和 &**ITfUIElement** 程式可以有 tip 自訂 UI 的協商。

## <a name="uielement-supporting-tip"></a>UIElement 支援提示

支援 UIElement 的秘訣必須由 GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED 分類。 GUID \_ TFCAT TIPCAP UIELEMENTENABLED 中的秘訣 \_ \_ 必須使用 [**ITFUIELEMENTMGR**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) 來顯示任何 ui，讓應用程式能夠控制 ui 的可見度。

**顯示/隱藏 UIElement 的狀態：** 顯示/隱藏 [**ITfUIElement：： Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) 或 [**ITfUIElement：： IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) 方法所指出的狀態是實際的可見狀態。 它與 UIElement 的可用性無關。 當顯示狀態存在時，UIElement 應該一律可供使用。 顯示狀態可從應用程式進行控制。 應用程式可能會突然進入 UILess 模式，並開始繪製一些 UI，方法是呼叫 **ITfUIElement：： Show** 和 **FALSE** 來隱藏所有提示 ui。 然後提示可以採用其中一個選項。 1) 提示可以將 UIElement 移至隱藏狀態，並開始產生 UpdateUIElement。 2) 提示可以完成 UIElement，因為 UI 元素不支援隱藏狀態和提示呼叫 EndUIElement () 完成。

## <a name="predefined-ui-elements"></a>預先定義的 UI 元素

**候選清單：** 候選清單是 EA 輸入的其中一個主要 UI 元素。 這個 UI 元素提供候選清單和對應的候選字串數目來進行繪製。

**閱讀資訊視窗** [閱讀資訊] 視窗常見於中文鍵盤輸入。 它具有無法以組合字元串的形式插入檔中的階段。 某些中文輸入處理器會開啟一個小型閱讀資訊視窗，其中顯示閱讀、拼音或輸入資訊。

## <a name="the-flow-chart-of-uilessmode"></a>UILessMode 的流程圖

![顯示 U I LessMode 流程圖的圖表。](images/tsf-uilessmode-ovw1.gif)

在 pbShown by ITfUIElementMgr：： BeginUIElement 中的提示收到 **TRUE** 之後 \* ，提示不需要 [](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement)呼叫 UIElement 的 UpdateUIElement。 但是提示必須呼叫 EndUIElement () 因此 [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) 和應用程式可以追蹤 UIElement 的狀態。 提示必須在 BeginUIElement 之後呼叫 UpdateUIElement () ， () 在 pbShow 中傳回 **FALSE** \* 。 想要繪製 UI 的應用程式不會檢查 BeginUIElement () 中的內容，它只會傳回 BeginUIElement () 的顯示狀態，並開始在 UpdateUIElement () 檢查內容。 例如，候選清單 UIElement 的 update 旗標有第一個 UpdateUIElement () 的所有位。 這表示 UIElement 的內容不需要在 BeginUIElement () 備妥。

![此圖顯示當 T I P 呼叫 ' ITUIElementMgr：： BeginUIElement () ' 和 ' BeginUIElement of Application UIElementSink ' 時，會呼叫。](images/tsf-uilessmode-ovw2.gif)![顯示應用程式在 * pbShow 中傳回 FALSE 的圖表。](images/tsf-uilessmode-ovw3.gif)![uilessmode 流程圖](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>候選清單 UIElement

**關於 PageIndex：** 當 (TF \_ CLUIE STRING 設定) 時，繪製候選清單的應用程式會計算每頁的字串數目 \_ 。 當候選清單適用于 UILess 模式時，不適合變更頁面索引。 這表示，當選取範圍移至下一個頁面時，提示的候選清單應該會有分頁的行為，而不是滾動。 如果捲軸在選取範圍移動時發生，則頁面索引會變更，而應用程式需要重新計算頁面索引。 提示可能不是預期的結果。

**沒有選取專案：** 如果候選清單沒有選取專案， [**ITfCandidateListUIElement：： GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) \_ 會傳回 FALSE。 第一個參數的傳回值無效。

 

 




