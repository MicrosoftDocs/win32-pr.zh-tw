---
title: 如何裝載 MSAA 無視窗 ActiveX 控制項
description: 瞭解如何建立控制項容器，以裝載可執行 Microsoft Active Accessibility 的無視窗 Microsoft ActiveX 控制項。
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA，無視窗 ActiveX 控制項
- 無視窗 ActiveX 控制項、MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115129"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>如何裝載 MSAA 無視窗 ActiveX 控制項

瞭解如何建立控制項容器，以裝載可執行 Microsoft Active Accessibility 的無視窗 Microsoft ActiveX 控制項。 依照此處所述的步驟，您可以確保在) 用戶端應用程式 (輔助技術可存取控制容器中裝載的任何 Microsoft Active Accessibility 型無視窗控制項。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   [ActiveX控制](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>必要條件

-   C/C++
-   Microsoft Win32 和元件物件模型 (COM) 程式設計
-   無視窗的 ActiveX 控制項
-   Microsoft Active Accessibility 伺服器

## <a name="instructions"></a>指示

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>步驟1：代表無視窗控制項提供根 IAccessible 介面。

只要系統需要無視窗控制項根目錄的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標，系統就會查詢控制項容器。 為了取得指標，容器會呼叫無視窗控制項的 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) 方法的實作為。

如果控制項容器有 Microsoft Active Accessibility 的執行，則可以將無視窗控制項的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標傳回系統。

如果控制項容器具有 Microsoft 消費者介面自動化的執行，請呼叫 [**UiaProviderFromIAccessible**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) 函式來取得代表控制項的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面指標，然後將 **IRawElementProviderSimple** 介面指標傳回系統。

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>步驟2： \_ 代表無視窗控制項回應 WM GETOBJECT message。

當用戶端應用程式回應無視窗控制項所引發的 New-winevent 時，控制項容器會代表控制項接收 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息。 訊息包含引發事件之無視窗控制項的物件識別碼。

控制項容器的回應方式是查詢「擁有」物件識別碼的無視窗控制項，然後呼叫該控制項的 [**IAccessibleHandler：： AccessibleObjectFromID**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) 方法。 **AccessibleObjectFromID** 方法會傳回 UI 專案的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標，而控制項容器會傳回指向系統的指標，然後將指標轉送至用戶端應用程式。

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>步驟3：執行 IAccessibleWindowlessSite 介面。

1.  執行 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法。

    當用戶端應用程式需要無視窗控制項根提供者父系的協助工具資訊時，系統會呼叫無視窗控制項的 [**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 方法。 控制項會藉由呼叫控制項容器的 [**IAccessibleWindowlessSite：： GetParentAccessible**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) 方法來回應，這個方法會提供無視窗控制項父系的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 指標。

2.  執行 [**IAccessibleWindowlessSite：： AcquireObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange)、 [**QueryObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)和 [**ReleaseObjectIdRange**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) 方法。

    您的控制項容器必須維持物件識別碼範圍與無視窗控制項的對應。 對應可讓控制項容器識別應該回應物件識別碼之特定要求的控制項。 下表顯示將物件識別碼範圍對應至無視窗控制項的範例。

    

    | 範圍基底 | 範圍大小 | 控制   |
    |------------|------------|-----------|
    | 1000       | 500        | 控制項1 |
    | 1500       | 1000       | 控制項2 |
    | 2500       | 2000       | 控制項1 |

    

     

    控制項容器必須維持物件識別碼範圍與本身和所有無視窗子系的無視窗控制項的對應。 物件識別碼範圍不需要彼此相鄰。 此外，為了避免拒絕服務的攻擊，控制容器可以限制授與特定控制項的範圍數目。 不過，允許每個控制項有一個以上的範圍，以便讓控制項成長變得很有用。

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>步驟4：選擇性：執行 IAccessibleHostingElementProviders 介面。

如果您的控制項容器具有 Microsoft Active Accessibility server 的執行，而伺服器是協助工具樹狀結構的根，其中包含支援消費者介面自動化的無視窗 ActiveX 控制項，則請執行 [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders)介面。 **IAccessibleHostingElementProviders** 介面具有單一方法 [**GetEmbeddedFragmentRoots**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots)，可抓取控制項容器所裝載的所有消費者介面自動化無視窗 ActiveX 控制項的 [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)介面指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何裝載消費者介面自動化無視窗 ActiveX 控制項](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[無視窗 ActiveX 控制項協助工具](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 