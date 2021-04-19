---
description: 網路來源的 Proxy 支援
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: 網路來源的 Proxy 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971690"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="1cdd2-103">網路來源的 Proxy 支援</span><span class="sxs-lookup"><span data-stu-id="1cdd2-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="1cdd2-104">Proxy 伺服器是您內部網路與網際網路之間的轉送伺服器，可將要求從用戶端應用程式路由傳送至媒體伺服器，並從媒體伺服器抓取檔案。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="1cdd2-105">當用戶端應用程式嘗試存取來源 URL 時，媒體基礎隱含地建立 *proxy 定位器* 物件。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="1cdd2-106">Proxy 定位器物件會公開 [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) 介面。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="1cdd2-107">在來源解析期間，媒體基礎會檢查傳遞給來源解析程式方法的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="1cdd2-108">如果屬性存放區包含的 [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) 屬性設定為應用程式所執行的 proxy 定位器 factory 物件，則會叫用 [**IMFNetProxyLocatorFactory：： CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) 方法，以使用自訂設定來建立 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="1cdd2-109">如果未設定屬性存放區，媒體基礎會使用預設設定來建立 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="1cdd2-110">這些設定如下所示：</span><span class="sxs-lookup"><span data-stu-id="1cdd2-110">These settings are as follows:</span></span>

-   <span data-ttu-id="1cdd2-111">如果設定了 [使用者原則]，則 proxy 定位器會使用登錄中指定的設定。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="1cdd2-112">若為 HTTP，proxy 定位器會使用瀏覽器 proxy 設定。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="1cdd2-113">針對 RTSP，proxy 定位器設定為在連線至媒體伺服器時略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="1cdd2-114">應用程式可以變更此預設設定。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="1cdd2-115">下列主題包含 proxy 定位器設定的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="1cdd2-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="1cdd2-116">Proxy 定位器設定</span><span class="sxs-lookup"><span data-stu-id="1cdd2-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="1cdd2-117">如何設定 Proxy 定位器</span><span class="sxs-lookup"><span data-stu-id="1cdd2-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="1cdd2-118">媒體基礎初始化指定給 [來源解析程式](source-resolver.md)之來源 URL 的 proxy 定位器。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="1cdd2-119">Proxy 定位器會根據設定來偵測要使用的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="1cdd2-120">當 proxy 定位器嘗試設定 proxy 伺服器時，它會在登錄中記錄成功或失敗的結果。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="1cdd2-121">在下一個 proxy 偵測程式期間，會檢查此值。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="1cdd2-122">如果已知特定的 proxy 伺服器在過去造成失敗，proxy 定位器就會略過它。</span><span class="sxs-lookup"><span data-stu-id="1cdd2-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cdd2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="1cdd2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cdd2-124">屬性和屬性</span><span class="sxs-lookup"><span data-stu-id="1cdd2-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="1cdd2-125">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="1cdd2-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



