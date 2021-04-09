---
title: 消費者介面技術
description: 本主題提供 Microsoft 技術的簡短問卷，以開發適用于 Windows 應用程式的 Ui。
ms.assetid: 5ecbaaf0-704e-4c27-b3ce-b5436e577d62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d9343672d064cf073ea8018758b90083f440bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933528"
---
# <a name="user-interface-technologies"></a>消費者介面技術

本主題提供 Microsoft 技術的簡短問卷，以開發適用于 Windows 應用程式的 Ui。 其中提供的資訊可協助您判斷是否要使用特定技術，並找出您可以在何處找到更多相關資訊。

本主題說明下列技術：

-   [非受控應用程式的消費者介面技術](#user-interface-technologies-for-unmanaged-applications)
    -   [Windows 控制項](#windows-controls)
    -   [視覺化樣式](#visual-styles)
    -   [Windows 功能區架構](#windows-ribbon-framework)
    -   [Windows 動畫管理員](#windows-animation-manager)
    -   [桌面視窗管理員](#desktop-window-manager)
    -   [Windows 自動化 API](#windows-automation-api)
    -   [Speech API](#speech-api)
    -   [放大 API](#magnification-api)
    -   [資源編譯器](#resource-compiler)
-   [受控應用程式的消費者介面技術](#user-interface-technologies-for-managed-applications)
    -   [Windows Forms](#windows-forms)
    -   [Windows Presentation Foundation](#windows-presentation-foundation)
    -   [Silverlight](#silverlight)
    -   [Expression Blend 3 + SketchFlow](/windows)
    -   [受控應用程式的消費者介面自動化](#ui-automation-for-managed-applications)

## <a name="user-interface-technologies-for-unmanaged-applications"></a>非受控應用程式的消費者介面技術

本節說明用於開發非受控 Windows 應用程式 Ui 的 Microsoft 技術。 這些技術適用于熟悉 WindowsAPI 程式設計概念的經驗豐富 C/c + + 開發人員，以及使用 Microsoft Windows 軟體開發套件 (SDK) 的人員。 有些技術有其他必要條件，例如，圖形程式設計問題的知識，或熟悉元件物件模型的基本概念， (COM) 程式設計。

### <a name="windows-controls"></a>Windows 控制項

Windows 控制項是與另一個視窗一起使用的使用者介面元素 (通常是用戶端視窗或對話方塊，) 讓使用者與應用程式互動。 組成傳統 Windows 應用程式 UI 的許多元素都是 Windows 控制項，包括功能表、捲軸、按鈕、清單方塊、樹狀檢視等專案。

所有 Windows 版本都支援 windows 控制項。 不過，因為支援控制項的執行時間元件在經過一段時間後就已演變，所以在較舊版本中不支援某些在較新版本中引進的控制項和功能。 應用程式必須偵測版本並只使用可用的功能。

如果您想要針對在各種 Windows 版本上執行的非受控 Windows 應用程式建立傳統 UI，請使用 Windows 控制項。

如需詳細資訊，請參閱 [Windows 控制項](../controls/window-controls.md)。

### <a name="visual-styles"></a>視覺化樣式

視覺化樣式是控制面板的規格。 例如，視覺效果樣式可以定義控制項的整體外觀，並讓軟體發展人員設定這些控制項的視覺化介面，以協調應用程式的外觀。 此外，視覺效果樣式為所有 Windows 應用程式提供一種機制，以將應用程式的外觀標準化。

Windows XP 和更新版本支援視覺化樣式，而且只會影響標準 Windows 控制項和 Microsoft Win32 通用控制項的外觀。

如果您需要變更標準 Windows 控制項和通用控制項的外觀，以符合應用程式 UI 的外觀，您應該使用視覺化樣式。

如需詳細資訊，請參閱 [視覺化樣式](../controls/themes-overview.md)。

### <a name="windows-ribbon-framework"></a>Windows 功能區架構

Windows 功能區架構是以 Windows 為基礎的應用程式的豐富命令呈現系統。 它是由功能區命令列所組成，可透過應用程式視窗頂端的一系列索引標籤來公開應用程式的主要功能，以及內容功能表系統。 下列 Windows 版本支援 Windows 功能區架構：

-   Windows Vista Service Pack 2 (SP2) 和 Windows Vista 的平臺更新
-   Windows 7 和更新版本
-   Windows Server 2008 R2
-   Windows Server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 的平臺更新

如果您想要執行的命令 UI 是傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的替代方案，您應該使用 Windows 功能區架構。

Windows 功能區架構適用于對 COM 程式設計熟練的開發人員。

如需詳細資訊，請參閱 [Windows 功能區架構](../windowsribbon/-uiplat-windowsribbon-entry.md)。

### <a name="windows-animation-manager"></a>Windows 動畫管理員

Windows 動畫管理員藉由提供強大的動畫引擎和標準化的程式設計介面，來支援 UI 元素的動畫。 平臺可簡化 UI 動畫順序的開發和維護，並可讓開發人員執行一致且直覺的 UI 動畫。 Windows 動畫可與任何圖形平台搭配使用，包括 Direct2D、Microsoft Direct3D 或 Windows GDI +。

Windows Vista 與 windows vista （含 SP2）的平臺更新，以及 windows Vista 和 Windows 7 （含）以後版本的平臺更新，都支援 Windows 動畫架構。

如果您想要將動畫順序新增至非受控 Windows 應用程式的 UI，您應該使用 Windows 動畫管理員。

如需詳細資訊，請參閱 [Windows 動畫管理員](../uianimation/-main-portal.md)。

### <a name="desktop-window-manager"></a>桌面視窗管理員

桌面視窗管理員 (DWM) 是 Windows 執行時間元件，可支援桌面撰寫，這是 Windows Vista 中引進的一項功能。 透過桌面電腦群組合，DWM 可在 UI 中啟用視覺效果，例如半透明視窗框架、立體視窗轉換動畫、Windows Flip 和 Windows Flip3D，以及高解析度支援。

DWM 會公開 API，以控制與桌面組合相關聯的許多視覺效果。 例如，應用程式可以顯示縮圖、將半透明和模糊效果套用至最上層視窗的工作區、控制在非 windows 用戶端區域中使用的透明度和轉換效果等等。

Windows Vista 和 Windows Server 2008 支援 DWM。

如果您的應用程式需要存取和控制與桌面組合相關聯的視覺效果，您應該使用 DWM。

如需詳細資訊，請參閱 [桌面視窗管理員](../dwm/dwm-overview.md)。

### <a name="windows-automation-api"></a>Windows 自動化 API

Windows 自動化 API 可協助開發人員建立可供最廣泛的物件存取的應用程式，包括具有視覺、聽力或動作障礙的人。 API 的運作方式是公開構成應用程式使用者介面之元素的相關資訊。 輔助技術應用程式（例如螢幕讀取器）可以使用此資訊，以殘障人士可使用的方式呈現 UI。

Windows 自動化 API 是由兩個不同的 API 架構（Microsoft Active Accessibility 和 Microsoft 消費者介面自動化所組成）。 Microsoft Active Accessibility 是在 Windows 95 中引進為平臺增益集的舊版 API。 消費者介面自動化是 Microsoft Active Accessibility 的後續版本，而且是消費者介面自動化規格的 Windows 執行。

Windows XP 和 Windows Server 2003 內建 Microsoft Active Accessibility 的完整支援。 Windows NT 4.0 （含 Service Pack 6） (SP6) 和更新版本，以及 Windows 98 Microsoft Active Accessibility 也支援。 下列作業系統支援消費者介面自動化： Windows XP、Windows Server 2003、Windows Server 2003 R2、Windows Vista、Windows 7、Windows Server 2008 和 Windows Server 2008 R2。

如果您的應用程式包含自訂控制項或其他自訂 UI 功能，您應該使用 Windows 自動化 API 來確保自訂控制項和功能都能完整存取。 一般情況下，開發人員需要對 COM 物件和介面、Unicode 和 Windows API 程式設計有中等程度的瞭解。

如需詳細資訊，請參閱 [Windows AUTOMATION API](../winauto/windows-automation-api-portal.md)。

### <a name="speech-api"></a>Speech API

Microsoft Speech API (SAPI) 提供應用程式和語音引擎之間的高階介面。 SAPI 會執行控制及管理各種語音引擎即時作業所需的所有低層級詳細資料。

這兩種類型的 SAPI 引擎為文字轉換語音 (TTS) 系統和語音辨識器。 TTS 系統使用綜合語音將文字字串和檔案合成至語音音訊。 語音辨識器會將人類的語音轉換成可讀取的文字字串和檔案。

如果您想要執行一個 UI，讓使用者除了鍵盤、滑鼠和顯示器等標準輸入設備之外，還能透過 TTS 和語音辨識來與您的應用程式互動，您應該使用 SAPI。

如需詳細資訊，請參閱 [Microsoft SPEECH API (SAPI) 5.4](/previous-versions/windows/desktop/ee125663(v=vs.85))。

### <a name="magnification-api"></a>放大 API

 (MAPI) 的放大 API 可用來放大螢幕的部分，並套用色彩效果和其他轉換。 此 API 主要適用于輔助技術應用程式，可以放大螢幕的各個部分，讓他們更容易看到。

Windows Vista、Windows 7、Windows Server 2008 和 Windows Server 2008 R2 都支援 MAPI。 它適用于熟悉圖形程式設計概念的開發人員。

如需詳細資訊，請參閱 [放大 API](/previous-versions/windows/desktop/magapi/entry-magapi-sdk)。

### <a name="resource-compiler"></a>資源編譯器

Microsoft Windows 資源編譯器是一種應用程式開發工具，可用來將 UI 和其他資源新增至 Windows 應用程式。 資源是應用程式所使用的任何無法執行的資料，並包含對話方塊、功能表、字串、資料指標、圖示、點陣圖等專案。 資源編譯器包含在 Microsoft Visual Studio 和 Windows SDK 中。

如需詳細資訊，請參閱[資源編譯器](../menurc/resource-compiler.md) \(英文\)。

## <a name="user-interface-technologies-for-managed-applications"></a>受控應用程式的消費者介面技術

本節說明針對在 .NET Framework 內容中執行的受控 Windows 應用程式開發 Ui 的 Microsoft 技術。 如需詳細資訊，請參閱 [.Net 開發](/previous-versions/ff361664(v=vs.100))。

### <a name="windows-forms"></a>Windows Forms

Windows Forms 是一種圖形化應用程式開發介面，用來建立以 .NET Framework 為基礎的受控 Windows 應用程式。 在 Windows Forms 中，表單是您向使用者顯示資訊的視覺介面，以及從中接收使用者輸入的視覺介面。

您可以藉由將控制項新增至表單，並開發使用者動作的回應（例如滑鼠點擊或按鍵按下）來建立 Windows Forms 應用程式。 控制項是顯示資料或接受資料輸入的離散 UI 元素。 Windows Form 包含可讓您加入表單中的各種控制項：顯示文字方塊、按鈕、下拉式清單方塊、選項按鈕甚至網頁的控制項。 Windows Forms 也支援建立自訂控制項。

如需詳細資訊，請參閱 [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100))。

### <a name="windows-presentation-foundation"></a>Windows Presentation Foundation

Windows Presentation Foundation (WPF) 是 [Windows Forms](/previous-versions/dotnet/netframework-4.0/cc656767(v=vs.100))的後續版本。 WPF 是一種呈現系統，可在 Windows 用戶端應用程式和瀏覽器裝載的應用程式中建立和轉譯使用者介面。 WPF 的核心是與解析度無關並以向量為基礎的轉譯引擎，其建置目的是為了利用現代化圖形硬體。 WPF 利用一組完整的應用程式開發功能來擴充核心，包括 XAML (Extensible Application Markup Language)、控制項、資料繫結、版面配置、2D 和 3D 圖形、動畫、樣式、範本、文件、媒體、文字，以及印刷樣式。

WPF 隨附於 .NET Framework，因此您可以建置納入 .NET Framework 類別庫之其他項目的應用程式。 Windows Vista、Windows 7、Windows Server 2008、Windows Server 2008 R2 支援 WPF，也適用于 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003。

如需詳細資訊，請參閱 [Windows Presentation Foundation](/dotnet/framework/wpf/)。

### <a name="silverlight"></a>Silverlight

Microsoft Silverlight 是一種功能強大的開發平臺，可針對 Web、桌上型電腦和行動裝置建立豐富的媒體應用程式和商務應用程式。

根據 .NET Framework，免費的 Silverlight 外掛程式可跨多個瀏覽器、裝置和作業系統運作，以將新的互動功能帶入 Web。 Silverlight 具有廣泛的版面配置和樣式選項、強大的通訊協定、穩固的資料存取，以及對使用者互動和高定義媒體的支援，可協助您建立快速、流暢且視覺化的豐富客戶體驗。 您可以使用 Microsoft Web Platform、Visual Studio 和 Expression Studio 快速開發 Silverlight 應用程式。

如需詳細資訊，請參閱 [Microsoft Silverlight](/previous-versions/windows/silverlight/dotnet-windows-silverlight/cc838158(v=vs.95))。

### <a name="expression-blend-3--sketchflow"></a>Expression Blend 3 + SketchFlow

Expression Blend 3 + SketchFlow 是一種視覺化檢視，可用於設計、建立原型，以及建立適用于 WPF 和 Silverlight 桌面和 web 應用程式的複雜使用者介面。 您可以藉由繪製圖形、繪製控制項（例如按鈕和清單方塊）來建立應用程式，讓應用程式的各部分回應滑鼠點擊和其他使用者輸入，並將所有專案的樣式設定為獨特的外觀。

如需詳細資訊，請參閱 [使用 SketchFlow 建立原型](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30))。

### <a name="ui-automation-for-managed-applications"></a>受控應用程式的消費者介面自動化

消費者介面自動化是 Windows 的協助工具架構，可在所有支援 WPF 的作業系統上使用。

消費者介面自動化可讓您以程式設計方式存取桌面上大部分的 UI 元素，讓輔助技術產品（例如螢幕讀取器）提供使用者介面的相關資訊，並透過標準輸入以外的方式操作 UI。 消費者介面自動化也可讓自動化測試腳本與 UI 互動。

如需詳細資訊，請參閱 [Managed 應用程式的消費者介面自動化](/dotnet/framework/ui-automation/)。

 

 