---
title: 視覺化樣式總覽
description: 本主題說明視覺化樣式，並識別支援這些樣式的 Windows 元件。 此外，也會說明在應用程式中使用視覺化樣式所必須採取的步驟。
ms.assetid: 5B5D7BB6-684F-478D-BF5F-B8D18BBCFF2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5663730c752fbf16c4f229a031eafa0c65bb9dbb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463941"
---
# <a name="visual-styles-overview"></a>視覺化樣式總覽

本主題說明視覺化樣式，並識別支援這些樣式的 Windows 元件。 此外，也會說明在應用程式中使用視覺化樣式所必須採取的步驟。 本主題包含下列章節：

-   [Themes and Visual Styles](#themes-and-visual-styles)
-   [視覺化樣式元件](#visual-styles-components)
-   [支援視覺效果樣式的應用程式需求](#application-requirements-for-supporting-visual-styles)
-   [相關主題](#related-topics)

## <a name="themes-and-visual-styles"></a>Themes and Visual Styles

Windows 包含數個功能，可讓使用者量身打造 UI 來滿足其個別的需求和喜好設定。 這些功能包括在 Microsoft Plus 中引進的主題 適用于 Windows 95。 主題是使用者可選取的設定集合，其中包含背景圖樣、游標、字型、音效和圖示。 以下是主題的一些特性。

-   主題設定是在具有類似 win.ini 檔案格式的主題檔案中指定。
-   獨立軟體廠商 (ISV) 可以使用產品來建立並散發主題檔案。
-   在 Windows Vista 之前的版本中，主題檔案會顯示在 [顯示] 控制台的 [主題] 索引標籤上。 在 Windows Vista 和更新版本中，主題會顯示在 [個人化] 控制台中。

如需主題檔案的詳細資訊，請參閱 [主題檔案格式](themesfileformat-overview.md)。

視覺化樣式是定義 Windows 通用控制面板的規格。 視覺化樣式與主題相關聯;亦即，主題檔案包含一個區段，可指定當特定主題為使用中時要套用的視覺化樣式。 以下是視覺化樣式的部分特性。

-   使用者可以選取不同的主題，隨時變更視覺效果樣式。
-   您必須使用視覺化樣式 API，將目前使用中的視覺效果樣式套用至應用程式的自訂或主控描繪控制項（如果有的話）。
-   定義視覺效果樣式的資訊會儲存在 msstyles 檔案中。 Microsoft 不支援 msstyles 檔案的撰寫。


下圖顯示一個簡單的對話方塊，其中包含工作列，在使用 Windows Aero 主題但沒有透明度的 Windows 7 桌面上。 因為應用程式未設定為使用視覺化樣式，所以不論主題設定為何，按鈕都會顯示相同。

![對話方塊的螢幕擷取畫面，其中包含不使用透明度的按鈕](images/tb-wostyles.png)

相反地，下圖顯示相同桌面上的相同對話方塊，但這次應用程式已設定為使用視覺化樣式。 請注意工作區中按鈕的不同外觀。 按鈕看起來會不同，因為系統已套用 Aero 主題中定義的視覺效果樣式。

![對話方塊的螢幕擷取畫面，其中包含使用透明度的按鈕](images/tb-withstyles.png)

下列範例顯示 Windows 8 桌面上的類似對話方塊。 在 Windows 8 中，視覺效果樣式一律會開啟，因此 Windows 8 應用程式會取得「免費」的主題。

![windows 8 桌面上簡單對話方塊的螢幕擷取畫面](images/tb-win8.png)

## <a name="visual-styles-components"></a>視覺化樣式元件

下列元件支援視覺化樣式：

-   第6版或更新版本的通用控制項程式庫 (ComCtl32.dll) 
-   在 UxTheme.dll 中實作為視覺化樣式 API
-   主題服務
-   一或多個視覺化樣式定義檔案 (. msstyles) 

視覺化樣式 API 相依于稱為主題的系統服務。 通用控制項程式庫會查詢主題服務來取得樣式相關資訊，而在 Windows 7 中，則會使用服務，以目前的視覺化樣式呈現控制項。

在 Windows 8 和更新版本中，如果主題服務已關閉，視覺效果樣式 API 仍可運作。 這表示當主題服務關閉時，通用控制項和非工作區的視窗仍會有視覺化樣式。 仍需要主題服務的 Windows 8 功能包括：

-   變更視覺效果樣式， **通常是透過 [** **電腦設定**] 的 [個人化] 頁面。
-   在使用者會話之間切換使用者、登出、關機和共用所涉及的效能優化。

視覺化樣式 API 會從與目前選取之主題相關聯的 msstyles 檔案取得樣式資訊。 Msstyles 檔案包含一組定義視覺效果樣式的度量、字型、色彩和點陣圖。

## <a name="application-requirements-for-supporting-visual-styles"></a>支援視覺效果樣式的應用程式需求

若要使用視覺化樣式，您的應用程式必須在包含 ComCtl32.dll 6 版或更新版本的作業系統上執行。 如果您想要讓應用程式使用 ComCtl32.dll 第6版，則必須新增應用程式資訊清單或編譯器指示詞，以指定應該使用第6版（如果有的話）。 如需如何建立應用程式資訊清單以便讓應用程式使用視覺化樣式的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

針對通用控制項，不需要採取進一步的動作，以確保控制項顯示在使用者的慣用視覺效果樣式中。

如果您的應用程式包含自訂或主控描繪的控制項，您必須使用視覺化樣式 API 來取得目前使用中視覺效果樣式的相關資訊，並使用該樣式來繪製控制項。

在 Windows 8 之前的 Windows 版本中，應用程式通常需要提供兩個不同的程式碼路徑，以繪製自訂和主控描繪的控制項。 當使用視覺化樣式的主題為作用中時，其中一個程式碼路徑會繪製控制項，而當 Windows 傳統主題或高對比主題為作用中時，另一個程式碼路徑會繪製控制項。 不過，在 Windows 8 中，視覺效果樣式一律是開啟的，因此不需要個別的主題程式碼路徑。 針對 Windows 8 的應用程式取得高對比主題「免費」。 如需詳細資訊，請參閱 [支援高對比主題](supporting-high-contrast-themes.md)。

如需的詳細資訊，請參閱 [使用視覺化樣式搭配自訂和 Owner-Drawn 控制項](using-visual-styles.md) 和 [視覺化樣式參考](uxctl-ref.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[視覺化樣式](themes-overview.md)
</dt> </dl>

 

 




