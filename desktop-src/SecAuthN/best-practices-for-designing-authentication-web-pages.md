---
description: 本主題說明設計使用 Web 驗證訊息代理程式進行登入之網頁的最佳作法。
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: 設計驗證網頁的最佳做法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353671"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>設計驗證網頁的最佳做法

本主題說明設計使用 Web 驗證訊息代理程式進行登入之網頁的最佳作法。

-   [使用 metatags](#use-of-metatags)
-   [使用 Windows 8 CSS 樣式](#use-of-windows-8-css-styling)
-   [使用色彩和主題](#use-of-color-and-themes)
-   [對齊](#alignment)
-   [設計嵌入式管理](#designing-for-snap)
-   [設計快速且流暢的登入體驗](#designing-for-a-fast-and-fluid-login-experience)
-   [安全性考量](#security-considerations)
-   [相關主題](#related-topics)

## <a name="use-of-metatags"></a>使用 metatags

使用 metatags 時，提供者 "Contoso Social" 可指定標題、圖示和標頭的色彩。 在 (WebAuthLogin.html) 的範例 HTML 檔案中，您可以使用下列程式碼來完成這項工作。


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



這可讓 Windows 在 UI 的標頭中，以顯著的方式整合提供者的存在，如下列螢幕擷取畫面中的紅色方塊反白顯示。 ![在 ui 中顯示 contoso 標頭的登入頁面](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>使用 Windows 8 CSS 樣式

提供的 ui-light 樣式表單是 Windows Store 應用程式所使用的 Windows 8 樣式表單。 它會定義印刷樣式和標準控制項（例如按鈕、文字方塊、超連結和核取方塊）的 Windows 存放區應用程式樣式，以確保它們的觸控性很好用。 當您設計和量身打造 Windows 8 的 web 授權頁面時，建議您使用此樣式表單，並視需要進行更新，只要您的網頁仍以自己的方式遵循最佳作法。

比方說，如果您有一個特殊的樣式表單，讓超連結看起來像是在您的網頁上，最好是仔細確定您所提供的樣式跟標準 Windows 8 超連結一樣容易使用。 這對於在其觸控裝置上使用 Windows 8 的取用者基底而言是不可或缺的。

## <a name="use-of-color-and-themes"></a>使用色彩和主題

此範例將示範如何使用幾種不同的方式來仔細使用色彩。

-   網頁的白色背景。 您可以從上一個螢幕擷取畫面中看出，網頁是裝載在橫跨畫面寬度的白色介面內。 若要確定網頁與介面整合，建議網頁必須有白色背景的外觀。
-   根據您的品牌色彩標示控制項。 CSS 檔案 theme-colors 提供樣式來覆寫 ui 淺色樣式表單中的標準控制項色彩，以比對控制項的主題與標頭的色彩。 例如，在下列螢幕擷取畫面中，按鈕和超連結會採用衍生自頁首色彩的色彩。 ![具有與標頭相同色彩的按鈕和文字螢幕擷取畫面](images/wab-figure11.png)
-   標題色彩。 在標頭中使用 Contoso 的品牌色彩，可針對提供者在系統 UI 內的品牌建立一致的特質。

## <a name="alignment"></a>對齊

網頁本身的左邊或右邊沒有填補，以允許在左邊標題的標題和右邊的標頭中使用標題的印刷樣式對齊。

您也會注意到，按鈕一律會靠右對齊網頁 (，並靠右對齊標題) 中的圖示。 這是最佳做法，因為 Windows 8 使用者習慣于右下方具有按鈕的類似對話流程。

## <a name="designing-for-snap"></a>設計嵌入式管理

在下圖中，您可以看到 [登入] 和 [許可權] 頁面處於 [貼齊狀態]。

![登入畫面的貼齊視圖 ](images/wab-figure12.png) . ![[許可權] 頁面的貼齊視圖 ](images/wab-figure13.png)

在範例檔案 ui-webauth 中，您可以看到使用媒體查詢，根據網頁的可用寬度，將頁面的版面配置優化。 以下列範圍括住的程式碼片段，可為貼齊狀態量身打造 CSS。


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



在 Windows 8 中，對齊狀態的寬度為320圖元。 Web 驗證頁面在上述 UI 中會佔用260圖元。 我們使用的最大寬度值具有足夠的邊界，因此提供者的媒體查詢程式碼不會系結至格線的確切寬度。

在量身打造您的應用程式時，請務必讓使用者不會遺失其在 web 驗證體驗的其他觀點中的任何內容 (完整、填滿或快速鍵的觀點) ，但要重新結構頁面中的元素版面配置和階層，以保持內容的內容是可見且互動式的，是很重要的。 我們已將範例說明如何調適此範例的網頁，以取得貼齊狀態。

-   例如，在 [貼齊狀態] 的 [登入] 頁面中，[輸入文字] 欄位的 [寬度] 屬性 (如) ui-light 中所指定）已被覆寫並設定為較小的數值，因此文字欄位不會水準裁剪。
-   另一個範例是，在 [貼齊] 狀態中，h1 和 h2 標頭的字型大小會從 42 pt 和 20 pt 分別縮減為 20 pt 和 11 pt。 這是根據 Windows 8 型別遞增來完成，並將文字優化，以在變更的區中更精簡。
-   另舉一個範例，請注意，[許可權] 頁面中的圖示大小較小 (相較于上述) 的完整視圖頁面。 同樣地，這是為了保留內容，同時針對已變更的功能區交換設計資產。

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>設計快速且流暢的登入體驗

在此網頁的設計初期，我們會在這一頁最適合的一件事，是一種快速且流暢的登入體驗。 因此，流程中最重要的 UI 是 [登入] 頁面中的 [使用者名稱] 和 [密碼] 欄位，以取得快速認證專案體驗。 雖然我們發現有其他常見的案例（例如密碼抓取）和參考隱私權聲明，但網路的豐富體驗是更適合這些經驗的地方。 針對與安全 web 驗證體驗無關的所有流程，建議您將使用者流覽至瀏覽器。 這會顯示在範例 HTML 檔案 (WebAuthLogin.html) 如下所示： `<meta name="mswebdialog-newwindowurl" content="*" />` 這會從使用者的預設瀏覽器中的 [登入] 或 [許可權] 頁面開啟所有連結的網頁，讓使用者可以在其中完成這些流程，然後返回應用程式進行登入。

## <a name="security-considerations"></a>安全性考量

下列文章提供撰寫安全 c + + 程式碼的指引。

-   [C + + 的安全性最佳作法](/cpp/security/security-best-practices-for-cpp)
-   [適用于應用程式的模式 & 實務安全性指引](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web 驗證訊息代理程式的常見問題](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
