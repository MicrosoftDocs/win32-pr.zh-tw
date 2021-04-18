---
title: UI 自動化概觀
description: Microsoft 消費者介面自動化是適用于 Windows 的協助工具架構。
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- 消費者介面自動化，關於
- 消費者介面自動化，協助工具
- 消費者介面自動化，元件
- 消費者介面自動化，提供者 API
- 消費者介面自動化，用戶端 API
- 消費者介面自動化，標頭檔
- 消費者介面自動化，模型
- components
- 協助工具
- 提供者 API
- 用戶端 API
- 標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ea29b0abd4c6ed791ae3195f36a0f8184c8596
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374331"
---
# <a name="ui-automation-overview"></a>UI 自動化概觀

Microsoft 消費者介面自動化是適用于 Windows 的協助工具架構。 它可讓您以程式設計方式存取桌面上大部分的 UI 元素。 它可讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊給使用者，以及透過標準輸入以外的方式操作 UI。 消費者介面自動化也可讓自動化測試腳本與 UI 互動。

在 Windows XP 中，消費者介面自動化是 Microsoft .NET Framework 的第一次提供。 雖然非受控 c + + API 也會在當時發佈，但因為互通性問題，所以用戶端函式的實用性受到限制。 針對 Windows 7，API 已在元件物件模型中重寫 (COM) 。

> [!Note]  
> 雖然在舊版消費者介面自動化引進的程式庫函式仍會記載，但不應該用於新的應用程式。

 

您可以撰寫消費者介面自動化的用戶端應用程式，以確保這些應用程式可在多個 Microsoft Windows 控制項架構上運作。 消費者介面自動化 core 會遮罩架構中各種不同部分的架構差異。 例如，Windows Presentation Foundation (WPF) 按鈕的 [ **內容** ] 屬性、[Microsoft Win32] 按鈕的 [ **標題** ] 屬性，以及 HTML 影像的 **ALT** 屬性，都會對應到消費者介面自動化視圖中的單一屬性 [ **名稱**]。

消費者介面自動化在 Windows XP、Windows Server 2003 和更新版本的作業系統中提供完整功能。

消費者介面自動化提供者是在控制項上執行消費者介面自動化支援的元件，並透過內建的橋接服務提供 Microsoft Active Accessibility 用戶端應用程式的一些支援。

> [!Note]  
> 消費者介面自動化不會啟用由不同使用者透過 [ **執行身份** ] 命令啟動的進程之間的通訊。

 

本主題包含下列各節。

-   [消費者介面自動化元件](#ui-automation-components)
-   [消費者介面自動化標頭檔](#ui-automation-header-files)
-   [使用者介面自動化模型](#ui-automation-model)
-   [相關主題](#related-topics)

## <a name="ui-automation-components"></a>消費者介面自動化元件

消費者介面自動化有四個主要元件，如下表所示。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>元件</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>提供者 API</td>
<td>由消費者介面自動化提供者所執行的一組 COM 介面。 消費者介面自動化提供者為物件，可提供 UI 元素的相關資訊，並回應程式設計的輸入。</td>
</tr>
<tr class="even">
<td>用戶端 API</td>
<td>一組 COM 介面，可讓用戶端應用程式取得 UI 的相關資訊，並將輸入傳送給控制項。
<blockquote>
[!Note]<br />
已淘汰的 <a href="uiauto-entry-cpfunctions.md">控制項模式函數</a> 和已淘汰的 <a href="uiauto-entry-uianodefunctions.md">節點</a> 函式中所述的函式已被取代。 相反地，用戶端應用程式應該使用 <a href="uiauto-entry-uiautoclientinterfaces.md">用戶端消費者介面自動化元素介面</a>中所述的消費者介面自動化 COM 介面。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>UIAutomationCore.dll</td>
<td>執行時間程式庫（有時稱為消費者介面自動化 core）可處理提供者與用戶端之間的通訊。</td>
</tr>
<tr class="even">
<td>Oleacc.dll</td>
<td>Microsoft Active Accessibility 和 proxy 物件的執行時間程式庫。 此程式庫也會提供 Microsoft Microsoft Active Accessibility 用來消費者介面自動化 Proxy 以支援 Win32 控制項的 proxy 物件。</td>
</tr>
</tbody>
</table>



 

使用消費者介面自動化的方式有兩種：使用提供者 API 來建立自訂控制項的支援，以及建立使用消費者介面自動化核心來與進行通訊的用戶端應用程式，並取得 UI 元素的相關資訊。 視您著重的部分而定，您應該參閱本文件的不同部分。 如果您需要建立自訂控制項的支援，請參閱 [消費者介面自動化提供者程式](uiauto-providerportal.md)設計人員手冊。 如果您需要與 UI 元素通訊或取得相關資訊，請參閱 [消費者介面自動化用戶端程式設計人員手冊](uiauto-clientportal.md)。

## <a name="ui-automation-header-files"></a>消費者介面自動化標頭檔

消費者介面自動化 API 是在 Windows 軟體開發套件 (SDK) 隨附的數個不同 C/c + + 標頭檔中定義。 下表說明消費者介面自動化標頭檔案：



| 標頭檔           | Description                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uiautomationclient.dll。h  | 定義消費者介面自動化用戶端所使用的介面和相關的程式設計項目。                                                                                                                                                                                           |
| UIAutomationCore。h    | 定義消費者介面自動化提供者所使用的介面和相關的程式設計項目。                                                                                                                                                                                         |
| UIAutomationCoreApi。h | 定義消費者介面自動化用戶端和提供者所使用的一般常數、Guid、資料類型和結構。 它也包含已被取代之節點和控制項模式函數的定義。                                                                                    |
| UIAutomation。h        | 包含所有其他的消費者介面自動化標頭檔。 由於大部分的消費者介面自動化應用程式都需要所有消費者介面自動化標頭檔中的元素，因此最好將 UIAutomation 包含在消費者介面自動化應用程式專案中，而不是個別包含每個檔案。 |



 

如果您正在開發使用消費者介面自動化 API 的應用程式，您應該在專案中包含 UIAutomation。 如果您的應用程式支援 Microsoft Active Accessibility，請包含 Oleacc .h 標頭檔。 使用 Guid 的消費者介面自動化應用程式也需要 Initguid .h 標頭檔。 如有需要，Initguid 應該包含在 UIAutomation 之前。

## <a name="ui-automation-model"></a>使用者介面自動化模型

消費者介面自動化會將 UI 的每個元素公開給用戶端應用程式，以做為 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面所代表的物件。 項目包含於樹狀結構中，且桌面是根項目。 用戶端可將樹狀結構之未經處理的檢視篩選為控制項檢視或內容檢視。 使用 Windows SDK 隨附的 [檢查](inspect-objects.md) 應用程式，即可輕鬆地查看結構的這些標準觀點。 應用程式也可以建立自訂檢視。

消費者介面自動化專案會公開其所代表之控制項或 UI 專案的屬性。 其中一個屬性是控制項類型，它會將控制項或 UI 元素的基本外觀和功能定義為單一可辨識的實體，例如按鈕或核取方塊。 如需控制項類型的詳細資訊，請參閱 [消費者介面自動化控制項類型總覽](uiauto-controltypesoverview.md)。

此外，消費者介面自動化元素會公開一或多個控制項模式。 控制項模式提供特定控制項類型專屬的一組屬性。 控制項模式也會公開方法，讓用戶端應用程式取得專案的詳細資訊，並提供輸入給元素。 如需控制項模式的詳細資訊，請參閱 [F:System.Windows.Automation.ValuePatternIdentifiers.ValueProperty](uiauto-controlpatternsoverview.md)。

> [!Note]  
> 控制項類型和控制項模式之間沒有一對一的對應關係。 控制項模式可由多個控制項類型所支援，且控制項可支援多個控制項模式，每個控制項都會公開其行為的不同層面。 例如，下拉式方塊擁有至少兩個控制項模式：其中一個代表展開和折疊的能力，另一個則代表選取機制。 不過，控制項只能展示單一控制項類型。

 

消費者介面自動化透過事件提供用戶端應用程式的資訊。 不同于 WinEvents，消費者介面自動化事件不是以廣播機制為基礎。 消費者介面自動化用戶端會註冊特定的事件通知，並且可要求將特定屬性和控制項模式資訊傳遞給其事件處理常式。 此外，消費者介面自動化事件包含引發它之專案的參考。 提供者可以選擇引發事件來改善效能，取決於是否有任何用戶端接聽。 如需事件的詳細資訊，請參閱 [UI Automation Events Overview](uiauto-eventsoverview.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化控制項類型概觀](uiauto-controltypesoverview.md)
</dt> <dt>

[UI 自動化控制項模式概觀](uiauto-controlpatternsoverview.md)
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> </dl>

 

 





