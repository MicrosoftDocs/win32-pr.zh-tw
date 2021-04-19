---
description: 為了簡化 proxy 設定的設定，WinHTTP 5.1 會 (WPAD) 通訊協定（也稱為自動代理程式）來實行 Web Proxy 自動探索。
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: WinHTTP 自動代理支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973848"
---
# <a name="winhttp-autoproxy-support"></a><span data-ttu-id="a47c7-103">WinHTTP 自動代理支援</span><span class="sxs-lookup"><span data-stu-id="a47c7-103">WinHTTP AutoProxy Support</span></span>

<span data-ttu-id="a47c7-104">為了簡化 proxy 設定的設定，WinHTTP 5.1 會 (WPAD) 通訊協定（也稱為自動代理程式）來實行 Web Proxy 自動探索。</span><span class="sxs-lookup"><span data-stu-id="a47c7-104">To ease the configuration of proxy settings, WinHTTP 5.1 implements the Web Proxy Auto-Discovery (WPAD) protocol, also known as autoproxy.</span></span>

## <a name="overview-of-autoproxy"></a><span data-ttu-id="a47c7-105">自動代理程式總覽</span><span class="sxs-lookup"><span data-stu-id="a47c7-105">Overview of AutoProxy</span></span>

<span data-ttu-id="a47c7-106">使用 WinHTTP 傳送 HTTP 要求的應用程式和元件應確定已正確設定 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="a47c7-106">Applications and components that use WinHTTP to send HTTP requests should ensure that the proxy configuration is set correctly.</span></span> <span data-ttu-id="a47c7-107">除非用戶端有直接的網際網路連線，否則 HTTP 要求通常會透過將用戶端區域網路連線到網際網路的 web proxy 伺服器傳送 (例如，通常是在公司 LAN 上的 Web 用戶端) 的情況。</span><span class="sxs-lookup"><span data-stu-id="a47c7-107">Unless the client has a direct Internet connection, an HTTP request should normally be sent through a web proxy server that connects the client's local network to the Internet (for example, this is often the case for Web clients on a corporate LAN).</span></span> <span data-ttu-id="a47c7-108">若是以伺服器為基礎的應用程式，則 proxy 設定通常是由伺服器的系統管理員使用 WinHTTP ProxyCfg.exe 公用程式來管理。</span><span class="sxs-lookup"><span data-stu-id="a47c7-108">For server-based applications, the proxy configuration is normally managed by the server's administrator using the WinHTTP ProxyCfg.exe utility.</span></span> <span data-ttu-id="a47c7-109">伺服器管理員事先知道 proxy 伺服器的名稱，並使用 ProxyCfg.exe 將此設定記錄在 WinHTTP 可以查詢的登錄中。</span><span class="sxs-lookup"><span data-stu-id="a47c7-109">The server administrator knows the name of the proxy server in advance and uses ProxyCfg.exe to record this setting in the registry where WinHTTP can look it up.</span></span> <span data-ttu-id="a47c7-110">不過，要求用戶端桌面使用者手動設定 WinHTTP proxy 設定有問題。</span><span class="sxs-lookup"><span data-stu-id="a47c7-110">However, requiring client desktop end-users to manually configure WinHTTP proxy settings is problematic.</span></span> <span data-ttu-id="a47c7-111">終端使用者可能不知道 proxy 伺服器的名稱;要求終端使用者執行 ProxyCfg.exe 公用程式，可能是組織的支援負擔。</span><span class="sxs-lookup"><span data-stu-id="a47c7-111">The end-user may not know the name of the proxy server; requiring the end-user to run the ProxyCfg.exe utility can be a support burden for an organization.</span></span> <span data-ttu-id="a47c7-112">為了支援絕佳的使用者體驗，有 web 功能的用戶端應用程式應該判斷 proxy 設定，而不需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="a47c7-112">To support a good user experience, a web-enabled client application should determine the proxy configuration without user intervention.</span></span>

<span data-ttu-id="a47c7-113">為了讓您更輕鬆地設定以 WinHTTP 為基礎之應用程式的 proxy 設定，WinHTTP 現在會將 [Web Proxy 自動探索 (WPAD) 通訊協定](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)，通常稱為自動 *代理* 程式。</span><span class="sxs-lookup"><span data-stu-id="a47c7-113">To make configuring the proxy settings for WinHTTP-based applications easier, WinHTTP now implements the [Web Proxy Auto-Discovery (WPAD) protocol](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), often referred to as *autoproxy*.</span></span> <span data-ttu-id="a47c7-114">這是 web 瀏覽器所執行的相同通訊協定，可自動探索 proxy 設定，而不需要使用者手動指定 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a47c7-114">This is the same protocol that web browsers implement to automatically discover the proxy configuration without requiring an end-user to specify a proxy server manually.</span></span> <span data-ttu-id="a47c7-115">從 Windows 2000 Service Pack 3、Windows XP Service Pack 1 和 Windows Server 2003 中的 WinHTTP 5.1 版開始，可以使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="a47c7-115">This feature is available starting with WinHTTP version 5.1 in Windows 2000 Service Pack 3, Windows XP Service Pack 1 and Windows Server 2003.</span></span> <span data-ttu-id="a47c7-116">請注意，雖然 Microsoft Internet Explorer 和 Microsoft WinHTTP 都支援 WPAD，但該規格絕不會超過「網際網路草稿」階段，並于2001年5月過期。</span><span class="sxs-lookup"><span data-stu-id="a47c7-116">Note that although both Microsoft Internet Explorer and Microsoft WinHTTP support WPAD, the specification never progressed beyond the "Internet-Draft" stage, and expired in May 2001.</span></span>

<span data-ttu-id="a47c7-117">WPAD 通訊協定的運作方式如下：</span><span class="sxs-lookup"><span data-stu-id="a47c7-117">The WPAD protocol works as follows:</span></span>

1.  <span data-ttu-id="a47c7-118">使用 DHCP 和（或） DNS 網路通訊協定時，會探索 Proxy 自動設定 (PAC) 檔的 URL。</span><span class="sxs-lookup"><span data-stu-id="a47c7-118">Using the DHCP and/or DNS network protocols, the URL of a Proxy Auto-Configuration (PAC) file is discovered.</span></span> <span data-ttu-id="a47c7-119">URL 會在用戶端的區域網路上識別 PAC 檔案。</span><span class="sxs-lookup"><span data-stu-id="a47c7-119">The URL identifies a PAC file on the client's local network.</span></span> <span data-ttu-id="a47c7-120">WinHTTP 只支援 "HTTP：" 和 "HTTPs：" PAC Url;例如，它不支援 "file：" URL。</span><span class="sxs-lookup"><span data-stu-id="a47c7-120">WinHTTP supports only "http:" and "https:" PAC URLs; it does not, for example, support "file:" URLS.</span></span>
2.  <span data-ttu-id="a47c7-121">PAC 檔案會下載並選擇性地快取在用戶端的電腦上。</span><span class="sxs-lookup"><span data-stu-id="a47c7-121">The PAC file is downloaded and optionally cached on the client's computer.</span></span> <span data-ttu-id="a47c7-122">PAC 檔案是可執行檔腳本，它會根據指定的目標主機名稱和 URL，產生一或多個 proxy 伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="a47c7-122">The PAC file is an executable script that generates a list of one or more proxy servers given a target host name and URL.</span></span> <span data-ttu-id="a47c7-123">WinHTTP 只支援 ECMAScript 型 PAC 檔案。</span><span class="sxs-lookup"><span data-stu-id="a47c7-123">WinHTTP supports only ECMAScript-based PAC files.</span></span>
3.  <span data-ttu-id="a47c7-124">在每個 HTTP 要求中，會執行 PAC 腳本程式碼，並將 HTTP 要求的主機名稱和 URL 當作參數傳入。</span><span class="sxs-lookup"><span data-stu-id="a47c7-124">On each HTTP request, the PAC script code is executed, with the host name and URL of the HTTP request passed in as parameters.</span></span> <span data-ttu-id="a47c7-125">WinHTTP 預期 PAC 腳本程式碼必須包含名為 **FindProxyForURL** 的函式，格式如下：</span><span class="sxs-lookup"><span data-stu-id="a47c7-125">WinHTTP expects the PAC script code to contain a function called **FindProxyForURL**, in the form:</span></span>
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    <span data-ttu-id="a47c7-126">此函式會計算可供 HTTP 用戶端用來傳輸要求的一或多個 proxy 伺服器的清單。</span><span class="sxs-lookup"><span data-stu-id="a47c7-126">This function computes a list of one or more proxy servers that can be used by the HTTP client in order to transmit the request.</span></span> <span data-ttu-id="a47c7-127">如果 PAC 腳本判斷 HTTP 用戶端可以直接連線到目標伺服器而不需要通過 proxy 伺服器，則會使用特殊的傳回值來指出這一點。</span><span class="sxs-lookup"><span data-stu-id="a47c7-127">If the PAC script determines that the HTTP client can reach the target server directly without going through a proxy server at all, it indicates this using a special return value.</span></span>

## <a name="autoproxy-topics"></a><span data-ttu-id="a47c7-128">自動代理主題</span><span class="sxs-lookup"><span data-stu-id="a47c7-128">AutoProxy Topics</span></span>

-   [<span data-ttu-id="a47c7-129">WinHTTP 自動代理函數</span><span class="sxs-lookup"><span data-stu-id="a47c7-129">WinHTTP AutoProxy Functions</span></span>](winhttp-autoproxy-api.md)
-   [<span data-ttu-id="a47c7-130">沒有自動設定檔的探索</span><span class="sxs-lookup"><span data-stu-id="a47c7-130">Discovery Without an Auto-Config File</span></span>](discovery-without-an-auto-config-file.md)
-   [<span data-ttu-id="a47c7-131">WinHTTP 中的自動代理問題</span><span class="sxs-lookup"><span data-stu-id="a47c7-131">AutoProxy Issues in WinHTTP</span></span>](autoproxy-issues-in-winhttp.md)
-   [<span data-ttu-id="a47c7-132">在 WinHTTP 中設定 WinInet Proxy 設定</span><span class="sxs-lookup"><span data-stu-id="a47c7-132">Setting WinInet Proxy Configurations in WinHTTP</span></span>](setting-wininet-proxy-configurations-in-winhttp.md)
-   [<span data-ttu-id="a47c7-133">自動代理快取</span><span class="sxs-lookup"><span data-stu-id="a47c7-133">AutoProxy Cache</span></span>](autoproxy-cache.md)
-   [<span data-ttu-id="a47c7-134">瀏覽器自動設定檔案格式的 IPv6 擴充功能</span><span class="sxs-lookup"><span data-stu-id="a47c7-134">IPv6 Extensions to Navigator Auto-Config File Format</span></span>](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



