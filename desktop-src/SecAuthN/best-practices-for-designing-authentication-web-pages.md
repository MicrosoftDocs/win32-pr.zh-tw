---
description: 本主題說明設計使用 Web 驗證訊息代理程式進行登入之網頁的最佳作法。
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: 設計驗證網頁的最佳做法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318723"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="45e9a-103">設計驗證網頁的最佳做法</span><span class="sxs-lookup"><span data-stu-id="45e9a-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="45e9a-104">本主題說明設計使用 Web 驗證訊息代理程式進行登入之網頁的最佳作法。</span><span class="sxs-lookup"><span data-stu-id="45e9a-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="45e9a-105">使用 metatags</span><span class="sxs-lookup"><span data-stu-id="45e9a-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="45e9a-106">使用 Windows 8 CSS 樣式</span><span class="sxs-lookup"><span data-stu-id="45e9a-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="45e9a-107">使用色彩和主題</span><span class="sxs-lookup"><span data-stu-id="45e9a-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="45e9a-108">對齊</span><span class="sxs-lookup"><span data-stu-id="45e9a-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="45e9a-109">設計嵌入式管理</span><span class="sxs-lookup"><span data-stu-id="45e9a-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="45e9a-110">設計快速且流暢的登入體驗</span><span class="sxs-lookup"><span data-stu-id="45e9a-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="45e9a-111">安全性考量</span><span class="sxs-lookup"><span data-stu-id="45e9a-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="45e9a-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="45e9a-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="45e9a-113">使用 metatags</span><span class="sxs-lookup"><span data-stu-id="45e9a-113">Use of metatags</span></span>

<span data-ttu-id="45e9a-114">使用 metatags 時，提供者 "Contoso Social" 可指定標題、圖示和標頭的色彩。</span><span class="sxs-lookup"><span data-stu-id="45e9a-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="45e9a-115">在 (WebAuthLogin.html) 的範例 HTML 檔案中，您可以使用下列程式碼來完成這項工作。</span><span class="sxs-lookup"><span data-stu-id="45e9a-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="45e9a-116">這可讓 Windows 在 UI 的標頭中，以顯著的方式整合提供者的存在，如下列螢幕擷取畫面中的紅色方塊反白顯示。</span><span class="sxs-lookup"><span data-stu-id="45e9a-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![在 ui 中顯示 contoso 標頭的登入頁面](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="45e9a-118">使用 Windows 8 CSS 樣式</span><span class="sxs-lookup"><span data-stu-id="45e9a-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="45e9a-119">提供的 ui-light 樣式表單是 Windows Store 應用程式所使用的 Windows 8 樣式表單。</span><span class="sxs-lookup"><span data-stu-id="45e9a-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="45e9a-120">它會針對印刷樣式和標準控制項（例如按鈕、文字方塊、超連結和核取方塊）定義 Windows Store 應用程式樣式，以確保它們的觸控性很容易理解。</span><span class="sxs-lookup"><span data-stu-id="45e9a-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="45e9a-121">當您設計和量身打造 Windows 8 的 web 授權頁面時，建議您使用此樣式表單，並視需要進行更新，只要您的網頁仍以自己的方式遵循最佳作法。</span><span class="sxs-lookup"><span data-stu-id="45e9a-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="45e9a-122">比方說，如果您有一個特殊的樣式表單，讓超連結看起來像是在您的網頁上，最好是仔細確定您所提供的樣式跟標準 Windows 8 超連結一樣容易使用。</span><span class="sxs-lookup"><span data-stu-id="45e9a-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="45e9a-123">這對於在其觸控裝置上使用 Windows 8 的取用者基底而言是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="45e9a-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="45e9a-124">使用色彩和主題</span><span class="sxs-lookup"><span data-stu-id="45e9a-124">Use of color and themes</span></span>

<span data-ttu-id="45e9a-125">此範例將示範如何使用幾種不同的方式來仔細使用色彩。</span><span class="sxs-lookup"><span data-stu-id="45e9a-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="45e9a-126">網頁的白色背景。</span><span class="sxs-lookup"><span data-stu-id="45e9a-126">White background for the web page.</span></span> <span data-ttu-id="45e9a-127">您可以從上一個螢幕擷取畫面中看出，網頁是裝載在橫跨畫面寬度的白色介面內。</span><span class="sxs-lookup"><span data-stu-id="45e9a-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="45e9a-128">若要確定網頁與介面整合，建議網頁必須有白色背景的外觀。</span><span class="sxs-lookup"><span data-stu-id="45e9a-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="45e9a-129">根據您的品牌色彩標示控制項。</span><span class="sxs-lookup"><span data-stu-id="45e9a-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="45e9a-130">CSS 檔案 theme-colors 提供樣式來覆寫 ui 淺色樣式表單中的標準控制項色彩，以比對控制項的主題與標頭的色彩。</span><span class="sxs-lookup"><span data-stu-id="45e9a-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="45e9a-131">例如，在下列螢幕擷取畫面中，按鈕和超連結會採用衍生自頁首色彩的色彩。</span><span class="sxs-lookup"><span data-stu-id="45e9a-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![具有與標頭相同色彩的按鈕和文字螢幕擷取畫面](images/wab-figure11.png)
-   <span data-ttu-id="45e9a-133">標題色彩。</span><span class="sxs-lookup"><span data-stu-id="45e9a-133">Header color.</span></span> <span data-ttu-id="45e9a-134">在標頭中使用 Contoso 的品牌色彩，可針對提供者在系統 UI 內的品牌建立一致的特質。</span><span class="sxs-lookup"><span data-stu-id="45e9a-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="45e9a-135">對齊</span><span class="sxs-lookup"><span data-stu-id="45e9a-135">Alignment</span></span>

<span data-ttu-id="45e9a-136">網頁本身的左邊或右邊沒有填補，以允許在左邊標題的標題和右邊的標頭中使用標題的印刷樣式對齊。</span><span class="sxs-lookup"><span data-stu-id="45e9a-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="45e9a-137">您也會注意到，按鈕一律會靠右對齊網頁 (，並靠右對齊標題) 中的圖示。</span><span class="sxs-lookup"><span data-stu-id="45e9a-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="45e9a-138">這是最佳做法，因為 Windows 8 使用者習慣于右下方具有按鈕的類似對話流程。</span><span class="sxs-lookup"><span data-stu-id="45e9a-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="45e9a-139">設計嵌入式管理</span><span class="sxs-lookup"><span data-stu-id="45e9a-139">Designing for snap</span></span>

<span data-ttu-id="45e9a-140">在下圖中，您可以看到 [登入] 和 [許可權] 頁面處於 [貼齊狀態]。</span><span class="sxs-lookup"><span data-stu-id="45e9a-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="45e9a-141">登入畫面的貼齊視圖</span><span class="sxs-lookup"><span data-stu-id="45e9a-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="45e9a-142">.</span><span class="sxs-lookup"><span data-stu-id="45e9a-142">.</span></span> ![<span data-ttu-id="45e9a-143">[許可權] 頁面的貼齊視圖</span><span class="sxs-lookup"><span data-stu-id="45e9a-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="45e9a-144">在範例檔案 ui-webauth 中，您可以看到使用媒體查詢，根據網頁的可用寬度，將頁面的版面配置優化。</span><span class="sxs-lookup"><span data-stu-id="45e9a-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="45e9a-145">以下列範圍括住的程式碼片段，可為貼齊狀態量身打造 CSS。</span><span class="sxs-lookup"><span data-stu-id="45e9a-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="45e9a-146">在 Windows 8 中，對齊狀態的寬度為320圖元。</span><span class="sxs-lookup"><span data-stu-id="45e9a-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="45e9a-147">Web 驗證頁面在上述 UI 中會佔用260圖元。</span><span class="sxs-lookup"><span data-stu-id="45e9a-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="45e9a-148">我們使用的最大寬度值具有足夠的邊界，因此提供者的媒體查詢程式碼不會系結至格線的確切寬度。</span><span class="sxs-lookup"><span data-stu-id="45e9a-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="45e9a-149">在量身打造您的應用程式時，請務必讓使用者不會遺失其在 web 驗證體驗的其他觀點中的任何內容 (完整、填滿或快速鍵的觀點) ，但要重新結構頁面中的元素版面配置和階層，以保持內容的內容是可見且互動式的，是很重要的。</span><span class="sxs-lookup"><span data-stu-id="45e9a-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="45e9a-150">我們已將範例說明如何調適此範例的網頁，以取得貼齊狀態。</span><span class="sxs-lookup"><span data-stu-id="45e9a-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="45e9a-151">例如，在 [貼齊狀態] 的 [登入] 頁面中，[輸入文字] 欄位的 [寬度] 屬性 (如) ui-light 中所指定）已被覆寫並設定為較小的數值，因此文字欄位不會水準裁剪。</span><span class="sxs-lookup"><span data-stu-id="45e9a-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="45e9a-152">另一個範例是，在 [貼齊] 狀態中，h1 和 h2 標頭的字型大小會從 42 pt 和 20 pt 分別縮減為 20 pt 和 11 pt。</span><span class="sxs-lookup"><span data-stu-id="45e9a-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="45e9a-153">這是根據 Windows 8 型別遞增來完成，並將文字優化，以在變更的區中更精簡。</span><span class="sxs-lookup"><span data-stu-id="45e9a-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="45e9a-154">另舉一個範例，請注意，[許可權] 頁面中的圖示大小較小 (相較于上述) 的完整視圖頁面。</span><span class="sxs-lookup"><span data-stu-id="45e9a-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="45e9a-155">同樣地，這是為了保留內容，同時針對已變更的功能區交換設計資產。</span><span class="sxs-lookup"><span data-stu-id="45e9a-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="45e9a-156">設計快速且流暢的登入體驗</span><span class="sxs-lookup"><span data-stu-id="45e9a-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="45e9a-157">在此網頁的設計初期，我們會在這一頁最適合的一件事，是一種快速且流暢的登入體驗。</span><span class="sxs-lookup"><span data-stu-id="45e9a-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="45e9a-158">因此，流程中最重要的 UI 是 [登入] 頁面中的 [使用者名稱] 和 [密碼] 欄位，以取得快速認證專案體驗。</span><span class="sxs-lookup"><span data-stu-id="45e9a-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="45e9a-159">雖然我們發現有其他常見的案例（例如密碼抓取）和參考隱私權聲明，但網路的豐富體驗是更適合這些經驗的地方。</span><span class="sxs-lookup"><span data-stu-id="45e9a-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="45e9a-160">針對與安全 web 驗證體驗無關的所有流程，建議您將使用者流覽至瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="45e9a-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="45e9a-161">這會顯示在範例 HTML 檔案 (WebAuthLogin.html) 如下所示： `<meta name="mswebdialog-newwindowurl" content="*" />` 這會從使用者的預設瀏覽器中的 [登入] 或 [許可權] 頁面開啟所有連結的網頁，讓使用者可以在其中完成這些流程，然後返回應用程式進行登入。</span><span class="sxs-lookup"><span data-stu-id="45e9a-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="45e9a-162">安全性考量</span><span class="sxs-lookup"><span data-stu-id="45e9a-162">Security Considerations</span></span>

<span data-ttu-id="45e9a-163">下列文章提供撰寫安全 c + + 程式碼的指引。</span><span class="sxs-lookup"><span data-stu-id="45e9a-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="45e9a-164">C + + 的安全性最佳作法</span><span class="sxs-lookup"><span data-stu-id="45e9a-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="45e9a-165">[適用于應用程式的模式 & 實務安全性指引](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="45e9a-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e9a-166">相關主題</span><span class="sxs-lookup"><span data-stu-id="45e9a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e9a-167">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="45e9a-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="45e9a-168">Web 驗證訊息代理程式的常見問題</span><span class="sxs-lookup"><span data-stu-id="45e9a-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="45e9a-169">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="45e9a-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="45e9a-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="45e9a-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
