---
description: 網頁會使用網頁上定義的元資料標記，利用標題、圖示和標題色彩，自訂使用者介面 (UI) 。
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: 如何自訂 UI 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19314f8e4c5d4944a500a0eef3aa0f75cd231b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851147"
---
# <a name="how-to-customize-the-ui-elements"></a>如何自訂 UI 元素

網頁會使用網頁上定義的元資料標記，利用標題、圖示和標題色彩，自訂使用者介面 (UI) 。 Web 開發人員可以使用 HTML <meta> 標記，在 Web 驗證訊息代理程式 UI 中顯示提供者的特質和品牌。 此外，開發人員也可以指示更複雜的使用者動作，例如註冊和復原密碼。 概念與 Windows Internet Explorer 9 和 Windows 7 的釘選網站功能非常類似。

除了在網頁區域周圍自訂使用者介面之外，網頁也應該利用 Windows 8 控制項的樣式、啟用觸控功能，並在適當的情況下啟用在瀏覽器中開啟的連結。

以下是已利用 Web 驗證 Broker 自訂模型的網頁範例。 ![web 驗證 broker 使用者介面元素](images/wab-figure7.png)

## <a name="instructions"></a>指示

### <a name="step-1-customize-the-icon"></a>步驟1：自訂圖示

網頁可以使用 mswebdialog 標誌元標記提供圖示。

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

內容是可以是相對或絕對頁面的 URL。 URL 的配置可以是 HTTP 或 HTTPS。 檔案的格式應該是 PNG 或 JPG。 影像的大小應該是30x30 圖元。 如果影像的大小不同，則會由作業系統相應減少或相應縮小，以符合30x30 空間。 當擴充至140% 和180%，以考慮較高的解析度畫面時，應該將影像設計成可妥善轉譯。 若要測試不同的縮放比例，請使用 Visual Studio 11 中載入的 [Web 驗證 BROKER SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) ，這可讓您使用設計模式的裝置視窗來模擬不同的解析度和縮放因數。

### <a name="step-2-customize-the-title-text"></a>步驟2：自訂標題文字

網頁可以使用 mswebdialog 標題中繼標記來提供標題。

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

標題應該是簡短的，且應該反映提供者的品牌 (例如 Contoso) 。

### <a name="step-3-customize-the-header-color"></a>步驟3：自訂頁首色彩

網頁可以使用 mswebdialog 標頭-色彩中繼標記，提供代表其品牌身分識別的色彩，以用於對話方塊的標頭。

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

此色彩可以是此處指定的任何值。 但是，Web 驗證代理人會忽略任何 Alpha 通道值。 使用此色彩，以及一般頁面上使用的色彩時，建議您遵循提供者 Windows 8 應用程式中所使用的相同色彩（如果有這類應用程式的話）。

> [!Note]  
> 剖析中繼標記之後，用戶端上的每個伺服器都會快取圖示和色彩。 在啟動 UI 之前清除用戶端快取，以便讓變更生效。 若要這樣做，請修改下列登錄設定。

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

下載圖示之後，就不會再收取24小時的時間。 若要使用標誌影像進行測試，請將上述的登錄機碼設定為較低的值。

### <a name="step-4-customize-the-web-page"></a>步驟4：自訂網頁

除了在網頁周圍自訂 UI 之外，開發人員也應該建立與整體 Windows 8 體驗緊密整合的網頁。 這包括使用建議的樣式，確保網頁適用于已啟用觸控功能的裝置，並在網頁瀏覽器中開啟特定網頁。

-   樣式

    強烈建議您使用此處建議的樣式，在 Web 驗證訊息代理程式網頁和 Windows 8 的其他 UI 元件之間建立更一致的使用者體驗。 網頁應該使用白色背景，而且沒有框線。 [登入] 或 [取消] 等按鈕應放置在右下角，並使用與標頭相同的色彩。 最後，由於 Web 驗證訊息代理程式提供了 [上一頁] 按鈕，因此請考慮完全刪除網頁中的 [取消] 按鈕。

-   啟用觸控

    網頁應以觸控式使用者的互動方式設計。 如需在 Windows 8 中設計觸控的詳細資訊，請參閱 [觸控互動設計](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) 主題。

-   自訂超連結的目標

    Web 驗證訊息代理程式很適合用來傳遞需要單一使用者動作的網頁，例如登入或 OAuth 授權頁面。 但是，如果是更複雜的使用者流程，例如帳戶建立、從遺失或忘記密碼中復原、顯示隱私權聲明等，而使用者預期需要花一些時間來瞭解和完成流程，建議您在使用者慣用的瀏覽器中啟動這些頁面，以支援完整流覽和流覽。 Web 驗證代理人預設不允許從網頁開啟新的瀏覽器視窗 (如需詳細資料，請參閱預設為沒有新視窗) 。 不過，藉由使用中繼標記， `mswebdialog-newwindowurl` 網頁可以宣告應該在瀏覽器中開啟的 url。

    `mswebdialog-newwindowurl`允許網頁指定 url 或部分 url，讓 Web 驗證訊息代理程式在每次要求您使用目標屬性或視窗開啟新視窗中的 url 時，用來比對 (左字串比對) 。請開啟 () 方法。 如果有相符的值，則會在使用者的預設瀏覽器中開啟 URL。 如果沒有相符的，Web 驗證代理人會)  (預設行為，流覽至 URL 本身。 例如：`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    在此中繼標記的情況下，Web 驗證代理人會 https://www.contoso.com/privacy/policy.html 在瀏覽器中開啟，但會直接流覽至 https://www.contoso.com/termsofuse.html 。 請注意，不會嘗試在新視窗中開啟的連結 (例如，未使用目標屬性或視窗的連結。開啟 () 方法) 不受此中繼標記影響。 內容是可以是相對或絕對頁面的 URL。 URL 的配置可以是 HTTP 或 HTTPS。 您應定義 `mswebdialog-newwindowurl` 中繼標籤來涵蓋任何不屬於核心使用者流程的連結，例如隱私權聲明、註冊表單等等。 如果您支援使用協力廠商驗證提供者登入 (例如 OpenID 提供者) ，請務必將這些互動保留在 Web 驗證訊息代理程式中。 若要讓頁面上的所有連結都能安全地在瀏覽器中開啟，請使用星狀語法，例如，請 `  <meta name="mswebdialog-newwindowurl" content="*"/>` 注意，" \* " 只能單獨使用，且無法與另一個 URL 合併，例如 " https://www.contoso.com/\ *" 不是有效的語法。

### <a name="step-5-rules-applied-to-all-meta-tags"></a>步驟5：套用至所有元標記的規則

當 Web 驗證代理人處理中繼標記時，適用下列規則：

-   中繼標籤的效果會跨相同第二層級網域下的所有頁面保存 (例如 contoso.com) ，除非遇到相同名稱但出現不同內容的其他中繼標記。
-   如果在相同的頁面上遇到相同名稱的多個中繼標記，Web 驗證代理人只會選擇其中一個，並忽略其餘部分。 所選擇的特定中繼標記未定義。
    > [!Note]  
    > 此規則不會套用至 `mswebdialog-newwindowurl` 允許相同頁面上多個實例的中繼標籤。

     

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
