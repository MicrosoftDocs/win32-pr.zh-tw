---
title: UI 自動化樹狀目錄概觀
description: 輔助技術產品和測試腳本會流覽 Microsoft 消費者介面自動化樹狀結構，以收集 UI 和其元素的相關資訊。
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- 消費者介面自動化，樹狀結構總覽
- 消費者介面自動化，樹狀結構的視圖
- 消費者介面自動化，樹狀結構的原始視圖
- 消費者介面自動化，樹狀結構的控制視圖
- 消費者介面自動化，樹狀結構的內容視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e1b8776f86931882acc85e2fb974ff5d1db0be266be94e391ce242ff2a497e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570393"
---
# <a name="ui-automation-tree-overview"></a>UI 自動化樹狀目錄概觀

輔助技術產品和測試腳本會流覽 Microsoft 消費者介面自動化樹狀結構，以收集 UI 和其元素的相關資訊。

消費者介面自動化樹狀結構中的根項目，表示 ( "desktop" ) 的 Windows 桌面視窗，以及其子項目代表應用程式視窗。 每個子專案都可以包含代表 UI 片段的元素，例如功能表、按鈕、工具列和清單方塊。 這些元素可以包含專案，例如清單專案。

消費者介面自動化樹狀結構不是固定的結構。 因為它可能包含數千個專案，所以很少會在 totality 中看到它。 消費者介面自動化樹狀結構的元件是以用戶端的需求建立，而樹狀結構的結構會隨著專案的加入、移動或移除而變更。

消費者介面自動化提供者會在片段中的專案之間執行導覽，以支援消費者介面自動化樹狀目錄。 片段是特定架構中專案的完整子樹，並且具有根項目 (稱為通常裝載在視窗中的 *片段根*) 。

提供者不在意從某個控制項流覽至另一個控制項。 這是由消費者介面自動化 core 管理，其使用預設視窗提供者的資訊。

本主題包含下列各節。

-   [消費者介面自動化樹狀結構的視圖](#views-of-the-ui-automation-tree)
    -   [原始視圖](#raw-view)
    -   [控制項視圖](#control-view)
    -   [內容視圖](#content-view)
-   [相關主題](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>消費者介面自動化樹狀結構的視圖

您可以篩選消費者介面自動化樹狀結構，以建立僅包含與特定用戶端相關之消費者介面自動化元素的視圖。 這種方法可讓用戶端自訂透過消費者介面自動化呈現的結構，以滿足其特定需求。

用戶端可以藉由設定範圍和篩選來自訂此視圖。 範圍是定義視圖的範圍，從基底元素開始。 例如，應用程式可能只想要尋找桌面的直接子系，或應用程式視窗的所有下階。 篩選會定義包含在此視圖中的專案類型。

消費者介面自動化提供者藉由定義專案的屬性（包括 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**IUIAutomationElement：： IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性）來支援篩選。

消費者介面自動化提供三個預設視圖：原始視圖、控制項視圖和內容視圖。 這些視圖是由執行的篩選類型所定義。 任何視圖的範圍是由應用程式所定義。 應用程式可以對屬性套用其他篩選;例如，只在控制項視圖中包含已啟用的控制項。

### <a name="raw-view"></a>未經處理的檢視

消費者介面自動化樹狀結構的原始視圖是桌面為其根目錄之 Automation 元素的完整樹狀結構。 原始視圖會緊密遵循應用程式的原生程式設計結構，而且是最詳細的可用視圖。 它也是樹狀結構其他檢視的建置基底。 因為這個視圖相依于基礎 UI 架構，所以 Windows Presentation Foundation 的原始視圖 (WPF) 按鈕與 Microsoft Win32 按鈕的原始觀點不同。

原始視圖的取得方式是藉由搜尋元素而不指定屬性，或使用 [**IUIAutomation：： RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) 來取得 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面來導覽樹狀結構。

### <a name="control-view"></a>控制項檢視

控制項檢視是未經處理檢視的子集。 它只包含將 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 屬性設定為 **TRUE** 的 UI 專案。

此控制視圖包含可提供資訊給使用者，或讓使用者執行動作的 UI 專案。 這些是自動化測試應用程式最感興趣的 UI 專案。

此控制視圖也包含對 UI 邏輯結構造成影響的非互動式 UI 專案。 這些包括專案容器，例如清單視圖標頭、工具列、功能表和狀態列。 顯示在 [控制台] 中的其他非互動式專案是在對話方塊中具有資訊和靜態文字的圖形。

非互動式專案只用于版面配置或裝飾用途，例如用來在對話方塊中配置控制項的面板，不會出現在控制項視圖中。

消費者介面自動化樹狀結構的控制項視圖會緊密對應至使用者所察覺的 UI 結構。 這可讓輔助技術產品更輕鬆地描述使用者的 UI，並協助使用者與應用程式互動。

您可以藉由搜尋將 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 屬性設定為 true 的專案，或使用 [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) 來取得用於流覽樹狀結構的 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面，來取得控制項視圖。

### <a name="content-view"></a>內容檢視

消費者介面自動化樹狀結構的內容視圖是控制視圖的子集。 它僅包含同時具有 [**IUIAutomationElement：： IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**IUIAutomationElement：： IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性設定為 **TRUE** 的 UI 專案。

內容視圖包含可在使用者介面中傳達實際資訊的 UI 專案，包括可以接收鍵盤焦點的 UI 專案，以及在 UI 專案上不是標籤的一些文字。 這些是螢幕讀取器應用程式最感興趣的 UI 專案。 例如，下拉式方塊中的值會出現在內容視圖中，因為這些值代表終端使用者所使用的資訊。

在內容視圖中，下拉式方塊和清單方塊都會表示為 UI 專案的集合，其中可以選取一個或多個專案。 其中一個專案一律會開啟，而且一個專案可以展開和折迭在內容視圖中是不相關的，因為它是設計用來顯示呈現給使用者的資料或內容。

您可以藉由搜尋將 [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) 和 [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) 屬性設定為 **TRUE** 的專案，或使用 [**IUIAutomation：： ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) 取得可流覽樹狀結構的 [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) 介面，來取得內容視圖。

下列影像顯示控制項視圖和內容視圖之間的差異。 第一個影像顯示下拉式清單中有三個專案的簡單下拉式方塊。 第二個影像顯示下拉式列示方塊 UI 專案如何出現在 UISpy.exe 應用程式的控制項和內容視圖中。

![包含三個下拉式專案的簡單下拉式方塊的螢幕擷取畫面](images/combobox.png)

![uispy.exe 應用程式的螢幕擷取畫面，其中包含下拉式方塊專案的控制項和內容視圖](images/treeviews.jpg)

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[建立 CUIAutomation 物件](uiauto-creatingcuiautomation.md)
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> <dt>

[UI 自動化基礎](entry-uiautocore-overview.md)
</dt> </dl>

 

 




