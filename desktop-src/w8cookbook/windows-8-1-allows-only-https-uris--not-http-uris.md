---
title: Windows 8.1 中的 Uri
description: Windows 8.1 只允許 HTTPs Uri，而非 HTTP Uri
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382545"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a><span data-ttu-id="42856-103">Windows 8.1 只允許 HTTPs Uri，而非 HTTP Uri</span><span class="sxs-lookup"><span data-stu-id="42856-103">Windows 8.1 allows only https URIs, not http URIs</span></span>

## <a name="platforms"></a><span data-ttu-id="42856-104">平台</span><span class="sxs-lookup"><span data-stu-id="42856-104">Platforms</span></span>

<dl> <span data-ttu-id="42856-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="42856-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="42856-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="42856-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="42856-107">Description</span><span class="sxs-lookup"><span data-stu-id="42856-107">Description</span></span>

<span data-ttu-id="42856-108">針對 Windows 8 所建立的應用程式可以在其應用程式內容 Uri 中包含 HTTP 和 HTTPs Uri，針對 Windows 8.1 所建立的應用程式可能只包含 HTTPs Uri。</span><span class="sxs-lookup"><span data-stu-id="42856-108">While apps built for Windows 8 can include http and https URIs in their application content URIs, apps built for Windows 8.1 may include only https URIs.</span></span>

<span data-ttu-id="42856-109">唯一的例外是應用程式 AppxManifest.xml 檔中所指定的動態 ContentUriRules。</span><span class="sxs-lookup"><span data-stu-id="42856-109">The only exception is for dynamic ContentUriRules that are specified in the app’s AppxManifest.xml file.</span></span> <span data-ttu-id="42856-110">使用動態 ContentUriRules，應用程式可以存取系統管理員提供的其他網域或網路資源，例如群組原則的 Uri。</span><span class="sxs-lookup"><span data-stu-id="42856-110">With dynamic ContentUriRules, apps can access additional domains or network resources that are provided by the admin, such as Group Policy URIs.</span></span> <span data-ttu-id="42856-111">不過，只有在符合下列條件的情況下，Windows Store 應用程式才能使用動態 ContentUriRules：</span><span class="sxs-lookup"><span data-stu-id="42856-111">However, dynamic ContentUriRules are only available to Windows Store apps if they meet these conditions:</span></span>

-   <span data-ttu-id="42856-112">群組原則已啟用</span><span class="sxs-lookup"><span data-stu-id="42856-112">The Group Policy is enabled</span></span>
-   <span data-ttu-id="42856-113">封裝指定了 enterpriseAuthentication 功能</span><span class="sxs-lookup"><span data-stu-id="42856-113">The package has specified the enterpriseAuthentication capability</span></span>
-   <span data-ttu-id="42856-114">封裝的 OSMaxVersionTested Windows 8.1 或更高</span><span class="sxs-lookup"><span data-stu-id="42856-114">The package’s OSMaxVersionTested is Windows 8.1 or greater</span></span>

<span data-ttu-id="42856-115">Windows 8.1 的新限制是增強式安全性限制的一部分，可進一步保護平臺。</span><span class="sxs-lookup"><span data-stu-id="42856-115">The new restrictions in Windows 8.1 are part of enhanced security restrictions to further protect the platform.</span></span>

## <a name="manifestations"></a><span data-ttu-id="42856-116">表現</span><span class="sxs-lookup"><span data-stu-id="42856-116">Manifestations</span></span>

<span data-ttu-id="42856-117">在 Windows 8.1 上執行針對 Windows 8 所建立的應用程式時，允許在 [s](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) 中使用 HTTP uri。</span><span class="sxs-lookup"><span data-stu-id="42856-117">When running an app built for Windows 8 on Windows 8.1, the use of http URIs in the [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) is allowed.</span></span>

## <a name="mitigations"></a><span data-ttu-id="42856-118">風險降低</span><span class="sxs-lookup"><span data-stu-id="42856-118">Mitigations</span></span>

<span data-ttu-id="42856-119">我們建議 WWA 開發人員從 [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)) 的 (<[](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) x->---</span><span class="sxs-lookup"><span data-stu-id="42856-119">We recommend that WWA developers switch from [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) to the [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) control (<x-ms-webview>).</span></span> <span data-ttu-id="42856-120">但是，如果您需要 AppCache、IndexedDB、地理位置或以程式設計方式存取剪貼簿存取的支援，您將需要繼續使用</span><span class="sxs-lookup"><span data-stu-id="42856-120">However, if you need support for AppCache, IndexedDB, geolocation, or programmatic clipboard access, you will need to continue using</span></span> <iframe> <span data-ttu-id="42856-121">適用于 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="42856-121">for Windows 8.1.</span></span>

<span data-ttu-id="42856-122">持續使用</span><span class="sxs-lookup"><span data-stu-id="42856-122">Continued usage of</span></span> <iframe> <span data-ttu-id="42856-123">針對遠端內容，應用程式的 s 中需要有新專案。</span><span class="sxs-lookup"><span data-stu-id="42856-123">for remote content will require a new entry in the ApplicationContentUriRules for the app.</span></span> <span data-ttu-id="42856-124">如果 web 內容需要叫用 s，則使用 web 內容的應用程式需要新的專案。請通知產生 [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) 事件。</span><span class="sxs-lookup"><span data-stu-id="42856-124">Apps with WebView require new entries in the ApplicationContentUriRules if the web content needs to invoke window.external.notify for generating a [ScriptNotify](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) event.</span></span> <span data-ttu-id="42856-125">如果您沒有 Visual Studio，可以藉由新增下列 XML 來更新應用程式資訊清單，包括子域的萬用字元 (例如 HTTPs:// \* . microsoft.com) ：</span><span class="sxs-lookup"><span data-stu-id="42856-125">If you do not have Visual Studio, you can update the app manifest by adding the following XML, including wildcards for subdomains (e.g. https://\*.microsoft.com):</span></span>


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a><span data-ttu-id="42856-126">資源</span><span class="sxs-lookup"><span data-stu-id="42856-126">Resources</span></span>

-   [<span data-ttu-id="42856-127">ApplicationContentUriRules</span><span class="sxs-lookup"><span data-stu-id="42856-127">ApplicationContentUriRules</span></span>](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<span data-ttu-id="42856-128"><iframe> element \| <iframe> 物件</span><span class="sxs-lookup"><span data-stu-id="42856-128"><iframe> element \| <iframe> object</span></span>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [<span data-ttu-id="42856-129">Web 類型類別</span><span class="sxs-lookup"><span data-stu-id="42856-129">Webview class</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [<span data-ttu-id="42856-130">ScriptNotify 事件</span><span class="sxs-lookup"><span data-stu-id="42856-130">WebView.ScriptNotify event</span></span>](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 