---
description: Web 驗證訊息代理程式建置於與 Windows Internet Explorer 的相同技術之上。
ms.assetid: 4BBAE30F-63AB-4AB0-9C99-016EF05220E8
title: 網頁開發的考量
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbe7e738616589afc4f7ba4f03d92a12207d189c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319379"
---
# <a name="considerations-for-the-web-page-development"></a><span data-ttu-id="2e3ba-103">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="2e3ba-103">Considerations for the web page development</span></span>

<span data-ttu-id="2e3ba-104">Web 驗證訊息代理程式建置於與 Windows Internet Explorer 的相同技術之上。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-104">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="2e3ba-105">不過，由於此元件的特殊用途，Internet Explorer 的某些功能已停用或鎖定特定的設定。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-105">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <span data-ttu-id="2e3ba-106">此外，Web 驗證訊息代理程式也提供專用的事件記錄通道，以協助針對其處理的頁面問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-106">Also, Web Authentication Broker provides a dedicated event logging channel to help troubleshoot issues with pages that it processes.</span></span>

## <a name="internet-explorer-10-standard-document-mode"></a><span data-ttu-id="2e3ba-107">Internet Explorer 10 標準檔案模式</span><span class="sxs-lookup"><span data-stu-id="2e3ba-107">Internet Explorer 10 standard document mode</span></span>

<span data-ttu-id="2e3ba-108">Web 驗證訊息代理程式會顯示「IE10 標準模式」中的所有頁面。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-108">The Web Authentication Broker displays all pages in the "IE10 Standards Mode".</span></span> <span data-ttu-id="2e3ba-109">您可以使用 Internet Explorer 中的開發人員工具，查看頁面在不同檔案模式下的運作方式。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-109">You can use the developer tools in Internet Explorer to see how your page works under different document modes.</span></span> <span data-ttu-id="2e3ba-110">如需 Internet Explorer 10 相容性的詳細資訊，請參閱 [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85))的 MSDN 主題。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-110">For more information on Internet Explorer 10 compatibility, see the MSDN topics for [Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/dev-guides/hh673527(v=vs.85)).</span></span>

## <a name="disabled-and-locked-down-features"></a><span data-ttu-id="2e3ba-111">停用和鎖定功能</span><span class="sxs-lookup"><span data-stu-id="2e3ba-111">Disabled and locked down features</span></span>

<span data-ttu-id="2e3ba-112">Internet Explorer 的數項功能完全停用，或鎖定為無法在作業系統的網際網路選項中變更的特定值。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-112">Several features of Internet Explorer are either completely disabled or locked down to specific values that can’t be changed in the Internet Options of the operating system.</span></span>



| <span data-ttu-id="2e3ba-113">功能</span><span class="sxs-lookup"><span data-stu-id="2e3ba-113">Feature</span></span>                            | <span data-ttu-id="2e3ba-114">狀態</span><span class="sxs-lookup"><span data-stu-id="2e3ba-114">Status</span></span>                                                                                                                                                                                                          |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ba-115">應用程式快取 API ( "AppCache" ) </span><span class="sxs-lookup"><span data-stu-id="2e3ba-115">Application Cache API ("AppCache")</span></span> | <span data-ttu-id="2e3ba-116">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-116">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="2e3ba-117">連結歷程記錄</span><span class="sxs-lookup"><span data-stu-id="2e3ba-117">Link history</span></span>                       | <span data-ttu-id="2e3ba-118">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-118">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="2e3ba-119">暫存檔案</span><span class="sxs-lookup"><span data-stu-id="2e3ba-119">Temporary files</span></span>                    | <span data-ttu-id="2e3ba-120">已啟用</span><span class="sxs-lookup"><span data-stu-id="2e3ba-120">Enabled</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="2e3ba-121">Cookie</span><span class="sxs-lookup"><span data-stu-id="2e3ba-121">Cookies</span></span>                            | <span data-ttu-id="2e3ba-122">會話 cookie 已啟用。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-122">Session cookies are enabled.</span></span> <span data-ttu-id="2e3ba-123">允許保存的 cookie，但受限於自動清除，除非 Web 驗證訊息代理程式是在 SSO 模式中。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-123">Persisted cookies are allowed, but are subject to automatic cleanup unless the Web Authentication Broker is in the SSO mode.</span></span> <span data-ttu-id="2e3ba-124">如需詳細資訊，請參閱「單一登入」一節。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-124">For more information, see the Single Sign On section.</span></span> |
| <span data-ttu-id="2e3ba-125">索引資料庫</span><span class="sxs-lookup"><span data-stu-id="2e3ba-125">Index DB</span></span>                           | <span data-ttu-id="2e3ba-126">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-126">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="2e3ba-127">DOM 儲存體</span><span class="sxs-lookup"><span data-stu-id="2e3ba-127">DOM storage</span></span>                        | <span data-ttu-id="2e3ba-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-128">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="2e3ba-129">ActiveX</span><span class="sxs-lookup"><span data-stu-id="2e3ba-129">ActiveX</span></span>                            | <span data-ttu-id="2e3ba-130">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-130">Disabled</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="2e3ba-131">檔案下載</span><span class="sxs-lookup"><span data-stu-id="2e3ba-131">File downloads</span></span>                     | <span data-ttu-id="2e3ba-132">Disabled</span><span class="sxs-lookup"><span data-stu-id="2e3ba-132">Disabled</span></span>                                                                                                                                                                                                        |



 

## <a name="https-requirement"></a><span data-ttu-id="2e3ba-133">HTTPS 需求</span><span class="sxs-lookup"><span data-stu-id="2e3ba-133">HTTPS requirement</span></span>

<span data-ttu-id="2e3ba-134">應用程式將用來與線上提供者通訊的第一個 URL 必須是 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-134">The first URL that an application will use to communicate with the online provider is required to be HTTPS.</span></span>

## <a name="dimension-for-different-window-sizes"></a><span data-ttu-id="2e3ba-135">不同視窗大小的維度</span><span class="sxs-lookup"><span data-stu-id="2e3ba-135">Dimension for different window sizes</span></span>

<span data-ttu-id="2e3ba-136">Windows 8 的應用程式可能會以數種不同的大小顯示，例如全螢幕、已調整大小的視窗，或像是共用快速鍵在內的快速鍵。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-136">A Windows 8 app may appear in several different sizes such as full screen, a resized window, or within a Charm such as Share Charm.</span></span> <span data-ttu-id="2e3ba-137">根據 Web 驗證訊息代理程式所顯示的視窗版面配置，網頁必須使用的大小可能會不同。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-137">Depending in which window layout the Web Authentication Broker appears, the size with which the web pages have to work could be different.</span></span> <span data-ttu-id="2e3ba-138">如需詳細資訊，請參閱 [調整成窄版面配置的指導方針](/previous-versions/windows/hh465371(v=win.10)) 和 [共用內容主題的指導方針](/previous-versions/windows/hh465251(v=win.10)) 。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-138">For more information, see the [Guidelines for resizing to narrow layouts](/previous-versions/windows/hh465371(v=win.10)) topic and the [Guidelines for sharing content](/previous-versions/windows/hh465251(v=win.10)) topic.</span></span>

<span data-ttu-id="2e3ba-139">網頁應該使用 CSS 媒體查詢來檢查它必須使用的大小，並據此加以配置。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-139">The web page should use CSS media queries to check the size it has to work with and lay itself out accordingly.</span></span> <span data-ttu-id="2e3ba-140">不過，此頁面不應根據此處記載的確切圖元來設計，而且應該能夠調整成不同的大小。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-140">However, the page should not be designed based on the exact pixels documented here and should be able to scale to different sizes.</span></span> <span data-ttu-id="2e3ba-141">本檔中指定的大小可能會在未來的作業系統版本中變更。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-141">The sizes specified in this document are subject to change in future OS versions.</span></span>

<span data-ttu-id="2e3ba-142">如果頁面無法容納分配空間中的所有資訊 (例如，應用程式要求的一長串許可權) ，Web 驗證代理人會提供捲軸，讓使用者視需要滾動頁面。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-142">If a page can’t fit all of the information in the allotted space (for example, a long list of permissions that an application is requesting), the Web Authentication Broker will provide scroll bars to allow the user to scroll the page as needed.</span></span> <span data-ttu-id="2e3ba-143">縮放功能也是由適用于桌上型電腦和膝上型電腦的縮放縮放裝置和 Ctrl + 滑鼠滾輪提供。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-143">Zooming is also provided by pinch zoom for touch-based devices and Ctrl + mouse wheel for desktop and laptop PCs.</span></span>

<span data-ttu-id="2e3ba-144">若要測試不同的縮放比例，請使用 Microsoft Visual Studio Professional 2012 中載入的 [Web 驗證 BROKER SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) ，以允許模擬全螢幕和調整大小的狀態。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-144">To test different scaling factors use the [Web Authentication Broker SDK sample app](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) loaded in Microsoft Visual Studio Professional 2012 which allows simulating the full screen and resized states.</span></span>

<span data-ttu-id="2e3ba-145">除了上述的不同版面配置之外，請務必以不同的螢幕方向測試您的頁面 (例如，直向和橫向) ，以及不同的地區設定和語言，以及協助工具功能，例如 [讓所有專案變大] 選項開啟。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-145">In addition to different layouts documented above, make sure to test your page in different screen orientation (for example, portrait and landscape), and different locales and languages as well as with accessibility features such as the "Make everything bigger" option turned on.</span></span>

<span data-ttu-id="2e3ba-146">可用的版面配置如下：</span><span class="sxs-lookup"><span data-stu-id="2e3ba-146">The available layouts are:</span></span>

-   [<span data-ttu-id="2e3ba-147">全螢幕</span><span class="sxs-lookup"><span data-stu-id="2e3ba-147">Full screen</span></span>](#full-screen)
-   [<span data-ttu-id="2e3ba-148">調整大小的視窗</span><span class="sxs-lookup"><span data-stu-id="2e3ba-148">Resized window</span></span>](#resized)
-   [<span data-ttu-id="2e3ba-149">快速鍵視圖</span><span class="sxs-lookup"><span data-stu-id="2e3ba-149">Charm view</span></span>](#charm-view)
-   [<span data-ttu-id="2e3ba-150">檔案選擇器視圖</span><span class="sxs-lookup"><span data-stu-id="2e3ba-150">File picker view</span></span>](#file-picker-view)

### <a name="full-screen"></a><span data-ttu-id="2e3ba-151">全螢幕</span><span class="sxs-lookup"><span data-stu-id="2e3ba-151">Full screen</span></span>

<span data-ttu-id="2e3ba-152">針對全螢幕版面配置，網頁尺寸如下：</span><span class="sxs-lookup"><span data-stu-id="2e3ba-152">For the full screen layout, the web page dimensions are:</span></span>

-   <span data-ttu-id="2e3ba-153">寬度：566圖元</span><span class="sxs-lookup"><span data-stu-id="2e3ba-153">Width: 566 pixels</span></span>
-   <span data-ttu-id="2e3ba-154">高度：螢幕高度 (取決於螢幕解析度) </span><span class="sxs-lookup"><span data-stu-id="2e3ba-154">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="2e3ba-155">下列範例會顯示全螢幕版面配置中的 web 驗證訊息代理程式 UI。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-155">The following example shows the web authentication broker UI in full screen layout.</span></span>

![全螢幕版面配置中的 web 驗證訊息代理程式 ui 範例](images/wab-figure2.png)

### <a name="resized"></a><span data-ttu-id="2e3ba-157">調整</span><span class="sxs-lookup"><span data-stu-id="2e3ba-157">Resized</span></span>

<span data-ttu-id="2e3ba-158">針對調整大小的視窗，網頁尺寸可以是：</span><span class="sxs-lookup"><span data-stu-id="2e3ba-158">For a resized window, the web page dimensions can be:</span></span>

-   <span data-ttu-id="2e3ba-159">寬度：260圖元</span><span class="sxs-lookup"><span data-stu-id="2e3ba-159">Width: 260 pixels</span></span>
-   <span data-ttu-id="2e3ba-160">高度：螢幕高度 (取決於螢幕解析度) </span><span class="sxs-lookup"><span data-stu-id="2e3ba-160">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="2e3ba-161">下列範例會在 XBox 網頁上的調整大小的視窗中，顯示 Web 驗證訊息代理程式 UI。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-161">The following example shows the Web Authentication Broker UI in a resized window on the XBox web page.</span></span> <span data-ttu-id="2e3ba-162">請注意，Web 驗證訊息代理程式 UI 只會在螢幕擷取畫面的右側。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-162">Note that the Web Authentication Broker UI is only on the right side of the screen capture.</span></span>

![已調整大小之視窗中的 web 驗證訊息代理程式 ui 範例](images/wab-figure3.png)

### <a name="charm-view"></a><span data-ttu-id="2e3ba-164">快速鍵視圖</span><span class="sxs-lookup"><span data-stu-id="2e3ba-164">Charm view</span></span>

<span data-ttu-id="2e3ba-165">針對快速鍵視圖，網頁尺寸如下：</span><span class="sxs-lookup"><span data-stu-id="2e3ba-165">For the Charm view, the web page dimensions are:</span></span>

-   <span data-ttu-id="2e3ba-166">寬度：566圖元</span><span class="sxs-lookup"><span data-stu-id="2e3ba-166">Width: 566 pixels</span></span>
-   <span data-ttu-id="2e3ba-167">高度：螢幕高度 (取決於螢幕解析度) </span><span class="sxs-lookup"><span data-stu-id="2e3ba-167">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="2e3ba-168">下列範例顯示 [快速鍵] 視圖中的 Web 驗證訊息代理程式 UI。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-168">The following example shows the Web Authentication Broker UI in Charm view.</span></span>

![範例顯示快速鍵 view 中的 web 驗證訊息代理程式 ui](images/wab-figure4.png)

### <a name="file-picker-view"></a><span data-ttu-id="2e3ba-170">檔案選擇器視圖</span><span class="sxs-lookup"><span data-stu-id="2e3ba-170">File picker view</span></span>

<span data-ttu-id="2e3ba-171">針對檔案選擇器視圖，網頁尺寸如下：</span><span class="sxs-lookup"><span data-stu-id="2e3ba-171">For the file picker view, the web page dimensions are:</span></span>

-   <span data-ttu-id="2e3ba-172">寬度：566圖元</span><span class="sxs-lookup"><span data-stu-id="2e3ba-172">Width: 566 pixels</span></span>
-   <span data-ttu-id="2e3ba-173">高度：螢幕高度 (取決於螢幕解析度) </span><span class="sxs-lookup"><span data-stu-id="2e3ba-173">Height: Screen height (depends on the screen resolution)</span></span>

<span data-ttu-id="2e3ba-174">下列範例顯示 [檔案選擇器] 中的 [Web 驗證代理人] UI。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-174">The following example shows the Web Authentication Broker UI in file picker view.</span></span>

![範例顯示 [檔案選擇器] 視圖中的 web 驗證訊息代理程式 ui](images/wab-figure5.png)

## <a name="no-new-windows-by-default"></a><span data-ttu-id="2e3ba-176">預設沒有任何新視窗</span><span class="sxs-lookup"><span data-stu-id="2e3ba-176">No new windows by default</span></span>

<span data-ttu-id="2e3ba-177">依預設，沒有任何 Url 將會開啟新視窗，但是會顯示在 Web 驗證訊息代理程式視窗中。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-177">By default, no URLs will result in a new window being opened but will instead be displayed within the Web Authentication Broker window.</span></span> <span data-ttu-id="2e3ba-178">這包括 window。開啟 JavaScript 方法、超連結的「目標」屬性，或當使用者使用 Ctrl + 按一下機制來強制開啟新視窗時。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-178">This includes window.open JavaScript method, "target" attribute of the hyperlinks, or when the user uses the Ctrl+Click mechanism to force a new window to open.</span></span> <span data-ttu-id="2e3ba-179">這項規則的例外狀況是，當網頁在瀏覽器中宣告可安全流覽的連結時（如自訂超連結的目標所述）。</span><span class="sxs-lookup"><span data-stu-id="2e3ba-179">The exception to this rule is when a web page declares a link as safe to be navigated in a browser as described in the Customizing Target of the Hyperlinks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e3ba-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="2e3ba-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e3ba-181">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="2e3ba-181">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="2e3ba-182">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="2e3ba-182">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
