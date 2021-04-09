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
# <a name="how-to-customize-the-ui-elements"></a><span data-ttu-id="90b7d-103">如何自訂 UI 元素</span><span class="sxs-lookup"><span data-stu-id="90b7d-103">How to customize the UI elements</span></span>

<span data-ttu-id="90b7d-104">網頁會使用網頁上定義的元資料標記，利用標題、圖示和標題色彩，自訂使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="90b7d-104">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span> <span data-ttu-id="90b7d-105">Web 開發人員可以使用 HTML <meta> 標記，在 Web 驗證訊息代理程式 UI 中顯示提供者的特質和品牌。</span><span class="sxs-lookup"><span data-stu-id="90b7d-105">Web developers can use HTML <meta> tags to display the provider's personality and brand in the Web Authentication Broker UI.</span></span> <span data-ttu-id="90b7d-106">此外，開發人員也可以指示更複雜的使用者動作，例如註冊和復原密碼。</span><span class="sxs-lookup"><span data-stu-id="90b7d-106">In addition, developers can direct more intricate user actions, for example signing up and recovering passwords.</span></span> <span data-ttu-id="90b7d-107">概念與 Windows Internet Explorer 9 和 Windows 7 的釘選網站功能非常類似。</span><span class="sxs-lookup"><span data-stu-id="90b7d-107">The concept is very similar to Pinned Sites feature of the Windows Internet Explorer 9 and Windows 7.</span></span>

<span data-ttu-id="90b7d-108">除了在網頁區域周圍自訂使用者介面之外，網頁也應該利用 Windows 8 控制項的樣式、啟用觸控功能，並在適當的情況下啟用在瀏覽器中開啟的連結。</span><span class="sxs-lookup"><span data-stu-id="90b7d-108">In addition to customizing the user interface around the web page area, the web page should also take advantage of the Windows 8 controls’ styles, be enabled for touch, and enable links to be opened in the browser where appropriate.</span></span>

<span data-ttu-id="90b7d-109">以下是已利用 Web 驗證 Broker 自訂模型的網頁範例。</span><span class="sxs-lookup"><span data-stu-id="90b7d-109">The following is an example of a web page that has taken advantage of the Web Authentication Broker customization model.</span></span> ![web 驗證 broker 使用者介面元素](images/wab-figure7.png)

## <a name="instructions"></a><span data-ttu-id="90b7d-111">指示</span><span class="sxs-lookup"><span data-stu-id="90b7d-111">Instructions</span></span>

### <a name="step-1-customize-the-icon"></a><span data-ttu-id="90b7d-112">步驟1：自訂圖示</span><span class="sxs-lookup"><span data-stu-id="90b7d-112">Step 1: Customize the icon</span></span>

<span data-ttu-id="90b7d-113">網頁可以使用 mswebdialog 標誌元標記提供圖示。</span><span class="sxs-lookup"><span data-stu-id="90b7d-113">The web page can provide an icon by using an mswebdialog-logo meta tag.</span></span>

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

<span data-ttu-id="90b7d-114">內容是可以是相對或絕對頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="90b7d-114">The content is a URL that can be a page relative or absolute.</span></span> <span data-ttu-id="90b7d-115">URL 的配置可以是 HTTP 或 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="90b7d-115">The scheme of the URL can be HTTP or HTTPS.</span></span> <span data-ttu-id="90b7d-116">檔案的格式應該是 PNG 或 JPG。</span><span class="sxs-lookup"><span data-stu-id="90b7d-116">The format of the file should be either PNG or JPG.</span></span> <span data-ttu-id="90b7d-117">影像的大小應該是30x30 圖元。</span><span class="sxs-lookup"><span data-stu-id="90b7d-117">The size of the image should be 30x30 pixels.</span></span> <span data-ttu-id="90b7d-118">如果影像的大小不同，則會由作業系統相應減少或相應縮小，以符合30x30 空間。</span><span class="sxs-lookup"><span data-stu-id="90b7d-118">If the image is of the different size, it will be scaled down or up by the operating system to fit the 30x30 space.</span></span> <span data-ttu-id="90b7d-119">當擴充至140% 和180%，以考慮較高的解析度畫面時，應該將影像設計成可妥善轉譯。</span><span class="sxs-lookup"><span data-stu-id="90b7d-119">The image should be designed to render well when scaled up to 140% and 180% to account for higher resolution screens.</span></span> <span data-ttu-id="90b7d-120">若要測試不同的縮放比例，請使用 Visual Studio 11 中載入的 [Web 驗證 BROKER SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) ，這可讓您使用設計模式的裝置視窗來模擬不同的解析度和縮放因數。</span><span class="sxs-lookup"><span data-stu-id="90b7d-120">To test different scaling factors, use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Visual Studio 11 which allows simulating different resolutions and scaling factors using the Device windows of the Design mode.</span></span>

### <a name="step-2-customize-the-title-text"></a><span data-ttu-id="90b7d-121">步驟2：自訂標題文字</span><span class="sxs-lookup"><span data-stu-id="90b7d-121">Step 2: Customize the title text</span></span>

<span data-ttu-id="90b7d-122">網頁可以使用 mswebdialog 標題中繼標記來提供標題。</span><span class="sxs-lookup"><span data-stu-id="90b7d-122">The web page can provide the title by using the mswebdialog-title meta tag.</span></span>

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

<span data-ttu-id="90b7d-123">標題應該是簡短的，且應該反映提供者的品牌 (例如 Contoso) 。</span><span class="sxs-lookup"><span data-stu-id="90b7d-123">The title should be short and should reflect the brand of the provider (for example, Contoso).</span></span>

### <a name="step-3-customize-the-header-color"></a><span data-ttu-id="90b7d-124">步驟3：自訂頁首色彩</span><span class="sxs-lookup"><span data-stu-id="90b7d-124">Step 3: Customize the header color</span></span>

<span data-ttu-id="90b7d-125">網頁可以使用 mswebdialog 標頭-色彩中繼標記，提供代表其品牌身分識別的色彩，以用於對話方塊的標頭。</span><span class="sxs-lookup"><span data-stu-id="90b7d-125">The web page can provide the color that represents its brand identity to be used for the header of the dialog by using the mswebdialog-header-color meta tag.</span></span>

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

<span data-ttu-id="90b7d-126">此色彩可以是此處指定的任何值。</span><span class="sxs-lookup"><span data-stu-id="90b7d-126">The color can be any value specified here.</span></span> <span data-ttu-id="90b7d-127">但是，Web 驗證代理人會忽略任何 Alpha 通道值。</span><span class="sxs-lookup"><span data-stu-id="90b7d-127">However, the Web Authentication Broker will ignore any alpha channel value.</span></span> <span data-ttu-id="90b7d-128">使用此色彩，以及一般頁面上使用的色彩時，建議您遵循提供者 Windows 8 應用程式中所使用的相同色彩（如果有這類應用程式的話）。</span><span class="sxs-lookup"><span data-stu-id="90b7d-128">With this color specifically and with colors used on the page in general, it is recommended to follow the same colors used in provider’s Windows 8 app if such app exists.</span></span>

> [!Note]  
> <span data-ttu-id="90b7d-129">剖析中繼標記之後，用戶端上的每個伺服器都會快取圖示和色彩。</span><span class="sxs-lookup"><span data-stu-id="90b7d-129">Icons and colors are cached per server on the client once META tags are parsed.</span></span> <span data-ttu-id="90b7d-130">在啟動 UI 之前清除用戶端快取，以便讓變更生效。</span><span class="sxs-lookup"><span data-stu-id="90b7d-130">Clear the client cache before launching the UI in order for the changes to take effect.</span></span> <span data-ttu-id="90b7d-131">若要這樣做，請修改下列登錄設定。</span><span class="sxs-lookup"><span data-stu-id="90b7d-131">To do so, modify the following registry settings.</span></span>

 

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

<span data-ttu-id="90b7d-132">下載圖示之後，就不會再收取24小時的時間。</span><span class="sxs-lookup"><span data-stu-id="90b7d-132">Once an icon is downloaded it is not picked up again for 24 hours.</span></span> <span data-ttu-id="90b7d-133">若要使用標誌影像進行測試，請將上述的登錄機碼設定為較低的值。</span><span class="sxs-lookup"><span data-stu-id="90b7d-133">In order to test with logo images, set the reg key above with a lower value.</span></span>

### <a name="step-4-customize-the-web-page"></a><span data-ttu-id="90b7d-134">步驟4：自訂網頁</span><span class="sxs-lookup"><span data-stu-id="90b7d-134">Step 4: Customize the web page</span></span>

<span data-ttu-id="90b7d-135">除了在網頁周圍自訂 UI 之外，開發人員也應該建立與整體 Windows 8 體驗緊密整合的網頁。</span><span class="sxs-lookup"><span data-stu-id="90b7d-135">In addition to customizing the UI around the web page, developers should also create web pages that are seamless and integrated with the overall Windows 8 experience.</span></span> <span data-ttu-id="90b7d-136">這包括使用建議的樣式，確保網頁適用于已啟用觸控功能的裝置，並在網頁瀏覽器中開啟特定網頁。</span><span class="sxs-lookup"><span data-stu-id="90b7d-136">This includes using recommended styles, making sure web pages work great with touch enabled devices, and open certain web pages in the web browser.</span></span>

-   <span data-ttu-id="90b7d-137">樣式</span><span class="sxs-lookup"><span data-stu-id="90b7d-137">Styling</span></span>

    <span data-ttu-id="90b7d-138">強烈建議您使用此處建議的樣式，在 Web 驗證訊息代理程式網頁和 Windows 8 的其他 UI 元件之間建立更一致的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="90b7d-138">It is strongly encouraged to use the styling recommended here to create a more consistent user experience across Web Authentication Broker web pages and other UI components of Windows 8.</span></span> <span data-ttu-id="90b7d-139">網頁應該使用白色背景，而且沒有框線。</span><span class="sxs-lookup"><span data-stu-id="90b7d-139">The web page should use a white background and no borders.</span></span> <span data-ttu-id="90b7d-140">[登入] 或 [取消] 等按鈕應放置在右下角，並使用與標頭相同的色彩。</span><span class="sxs-lookup"><span data-stu-id="90b7d-140">The buttons such as Login or Cancel should be positioned at the right bottom corner and use the same color as the header.</span></span> <span data-ttu-id="90b7d-141">最後，由於 Web 驗證訊息代理程式提供了 [上一頁] 按鈕，因此請考慮完全刪除網頁中的 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="90b7d-141">Finally, since Web Authentication Broker provides a Back button, consider eliminating a Cancel button from the web page completely.</span></span>

-   <span data-ttu-id="90b7d-142">啟用觸控</span><span class="sxs-lookup"><span data-stu-id="90b7d-142">Enabling touch</span></span>

    <span data-ttu-id="90b7d-143">網頁應以觸控式使用者的互動方式設計。</span><span class="sxs-lookup"><span data-stu-id="90b7d-143">The web page should be designed with a touch-based user interaction in mind.</span></span> <span data-ttu-id="90b7d-144">如需在 Windows 8 中設計觸控的詳細資訊，請參閱 [觸控互動設計](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) 主題。</span><span class="sxs-lookup"><span data-stu-id="90b7d-144">For more information about designing for touch in Windows 8, see the [Touch interaction design](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) topic.</span></span>

-   <span data-ttu-id="90b7d-145">自訂超連結的目標</span><span class="sxs-lookup"><span data-stu-id="90b7d-145">Customizing target of the hyperlinks</span></span>

    <span data-ttu-id="90b7d-146">Web 驗證訊息代理程式很適合用來傳遞需要單一使用者動作的網頁，例如登入或 OAuth 授權頁面。</span><span class="sxs-lookup"><span data-stu-id="90b7d-146">Web Authentication Broker is great for delivering web pages that require a single user action such as logon or OAuth authorization pages.</span></span> <span data-ttu-id="90b7d-147">但是，如果是更複雜的使用者流程，例如帳戶建立、從遺失或忘記密碼中復原、顯示隱私權聲明等，而使用者預期需要花一些時間來瞭解和完成流程，建議您在使用者慣用的瀏覽器中啟動這些頁面，以支援完整流覽和流覽。</span><span class="sxs-lookup"><span data-stu-id="90b7d-147">However, for more intricate user flows such as account creation, recovering from a lost or forgotten password, showing privacy statements and so on, where the user is expected to invest some time in understanding and completing the flow, it is recommended that these pages be launched in the user’s preferred browser to support full-navigation and reach browsing.</span></span> <span data-ttu-id="90b7d-148">Web 驗證代理人預設不允許從網頁開啟新的瀏覽器視窗 (如需詳細資料，請參閱預設為沒有新視窗) 。</span><span class="sxs-lookup"><span data-stu-id="90b7d-148">Web Authentication Broker by default doesn’t allow new browser windows to be opened from a web page (see section No New windows By Default for more details).</span></span> <span data-ttu-id="90b7d-149">不過，藉由使用中繼標記， `mswebdialog-newwindowurl` 網頁可以宣告應該在瀏覽器中開啟的 url。</span><span class="sxs-lookup"><span data-stu-id="90b7d-149">However, by using the meta tag `mswebdialog-newwindowurl` the web page can declare which URLs should be opened in the browser.</span></span>

    <span data-ttu-id="90b7d-150">`mswebdialog-newwindowurl`允許網頁指定 url 或部分 url，讓 Web 驗證訊息代理程式在每次要求您使用目標屬性或視窗開啟新視窗中的 url 時，用來比對 (左字串比對) 。請開啟 () 方法。</span><span class="sxs-lookup"><span data-stu-id="90b7d-150">The `mswebdialog-newwindowurl` allows the web page to specify a URL or part of the URL that the Web Authentication Broker will use to match (left-hand string match) against every time it is asked to open a URL in a new window either by using the target attribute or window.open() method.</span></span> <span data-ttu-id="90b7d-151">如果有相符的值，則會在使用者的預設瀏覽器中開啟 URL。</span><span class="sxs-lookup"><span data-stu-id="90b7d-151">If there is a match, the URL will be opened in the user’s default browser.</span></span> <span data-ttu-id="90b7d-152">如果沒有相符的，Web 驗證代理人會)  (預設行為，流覽至 URL 本身。</span><span class="sxs-lookup"><span data-stu-id="90b7d-152">If there is no match, the Web Authentication Broker will navigate to the URL itself (default behavior).</span></span> <span data-ttu-id="90b7d-153">例如：`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`</span><span class="sxs-lookup"><span data-stu-id="90b7d-153">For example:`<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`</span></span>

    <span data-ttu-id="90b7d-154">在此中繼標記的情況下，Web 驗證代理人會 https://www.contoso.com/privacy/policy.html 在瀏覽器中開啟，但會直接流覽至 https://www.contoso.com/termsofuse.html 。</span><span class="sxs-lookup"><span data-stu-id="90b7d-154">In the case of this meta tag, the Web Authentication Broker will open the https://www.contoso.com/privacy/policy.html in the browser, but will directly navigate to https://www.contoso.com/termsofuse.html.</span></span> <span data-ttu-id="90b7d-155">請注意，不會嘗試在新視窗中開啟的連結 (例如，未使用目標屬性或視窗的連結。開啟 () 方法) 不受此中繼標記影響。</span><span class="sxs-lookup"><span data-stu-id="90b7d-155">Note that links that don’t attempt to open in a new window (for example, links that are not using target attribute or window.open() method) are not affected by this meta tag.</span></span> <span data-ttu-id="90b7d-156">內容是可以是相對或絕對頁面的 URL。</span><span class="sxs-lookup"><span data-stu-id="90b7d-156">The content is a URL that can be a page relative or absolute.</span></span> <span data-ttu-id="90b7d-157">URL 的配置可以是 HTTP 或 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="90b7d-157">The scheme of the URL can be HTTP or HTTPS.</span></span> <span data-ttu-id="90b7d-158">您應定義 `mswebdialog-newwindowurl` 中繼標籤來涵蓋任何不屬於核心使用者流程的連結，例如隱私權聲明、註冊表單等等。</span><span class="sxs-lookup"><span data-stu-id="90b7d-158">You should define `mswebdialog-newwindowurl` meta tags to cover any links that are not part of the core user flow such as privacy statements, sign up forms, and such.</span></span> <span data-ttu-id="90b7d-159">如果您支援使用協力廠商驗證提供者登入 (例如 OpenID 提供者) ，請務必將這些互動保留在 Web 驗證訊息代理程式中。</span><span class="sxs-lookup"><span data-stu-id="90b7d-159">If you support login with a third-party authentication provider (for example, OpenID providers), make sure to keep those interactions within the Web Authentication Broker.</span></span> <span data-ttu-id="90b7d-160">若要讓頁面上的所有連結都能安全地在瀏覽器中開啟，請使用星狀語法，例如，請 `  <meta name="mswebdialog-newwindowurl" content="*"/>` 注意，" \* " 只能單獨使用，且無法與另一個 URL 合併，例如 " https://www.contoso.com/\ \*" 不是有效的語法。</span><span class="sxs-lookup"><span data-stu-id="90b7d-160">To enable all links on your page as safe to be opened in the browser, use the star syntax, such as, `  <meta name="mswebdialog-newwindowurl" content="*"/>` Note that the “\*” can only be used exclusively and can’t be combined with another URL, for example, "https://www.contoso.com/\*" is not a valid syntax.</span></span>

### <a name="step-5-rules-applied-to-all-meta-tags"></a><span data-ttu-id="90b7d-161">步驟5：套用至所有元標記的規則</span><span class="sxs-lookup"><span data-stu-id="90b7d-161">Step 5: Rules applied to all meta tags</span></span>

<span data-ttu-id="90b7d-162">當 Web 驗證代理人處理中繼標記時，適用下列規則：</span><span class="sxs-lookup"><span data-stu-id="90b7d-162">When Web Authentication Broker processes meta tags, the following rules apply:</span></span>

-   <span data-ttu-id="90b7d-163">中繼標籤的效果會跨相同第二層級網域下的所有頁面保存 (例如 contoso.com) ，除非遇到相同名稱但出現不同內容的其他中繼標記。</span><span class="sxs-lookup"><span data-stu-id="90b7d-163">The effect of the meta tag will persist across all pages under same second level domain (for example, contoso.com) unless another meta tag of the same name but different content is encountered.</span></span>
-   <span data-ttu-id="90b7d-164">如果在相同的頁面上遇到相同名稱的多個中繼標記，Web 驗證代理人只會選擇其中一個，並忽略其餘部分。</span><span class="sxs-lookup"><span data-stu-id="90b7d-164">If multiple meta tags of the same name are encountered on the same page, the Web Authentication Broker will choose only one of them and ignore the rest.</span></span> <span data-ttu-id="90b7d-165">所選擇的特定中繼標記未定義。</span><span class="sxs-lookup"><span data-stu-id="90b7d-165">Which specific meta tag is chosen is undefined.</span></span>
    > [!Note]  
    > <span data-ttu-id="90b7d-166">此規則不會套用至 `mswebdialog-newwindowurl` 允許相同頁面上多個實例的中繼標籤。</span><span class="sxs-lookup"><span data-stu-id="90b7d-166">This rule does not apply to the `mswebdialog-newwindowurl` meta tag that allows multiple instances on the same page.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="90b7d-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="90b7d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b7d-168">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="90b7d-168">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="90b7d-169">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="90b7d-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="90b7d-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="90b7d-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
