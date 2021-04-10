---
description: Proxy 定位器設定
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Proxy 定位器設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114369"
---
# <a name="proxy-locator-configuration-settings"></a><span data-ttu-id="9f249-103">Proxy 定位器設定</span><span class="sxs-lookup"><span data-stu-id="9f249-103">Proxy Locator Configuration Settings</span></span>

<span data-ttu-id="9f249-104">本主題說明預設 proxy 定位器的設定。</span><span class="sxs-lookup"><span data-stu-id="9f249-104">This topic describes the configuration settings for the default proxy locator.</span></span> <span data-ttu-id="9f249-105">如需有關使用自訂設定來建立 proxy 定位器的詳細資訊，請參閱 [如何設定 Proxy 定位器](how-to-configure-the-proxy-locator.md)。</span><span class="sxs-lookup"><span data-stu-id="9f249-105">For information about creating the proxy locator with custom configuration settings, see [How to Configure the Proxy Locator](how-to-configure-the-proxy-locator.md).</span></span>

<span data-ttu-id="9f249-106">Proxy 定位器可以設定為以三種模式運作： *手動模式*、 *自動偵測模式* 和 *瀏覽器模式*。</span><span class="sxs-lookup"><span data-stu-id="9f249-106">The proxy locator can be configured to operate in three modes: *manual mode*, *auto-detect mode*, and *browser mode*.</span></span> <span data-ttu-id="9f249-107">這些值定義于 [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="9f249-107">The values are defined in [**MFNET\_PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) enumeration.</span></span> <span data-ttu-id="9f249-108">應用程式可以藉由設定 [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) 屬性來設定模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-108">The application can configure the mode by setting the [**MFNETSOURCE\_PROXYSETTINGS**](mfnetsource-proxysettings-property.md) property.</span></span> <span data-ttu-id="9f249-109">您也可以將此屬性設定為 **MFNET \_ PROXYSETTING \_ NONE**，以將 proxy 定位器設定為不使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9f249-109">The proxy locator can also be configured not to use a proxy server by setting this property to **MFNET\_PROXYSETTING\_NONE**.</span></span> <span data-ttu-id="9f249-110">如果媒體伺服器是本機主機，或應用程式要求類別 (127. x. x. x. x. x. x. x. x. x. x) —保留給回送測試，則不會使用 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9f249-110">The proxy server is not used if the media server is a local host or the application requests a class A address (127.x.x.x)—reserved for loopback tests.</span></span>

> [!Caution]  
> <span data-ttu-id="9f249-111">Proxy 伺服器是內部網路與網際網路之間的安全性屏障。</span><span class="sxs-lookup"><span data-stu-id="9f249-111">A proxy server is a security barrier between your intranet and the Internet.</span></span> <span data-ttu-id="9f249-112">若未使用 proxy 伺服器，則會暴露網路的安全性威脅。</span><span class="sxs-lookup"><span data-stu-id="9f249-112">Not using a proxy server can expose the network to security threats.</span></span>

 

-   <span data-ttu-id="9f249-113">手動模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-113">Manual Mode.</span></span> <span data-ttu-id="9f249-114">應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ MANUAL** 來設定此模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-114">The application sets this mode by setting the [**MFNETSOURCE\_PROXYSETTING**](mfnetsource-proxysettings-property.md) property to **MFNET\_PROXYSETTING\_MANUAL**.</span></span> <span data-ttu-id="9f249-115">應用程式必須指定下列連接資訊：</span><span class="sxs-lookup"><span data-stu-id="9f249-115">The application must specify the following connection information:</span></span>

    -   <span data-ttu-id="9f249-116">Proxy 伺服器的主機名稱： [**MFNETSOURCE \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f249-116">Hostname of the proxy server: [**MFNETSOURCE\_PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) property.</span></span>
    -   <span data-ttu-id="9f249-117">埠號碼： [**MFNETSOURCE \_ PROXYPORT**](mfnetsource-proxyport-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f249-117">Port number: [**MFNETSOURCE\_PROXYPORT**](mfnetsource-proxyport-property.md) property.</span></span>
    -   <span data-ttu-id="9f249-118">是否針對本機位址使用 proxy 伺服器： [**MFNETSOURCE \_ PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f249-118">Whether to use a proxy server for local addresses: [**MFNETSOURCE\_PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) property.</span></span> <span data-ttu-id="9f249-119">這個設定是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="9f249-119">This setting is optional.</span></span> <span data-ttu-id="9f249-120">如果未指定此值，則 proxy 定位器會使用預設值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9f249-120">If this is not specified, then the proxy locator uses a default value of **FALSE**.</span></span>

        > [!Note]  
        > <span data-ttu-id="9f249-121">藉由略過 proxy 伺服器，應用程式可能可以更快地連接到內部網路上的媒體伺服器。</span><span class="sxs-lookup"><span data-stu-id="9f249-121">By bypassing the proxy server, the application might be able to connect to media servers on the intranet faster.</span></span>

         

    -   <span data-ttu-id="9f249-122">不需要 proxy 伺服器來建立連線的媒體伺服器地址清單： [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="9f249-122">List of media server addresses that do not require a proxy server to establish a connection: [**MFNETSOURCE\_PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) property.</span></span> <span data-ttu-id="9f249-123">這個設定是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="9f249-123">This setting is optional.</span></span>

-   <span data-ttu-id="9f249-124">自動偵測模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-124">Auto-Detect Mode.</span></span> <span data-ttu-id="9f249-125">應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ AUTO** 來設定此模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-125">The application sets this mode by setting the [**MFNETSOURCE\_PROXYSETTING**](mfnetsource-proxysettings-property.md) property to **MFNET\_PROXYSETTING\_AUTO**.</span></span> <span data-ttu-id="9f249-126">在此模式中，proxy 定位器會使用 WinHTTP 自動代理程式機制來取得 proxy 伺服器的主機名稱和埠號碼。</span><span class="sxs-lookup"><span data-stu-id="9f249-126">In this mode, the proxy locator uses the WinHTTP AutoProxy mechanism to get the hostname and the port number for the proxy server.</span></span> <span data-ttu-id="9f249-127">您可以使用 WPAD auto proxy 腳本（由網域系統管理員設定）來抓取此連接資訊。</span><span class="sxs-lookup"><span data-stu-id="9f249-127">This connection information is retrieved by using the WPAD auto proxy script, which is configured by the domain administrator.</span></span> <span data-ttu-id="9f249-128">如需此機制的詳細資訊，請參閱 [Microsoft 網站](../winhttp/winhttp-autoproxy-support.md)。</span><span class="sxs-lookup"><span data-stu-id="9f249-128">For more information about this mechanism, see the [Microsoft website](../winhttp/winhttp-autoproxy-support.md).</span></span>

    <span data-ttu-id="9f249-129">Proxy 定位器會在登錄中快取連接資訊。</span><span class="sxs-lookup"><span data-stu-id="9f249-129">The proxy locator caches the connection information in the registry.</span></span> <span data-ttu-id="9f249-130">在後續的 proxy 偵測呼叫中，proxy 定位器會從登錄快取讀取 proxy 資訊，以降低自動偵測所需的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="9f249-130">In subsequent proxy detection calls, the proxy locator reads proxy information from the registry cache to reduce the overhead involved in auto detection.</span></span> <span data-ttu-id="9f249-131">不過，應用程式可以藉由設定 [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) 屬性來強制執行自動 proxy redetection。</span><span class="sxs-lookup"><span data-stu-id="9f249-131">However, the application can force auto proxy redetection by setting the [**MFNETSOURCE\_PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) property.</span></span>

-   <span data-ttu-id="9f249-132">瀏覽器模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-132">Browser Mode.</span></span> <span data-ttu-id="9f249-133">應用程式會藉由將 [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) 屬性設定為 **MFNET \_ PROXYSETTING \_ BROWSER** 來設定此模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-133">The application sets this mode by setting the [**MFNETSOURCE\_PROXYSETTING**](mfnetsource-proxysettings-property.md) property to **MFNET\_PROXYSETTING\_BROWSER**.</span></span> <span data-ttu-id="9f249-134">在此模式中，proxy 定位器會使用瀏覽器應用程式的 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="9f249-134">In this mode, the proxy locator uses the proxy settings of the browser application.</span></span> <span data-ttu-id="9f249-135">如果通訊協定是 HTTP 或 HTTPD，預設會設定此模式。</span><span class="sxs-lookup"><span data-stu-id="9f249-135">This mode is set by default if the protocol is HTTP or HTTPD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f249-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f249-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f249-137">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="9f249-137">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
