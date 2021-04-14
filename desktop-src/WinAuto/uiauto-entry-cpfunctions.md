---
title: 已淘汰的控制項模式函數
description: 已淘汰的控制項模式函數
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371933"
---
# <a name="deprecated-control-pattern-functions"></a>已淘汰的控制項模式函數

> [!Note]  
> 本節所述的控制項模式函數已被取代。 用戶端應用程式應該使用元件物件模型 (COM) 介面，如下列各節所述：
>
> -   [用戶端的消費者介面自動化元素介面](uiauto-entry-uiautoclientinterfaces.md)
> -   [用戶端的屬性條件介面](uiauto-client-propconditioninterfaces.md)
> -   [用戶端的控制項模式介面](uiauto-client-controlpatterninterfaces.md)
> -   [用戶端的事件處理介面](uiauto-client-eventhandlinginterfaces.md)
> -   [用戶端的 Proxy Factory 介面](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>本節內容



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>函式</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用 Microsoft 消費者介面自動化 COM 介面。
</blockquote>
<br/> 將消費者介面自動化專案停駐在停駐容器內要求的 <em>dockPosition</em> 。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 隱藏消費者介面自動化元素的所有子系節點、控制項或內容。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 展開畫面上的控制項，使其顯示詳細資訊。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得方格中專案的節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 傳送要求以啟動控制項，並啟始其單一明確的動作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 根據指定的屬性值，抓取包含節點內的節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 執行元素的 Microsoft Active Accessibility 預設動作。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取 <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> 物件，該物件對應至消費者介面自動化元素。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 執行 Microsoft Active Accessibility 選取專案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 設定節點的 Microsoft Active Accessibility value 屬性。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 擷取控制項特定檢視的名稱。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將控制項設定為不同的版面配置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 設定具有數位範圍之控制項的值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 滾動容器物件的內容區域，以便在容器) 的可見區域中顯示消費者介面自動化專案 (。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將內容區域的目前可見區域，以水準、垂直或兩者的方式滾動至指定的 <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 水準、垂直或兩者都會將容器滾動至特定位置。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將未選取的元素加入至控制項中的選取專案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從選取專案容器的選取範圍中移除專案。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 選取選取專案容器中的元素。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 使消費者介面自動化提供者停止接聽滑鼠或鍵盤輸入。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 使消費者介面自動化提供者開始接聽滑鼠或鍵盤輸入。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得整份檔的文字範圍。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> Ascertains 是否可以選取和取消選取文字容器的內容。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從支援文字模式的文字容器中，取得所選取文字的目前範圍。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從文字容器擷取斷續文字範圍的陣列，其中每一個文字範圍都以第一個局部可見行開頭，一直到最後一個局部可見行的尾端為止。 例如，多資料行的版面配置，其中的資料行會部分地從隱藏區的可見區域中隱藏，而內容會從一個資料行的底部流向下一個資料行的頂端。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得指定節點跨越的文字範圍。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取最接近指定螢幕座標的 (空白) 文字範圍的退化。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 藉由反白顯示對應至呼叫文字範圍 <em>開始</em> 與 <em>結束</em> 端點的補充文字，來將文字容器中反白顯示之文字的現有集合新增至支援多個不連續的選取專案。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 複製文字範圍。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 比較兩個文字範圍。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 傳回值，指出兩個文字範圍是否具有相同的端點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將文字範圍展開為較大或較小的單位，例如字元、文字、線條或頁面。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 針對支援指定之文字屬性的第一段文字，以指定的方向搜尋。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 傳回指定方向的第一個文字範圍，其中包含用戶端搜尋的文字。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得文字範圍的 text 屬性值。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取可括住範圍之周框的最小數目，每行一個矩形。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 傳回指定文字範圍內包含的所有消費者介面自動化專案。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 針對下一個涵蓋範圍的最小提供者傳回節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 傳回文字範圍中的文字，最多可達指定的字元數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將文字範圍移至用戶端所要求的指定單位數。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將一個範圍的端點移至另一個範圍的端點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 移動指定單位數的範圍端點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從支援多個不相鄰選項的文字容器中現有的選定文字集合，移除選取的文字（對應至呼叫的文字範圍 <em>TextPatternRangeEndpoint_Start</em> 和 <em>TextPatternRangeEndpoint_End</em> 端點）。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 滾動文字，讓指定的範圍可顯示在區域中。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 選取文字範圍。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將控制項切換至其下一個支援的狀態。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將元素移至螢幕上的指定位置。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 調整螢幕上元素的大小。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 旋轉螢幕上的元素。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 設定元素的文字值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 允許將虛擬項目當做使用者介面自動化項目完整存取。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 關閉開啟的視窗。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 設定視窗的視覺狀態;例如，將視窗最大化。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 導致將呼叫程式碼封鎖指定的時間，或直到相關聯的處理序進入閒置狀態 (就看何者先完成)。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化用戶端](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





