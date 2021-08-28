---
title: 高對比模式
description: 高對比模式
ms.assetid: 817F2BBD-3744-4D34-927F-EBF9F7894CC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a288447dda8d3a76278ad695459d2c15598b328
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883894"
---
# <a name="high-contrast-mode"></a>高對比模式

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器**-Windows Server 2012  



## <a name="description"></a>說明

在先前的 Windows 作業系統中，高對比模式僅限於在傳統主題下執行的主題，這些主題未以視覺化方式呈現樣式。 在 Windows 8 和 Windows Server 2012 中，傳統模式已移除，並以視覺化樣式的高對比主題來取代。 這項變更的主要優點之一，是移除以傳統模式執行之應用程式的不同程式碼路徑。

開發人員仍然需要在高對比模式影響其應用程式的方式，以及如何開發真正與樣式無關的應用程式方面獲得教育。 這點很重要，因為當主題色彩不正確的使用或假設可能會導致應用程式在視覺效果樣式（例如 Aero）下正確運作，而這些相同的應用程式在高對比下回應錯誤。 比方說，在 Aero 中，文字一律是黑色，而反白顯示色彩則是淺藍色。 但在高對比的黑色中，反白顯示色彩為黑色。 如果您假設有黑色文字，在 Windows 8 之前的許多內建應用程式中，並使用系統預設值進行醒目提示，則使用者會在黑色背景看到黑色文字。 在這些情況下，您必須瞭解如何正確使用主題和系統計量，讓應用程式在樣式之間看起來正確。

## <a name="manifestations"></a>表現

-   未在 &lt; &gt; 其應用程式資訊清單中包含 Windows 8 supportedOS 標記的應用程式工作區中，未啟用主題。 因此，應用程式必須使用在傳統主題的高對比模式下轉譯所需的程式碼路徑，來轉譯工作區。
-   在高對比主題中，應用程式的非用戶端和用戶端區域都不會啟用主題。 它也不會在其應用程式資訊清單中未包含 Windows 8 supportedOS 標記的應用程式中啟用， &lt; &gt; 而且會使用 DwnIsCompositionEnabled () API 在視窗的非工作區中繪製。 整個應用程式會以傳統主題的高對比模式呈現。
-   在其資訊清單中新增 Windows 8 支援的應用程式，但不使用視覺化樣式進行轉譯，也就是說，它們會在其應用程式中硬式編碼色彩或影像，可能無法在高對比主題中正確呈現。 文字可能難以閱讀，或影像可能不會出現在高對比模式中。

## <a name="mitigation"></a>降低

高對比主題中的文字色彩已撰寫成符合 Microsoft 協助工具指導方針的規範。 在前景和背景之間保持14:1 的高對比比例。 如果預設啟用的色彩不適合特定的使用者，可以在這些高對比主題中，透過 [視窗色彩] 的 [控制台] 設定輕鬆地加以自訂。

這些 UI 元件可以自訂在高對比主題中：

-   視窗背景色彩
-   文字色彩
-   超連結色彩
-   停用的文字
-   選取的文字前景和背景色彩
-   使用中視窗標題前景和背景色彩
-   非作用中視窗標題前景和背景色彩
-   按鈕前景和背景色彩

## <a name="solution"></a>解決方案

如果在高對比主題的應用程式中看到非預期的行為，這些解決方案中的其中一個可能會有説明：

-   **股潮流應用程式以 Windows 8：**

    在應用程式資訊清單中不包含 Windows 8 supportedOS 標籤的應用程式， &lt; &gt; 其用戶端區域會呈現，而不需要主題。 內建應用程式應該會在應用程式資訊清單中包含這個專案。 新增 Windows 8 的 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38 GUID 值。

-   **使用視覺化樣式搭配主控描繪的 Ui：**

    擁有者繪製的控制項應遵循 [MSDN](/windows/desktop/Controls/using-visual-styles) 上的指示，以正確轉譯控制群組件和狀態，包括文字。 開發人員不應該依賴裝置內容中所指定的文字或背景色彩，就能使用非 UxTheme 的方法來呈現。 如果有問題的控制項沒有主題元件，請使用 GetThemeSysColor 搭配 [適當的度量](/windows/desktop/api/winuser/nf-winuser-getsyscolor) ，並使用標準 GDI 方法來繪製文字。 如果沒有適當的 UxTheme 呼叫，請使用 GetSysColor 方法來取得適當的度量。

-   **選取文字色彩：**

    請勿使用硬式編碼的文字色彩，即使它在所有常見的案例中都是正確的。 建立出貨主題的方式，會以支援相關計量的高可見度來建立。 例如，色彩 \_ HIGHLIGHTTEXT 的目的是要搭配色彩醒目提示一起使用， \_ 而色彩 \_ WINDOWTEXT 則是要搭配色彩視窗當做背景使用 \_ 。 如果這些關聯有例外狀況，請在主題元件和狀態定義中使用它們，而不是在程式碼中。 設計高對比 Ui 時，UI 必須與目前套用的高對比主題無關，因為高對比使用者可以自訂其色彩。

-   **回應 WM \_ ThemeChange 事件：**

    如果您的應用程式會快取從主題中取出的色彩，或是以非標準方式套用色彩，請新增 \_ 會重新計算預存色彩值並重新繪製 UI 的 WM THEMECHANGE 訊息處理常式。

-   **撰寫高對比的 WWA 應用程式：**

    Web apps 無法存取 UxTheme Api，但仍應以目前的系統計量作為 UI 的基礎來撰寫。 有幾個資源可供 WWA 開發人員運用，以確保符合高對比規範的應用程式：

    -   [W3C CSS 色彩規格](https://www.w3.org/TR/css3-color/)會指定使用系統計量的語法，而不是特定的色彩
    -   將高對比媒體查詢的支援新增至 Internet Explorer 10
    -   WWAs 可以利用 IAccessibilityCapabilities：： get \_ systeminformation.highcontrast () 方法來檢查高對比的狀態

    WindowsStore 應用程式與傳統 Windows 應用程式中的主題元件沒有許多相同的問題，但您仍然需要確保高對比的合規性。 根據預設，Internet Explorer 會忽略某些使用者定義樣式，並將其取代為高對比相容的值。 例如，背景影像、背景和色彩 CSS 屬性都會被忽略。

    如果您不想要 Internet Explorer 忽略任何您設定的屬性，並確定 UI 符合高對比規範，您可以在父元素上設定新的 M3 CSS 屬性– ms-高對比： off。

-   **撰寫高對比的 Windows 存放區應用程式：**

    WindowsStore 應用程式應該使用[SystemColors](/dotnet/api/system.windows.systemcolors)類別來判斷適當的 UI 元素著色，請記住，某些系統計量色彩是設計來搭配使用，例如 SystemColors. WindowColor 和 SystemColors. WindowTextColor。 這有助於提供絕佳的高對比體驗。

-   **在舊版 Windows 中正確偵測高對比：**

    在舊版 Windows 上執行的應用程式無法存取新的高對比主題，即使資訊清單指定與 Windows 問題的版本相容。 因此，可能需要插入額外的程式碼路徑，以處理舊版 Windows 所使用的傳統環境中的呈現。 在此情況下，應該透過使用 SPI GETHIGHCONTRAST 旗標呼叫 [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式來檢查高對比的存在 \_ 。 這是檢查高對比是否存在的唯一支援方法。

## <a name="tests"></a>測試

測試應用程式時，請確定它會在 Windows 8： Aero、Basic、高對比1、高對比2、高對比黑色和高對比白色提供的所有內建主題中正確呈現。 確定文字在高對比主題中清楚可見且容易閱讀。

## <a name="resources"></a>資源

-   [Aero 樣式類別、元件和狀態](../controls/aero-style-classes-parts-and-states.md) (新的基本主題和高對比主題也會使用這些狀態) 
-   [所有視覺效果樣式通用的元件和狀態](../controls/parts-and-states.md)
-   [使用視覺效果樣式搭配自訂和 Owner-Drawn 控制項](../controls/using-visual-styles.md)
-   [GetSysColor 函式](/windows/win32/api/winuser/nf-winuser-getsyscolor)
-   [W3C CSS 色彩模組層級3](https://www.w3.org/TR/css3-color/)
-   [SystemColors 類別](/dotnet/api/system.windows.systemcolors?view=netcore-3.1)
-   [SystemParametersInfo 函式](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
-   [Microsoft Accessibility](https://www.microsoft.com/enable/) (Microsoft 協助工具)

 

 
