---
title: 已淘汰的節點函式
description: 已淘汰的節點函式
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933684"
---
# <a name="deprecated-node-functions"></a>已淘汰的節點函式

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
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用 Microsoft 消費者介面自動化 COM 介面。
</blockquote>
<br/> 在消費者介面自動化樹狀結構中的節點上加入事件的接聽程式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將視窗加入至事件接聽程式。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 用戶端所執行的函式，當用戶端已訂閱的事件引發時，消費者介面自動化會呼叫此函數。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從事件接聽程式中移除視窗。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取符合搜尋準則的一或多個消費者介面自動化節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得可傳遞給用戶端的錯誤字串。 用戶端不直接使用這個方法。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取 <em>控制項模式</em>。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取消費者介面自動化屬性的值。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取根消費者介面自動化節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取消費者介面自動化節點的執行時間識別碼。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 更新屬性值和控制項模式的快取。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 型別取得控制項模式物件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 類型取得文字範圍。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從 <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>VARIANT</strong></a> 型別取得 HUIANODE。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得可用於需要 PROPERTYID、PATTERNID、CONTROLTYPEID、TEXTATTRIBUTEID 或 EVENTID 之方法中的整數識別碼。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 在消費者介面自動化樹狀結構中流覽，選擇性地取出快取的資訊。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 針對目前具有輸入焦點的 UI 元素，抓取消費者介面自動化節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取與視窗相關聯的消費者介面自動化節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 針對位於指定點的專案，抓取消費者介面自動化節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 抓取原始元素提供者的消費者介面自動化節點。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從記憶體中刪除節點。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從記憶體刪除配置的模式物件。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 由消費者介面自動化呼叫的應用程式定義函式，可取得專案的用戶端提供者。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 取得布林值，這個值會指定矩形是否將其所有座標設定為0。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將 <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> 結構的元素設定為0。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 註冊由消費者介面自動化呼叫的應用程式定義方法，以取得元素的提供者。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 移除消費者介面自動化樹狀結構中節點上的事件接聽程式。<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 將輸入焦點設定為 UI 中的指定元素。<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
這個函數已被取代。 用戶端應用程式應該改用消費者介面自動化 COM 介面。
</blockquote>
<br/> 從記憶體中刪除配置的文字範圍物件。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[消費者介面自動化用戶端](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

