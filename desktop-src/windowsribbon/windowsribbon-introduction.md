---
title: Windows 功能區架構簡介
description: Windows 功能區架構是一種豐富的命令呈現系統，提供了傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，關於
- 功能區，關於
- Windows 功能區，元件
- 功能區、元件
- Windows 功能區，views
- 功能區、視圖
- Windows 功能區，架構
- 功能區，架構
- Windows 功能區，Api
- 功能區，Api
- Windows 功能區，安全性
- 功能區，安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ac5c3acccf1c48a54f93b1752729067e63e4c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104563838"
---
# <a name="introducing-the-windows-ribbon-framework"></a>Windows 功能區架構簡介

Windows 功能區架構是一種豐富的命令呈現系統，提供了傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。

-   [新的命令範例](#a-new-command-paradigm)
-   [檢視](#views)
    -   [功能區視圖](#the-ribbon-view)
    -   [CoNtextPopup 視圖](#the-contextpopup-view)
-   [功能區架構](#ribbon-architecture)
    -   [功能區 Api](#the-ribbon-apis)
    -   [安全性和隱私權](#security-and-privacy)
    -   [存取範圍和當地語系化](#accessibility-and-localization)
-   [結論](#conclusion)
-   [相關主題](#related-topics)

## <a name="a-new-command-paradigm"></a>新的命令範例

功能區架構是 Microsoft Win32 Api 的集合，可支援 Windows 開發人員的新 UI 功能。

這種豐富的新式 UI 命令架構提供：

-   輕鬆地為新的功能區架構應用程式，並直接遷移現有的 Win32 應用程式。
-   跨功能區應用程式一致的外觀和行為。
-   遵循適用于透過協助工具標準的第一層 Windows 體驗的 Windows UI 指導方針、視覺化樣式 (主題) 支援、自動高對比調整，以及每英寸的高點 (DPI) 認知。

功能區架構是由兩個主要的 UI 元件所組成：

-   功能區命令列是由快速存取工具列 (QAT) ，它會公開和醒目顯示使用者或應用程式所指定的各種功能區命令，以及包含應用程式功能表、標準或內容索引標籤的索引標籤列，以及 [說明] 按鈕。
-   豐富的內容功能表系統。

宣告式 XML 和原生 COM 介面的組合是用來分離這些元件的呈現和功能。

## <a name="views"></a>檢視

功能區架構、功能區命令列和內容功能表系統的主要 UI 元件，在結構上是透過 *視圖* 來區分。 架構支援兩種視圖： [**功能區**](windowsribbon-element-ribbon.md) 視圖和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖。

### <a name="the-ribbon-view"></a>功能區視圖

[**功能區**](windowsribbon-element-ribbon.md)視圖的 UI 是功能區架構的主要功能，並提供在 Windows 應用程式中呈現命令的下一代使用者體驗。

功能區是一個命令列，可透過應用程式視窗頂端的一系列索引標籤，來公開應用程式的主要功能。 它類似于 Microsoft Office 2007 流暢 UI 的功能和外觀。 功能區提供以直覺的對應，說明通常是標準 Windows 功能表系統的命令探索的試驗和錯誤程式。 功能區已針對效率和可搜尋性進行優化，可透過標準控制項、資源庫和即時預覽的系統，以最少的滑鼠點擊和按鍵來加速尋找、瞭解及使用命令。

下圖說明適用于 Windows 7 的 Paint 中的功能區架構執行。

![螢幕擷取畫面，顯示 windows 7 的 [油漆] 中的功能區執行。](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>CoNtextPopup 視圖

[**CoNtextPopup**](windowsribbon-element-contextpopup.md) View （透過 [內容](windowsribbon-controls-contextpopup.md)快顯控制項）提供的內容功能表系統，比舊版 Windows 應用程式所提供的更豐富。 您只能部署內容快顯視窗，以支援功能區，功能區架構不支援獨立的內容快顯視窗。

## <a name="ribbon-architecture"></a>功能區架構

相較于傳統以控制項為基礎的 Windows UI 開發模型，Windows 功能區架構 UI 開發是以更抽象的命令概念為基礎。 藉由將焦點放在與控制項相關聯的命令（而不是控制項本身），架構就能夠視需要自動調整 UI，以回應從功能區主機應用程式取出的命令執行狀態。

使用功能區架構的應用程式會公開命令，而不會在 UI 中呈現該命令的詳細資料。 這有時稱為以意圖為基礎的 UI 模型。 [**命令類型**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)、其屬性和其資源會定義應用程式命令的意圖。 例如，滑鼠輸入、鍵盤輸入或甚至是搖動 gyroscopic 裝置可能會導致執行相同的命令，而應用程式只在意執行命令，而不是叫用該命令的方式。

功能區架構可讓您以兩種不同的開發結構分隔功能，以提供這種彈性： Extensible Application Markup Language (XAML) 型標記語言來宣告控制項和功能區實的視覺化配置，以及 c + + COM 型介面，可在執行時間初始化架構和處理事件。 這項區別可讓 UI 開發人員和設計人員單獨負責功能區應用程式的外觀，而核心功能仍然是軟體工程師的領域。

如需詳細資訊，請參閱 [瞭解命令和控制項](windowsribbon-commandscontrols.md)。

### <a name="the-ribbon-apis"></a>功能區 Api

功能區 Api 會在 View 和功能區主應用程式之間提供必要的連接。 這些 Api 包含下列介面和屬性索引鍵：

-   功能區架構所執行的一組 COM 介面，用來執行 UI 服務。

    

    | 介面                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUICoNtextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | 定義 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖核心功能的方法。                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | 定義支援 [**功能區**](windowsribbon-element-ribbon.md) 和 [**CoNtextPopup**](windowsribbon-element-contextpopup.md) 視圖核心功能的方法。                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | 定義用於指定 [**功能區**](windowsribbon-element-ribbon.md) 視圖之設定和屬性的方法。                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | 定義方法，以抓取屬性索引鍵所識別的值。 這個介面是由功能區架構所執行，而且也會由主應用程式針對專案資源庫的 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) 物件中的每個專案執行。<br/> 由主應用程式執行時，這個介面所定義的方法會用來在 [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)中取得所選取專案的屬性索引鍵值。<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | 定義在執行時間動態操作集合型控制項（例如功能區 QAT 和以集合為基礎的資源 [庫](ribbon-controls-galleries.md)）的方法。                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | 定義用來抓取影像以顯示在功能區 UI 中的方法。                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | 定義用來建立 [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) 物件的 factory 方法。                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   功能區主機應用程式所執行的一組 COM 介面，架構會呼叫這些介面來回應 UI 變更。

    

    | 介面                                                                                  | 描述                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | 定義功能區架構的應用程式回呼進入點方法。                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | 定義用來從功能區架構收集命令資訊和處理命令事件的方法。 |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | 定義在執行時間處理集合變更所需的方法。                                   |

    

     

-   一組屬性索引鍵，定義應用程式以程式設計方式控制的 UI 屬性。

    

    | 屬性索引鍵類型                                                  | Description                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [集合](windowsribbon-reference-properties-collection.md)    | 定義以功能區集合為基礎之控制項的屬性。 |
    | [色彩選擇器](windowsribbon-reference-properties-colorpicker.md) | 定義功能區色彩選擇器控制項的屬性。     |
    | [字型](windowsribbon-reference-properties-fontcontrol.md)         | 定義功能區 FontControl 的屬性。           |
    | [全球](windowsribbon-reference-properties-framework.md)         | 定義功能區架構的全域屬性。      |
    | [Resource](windowsribbon-reference-properties-resource.md)        | 定義功能區資源屬性。                      |
    | [功能區](windowsribbon-reference-properties-ribbon.md)            | 定義功能區視圖屬性。                          |
    | [State](windowsribbon-reference-properties-state.md)              | 定義功能區控制項狀態或內容的屬性。  |

    

     

### <a name="security-and-privacy"></a>安全性和隱私權

功能區架構 DLL (uiribbon.dll) 在同進程中執行，而且具有與主應用程式相同的許可權。 功能區只接受主機應用程式做為輸入或使用者輸入（來自嚴格限制的控制項），例如微調和可編輯的下拉式方塊。

此外，除了由主應用程式提供的資訊之外，架構也不會永久儲存任何資訊，或是由使用者透過「加入宣告 Windows 客戶經驗計畫」所授權) 收集 (。

### <a name="accessibility-and-localization"></a>存取範圍和當地語系化

功能區架構會執行 Microsoft Active Accessibility，以提供可高度存取的 UI。 架構會自動以有效且有用的資訊來填入相關的 Microsoft Active Accessibility 屬性，以大幅降低開發人員為所有使用者提供內含體驗的負擔。

如需功能區架構中協助工具的詳細資訊，請參閱 [使用 2007 Office 流暢消費者介面中的 Active Accessibility](/previous-versions/office/developer/office-2007/bb404170(v=office.12))。

此外，功能區架構也是 Windows 功能，因此會針對 Windows 支援的所有語言進行當地語系化。 不過，開發人員必須負責當地語系化自己的特定應用程式資源。

## <a name="conclusion"></a>結論

功能區是一種全新且吸引人的命令展示，應用程式開發人員、架構設計人員和設計人員在設計和建立新的應用程式或更新現有的應用程式時，應該考慮到。

[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可討論主題，並詢問與開發執行 Windows 功能區架構的應用程式有關的問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用功能區標記宣告命令和控制項](windowsribbon-schema.md)
</dt> <dt>

[功能區使用者體驗指導方針](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[功能區設計流程](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

