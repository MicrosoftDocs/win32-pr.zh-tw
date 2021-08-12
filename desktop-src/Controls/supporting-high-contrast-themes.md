---
title: 支援高對比主題
description: 本主題將 Windows 8 中的高對比主題，與舊版 Windows 的支援進行比較，並說明如何在 Windows 8 應用程式中支援高對比主題。
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f32c89302daeb7190174a0d6b9e822e1c55d3e530ad29baedd00c5ffdefc97b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670618"
---
# <a name="supporting-high-contrast-themes"></a>支援高對比主題

本主題將 Windows 8 中的高對比主題，與舊版 Windows 的支援進行比較，並說明如何在 Windows 8 應用程式中支援高對比主題。

其中包含下列各節。

-   [高對比主題的支援總覽](#overview-of-support-for-high-contrast-themes)
-   [在 Windows 8 和更新版本中支援高對比主題](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [將相容性區段新增至您的應用程式資訊清單](#adding-a-compatibility-section-to-your-application-manifest)
-   [偵測舊版 Windows 中的高對比](#detecting-high-contrast-in-previous-versions-of-windows)
-   [相關主題](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a>高對比主題的支援總覽

Windows 7 及更早版本支援兩個主題模型，包括舊版 Windows 傳統模型，以及目前的視覺化樣式。 Windows 傳統模型已透過 Windows 7 保留，主要是為了支援各種高對比主題。 不過，Windows 傳統模型有一些缺點：

-   不支援使用視覺化樣式的主題，例如 Windows Aero。 高對比主題的使用者必須使用 Windows 傳統 UI。
-   不支援依賴桌面視窗管理員 (DWM) 執行的 UI 功能，例如縮圖預覽和 Windows 7 中引進的全螢幕放大鏡。
-   開發人員必須維護兩個不同的程式碼路徑，以支援兩個不同的主題模型。

在 Windows 8 和更新版本中，下列主題模型的變更會解決先前的缺點：

-   不再支援 Windows 傳統主題模型，讓開發人員只針對以 Windows 8 為目標的應用程式維護一個程式碼路徑。
-   由於視覺效果樣式和 DWM 都在 Windows 8 中，因此高對比使用者可以存取縮圖預覽和全螢幕放大鏡等功能。
-   視覺化樣式支援設定各種 UI 元素的色彩，讓高對比使用者可以自訂 UI，以配合個別的需求和喜好設定。
-   Windows 8 包含的現有應用程式的相容性支援，是根據 Windows 的傳統主題模型，設計成使用高對比主題。

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a>在 Windows 8 和更新版本中支援高對比主題

在 Windows 8 中，因為視覺效果樣式是在高對比模式中，所以只要您注意下列指導方針，支援高對比的主題就會很簡單。

-   字型和控制項大小。 為了確保您的 UI 可供殘障使用者存取，請根據目前的主題設定來設定字型大小。 將控制項的大小設定為至少預設大小。
-   [色彩]。 避免使用硬式編碼的色彩。 相反地，請使用系統色彩，因為它們是以目前的主題為基礎。 使用自訂色彩可能會干擾和覆寫高對比主題中的色彩。
-   應用程式資訊清單。 設計用來使用新高對比主題的應用程式應該在其資訊清單中定義應用程式相容性區段，其中包含 Windows 8 相容性 guid。 否則，Windows 會假設應用程式是針對舊版 Windows 所設計，並藉由模擬 Windows 的傳統主題模型來呈現應用程式 UI。

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a>將相容性區段新增至您的應用程式資訊清單

應用程式資訊清單是描述應用程式需求的 XML 檔。 資訊清單的相容性區段會識別應用程式所支援的 Windows 版本。 [相容性] 區段中會使用下列 Guid 來識別 Windows 的各種版本。

| 版本       | GUID                                   |
|---------------|----------------------------------------|
| Windows Vista | {e2011457-1546-43c5-a5fe-008deee3d3f0} |
| Windows 7     | {35138b9a-5d96-4fbd-8e2d-a2440225f93a} |
| Windows 8     | {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} |



 

相容性區段可以指定 Windows 的多個版本，但每個版本都必須包含在它自己的 `<supportedOS/>` 標記內。 下列範例顯示在相容性區段中指定 Windows 7 和 Windows 8 的應用程式資訊清單：


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



如果應用程式沒有相容性資訊清單，則會假設為 Windows Vista 應用程式，且當高對比主題為使用中時，不會在工作區中使用主題控制項。 此外，某些視覺效果樣式函式的行為會受到影響。 例如， [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive)、 [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)和 [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) 會傳回 FALSE，而 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 和 [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) 則會傳回 Null 控制碼。 這是為了提供相容性支援，因此在 Windows 8 之前建立的應用程式仍然可以像舊版 Windows 的高對比模式一樣，在視覺效果樣式無法使用的情況下，呈現其 UI。

在 Windows 8，應用程式仍會獲得桌面電腦群組合的優點。 例如，這表示可用性應用程式（例如，全螢幕放大鏡）不會依賴個別應用程式資訊清單的狀態。 可用性應用程式會繼續在高對比模式下運作，而應用程式不會在其資訊清單中識別為 Windows 8 相容性。

下列影像顯示 Windows 7 高對比的簡單對話方塊。

![hig 對比對話方塊](images/win7-high-contrast.png)

此影像會在 Windows 8 上顯示相同的對話方塊，但在應用程式資訊清單中指定了 Windows 7 相容性：

![w8 高對比對話方塊](images/win7-compat.png)

此影像會顯示在 Windows 8 上具有高對比的相同對話方塊，並在應用程式資訊清單中指定 Windows 8：

![使用資訊清單 w8 高對比對話方塊](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a>偵測舊版 Windows 中的高對比

在舊版 Windows 上執行的應用程式無法存取新的高對比主題。 如果您的應用程式需要在舊版中執行，您應該在 Windows 的傳統主題模型中包含以高 contraWindowsst 方式呈現 UI 的支援。 您的應用程式可以藉由使用 **SPI \_ GETHIGHCONTRAST** 旗標呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)函式，來判斷高對比主題是否為使用中狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用視覺化樣式](cookbook-overview.md)
</dt> <dt>

[視覺化樣式](themes-overview.md)
</dt> </dl>

 

 