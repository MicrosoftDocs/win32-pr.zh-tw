---
title: 關於 Windows Web 服務
description: Windows Web 服務 API 是多層式 API，如下所示。
ms.assetid: 6e8c23d1-c86b-432d-8e0c-e16982849239
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7546aaa72d58e43d7faefccf394a3e27756f4a96
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558046"
---
# <a name="about-windows-web-services"></a><span data-ttu-id="ea9a5-103">關於 Windows Web 服務</span><span class="sxs-lookup"><span data-stu-id="ea9a5-103">About Windows Web Services</span></span>

<span data-ttu-id="ea9a5-104">Windows Web 服務 API 是多層式 API，如下所示：</span><span class="sxs-lookup"><span data-stu-id="ea9a5-104">The Windows Web Services API is a layered API and it may be pictured as follows</span></span>

![此圖顯示 Windows Web 服務 API 的圖層和跨層區域。](images/apistack.png)

<span data-ttu-id="ea9a5-106">WWSAPI 是多層式 API。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-106">The WWSAPI is a layered API.</span></span> <span data-ttu-id="ea9a5-107">我們預期大部分的開發人員都是以以方法為基礎的程式設計模型為目標的服務模型。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-107">We expect most developers to target the Service Model, which is a method-based programming model.</span></span> <span data-ttu-id="ea9a5-108">在服務模型中，服務主機會提供伺服器端程式設計模型，而服務 Proxy 則提供用戶端程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-108">In the Service Model, the Service Host provides the server side programming model, while Service Proxy provides the client side programming model.</span></span>

<span data-ttu-id="ea9a5-109">每一層都會公開一組 Api 和類型，可搭配該層的 Api 使用。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-109">Every layer exposes a set of APIs and types that can be used with APIs of that layer.</span></span>

## <a name="service-model"></a><span data-ttu-id="ea9a5-110">服務模型</span><span class="sxs-lookup"><span data-stu-id="ea9a5-110">Service Model</span></span>

<span data-ttu-id="ea9a5-111">稱為「 [服務模型](service-model-layer-overview.md) 」的最上層層提供以方法為基礎的程式設計模型，而且是最容易使用的模型。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-111">The top level layer called the [Service Model](service-model-layer-overview.md) provides a method-based programming model and it is the easiest model to use.</span></span> <span data-ttu-id="ea9a5-112">在服務模型中， [服務主機](service-host.md) 會提供伺服器端程式設計模型，而 [服務 Proxy](service-proxy.md) 則提供用戶端程式設計模型。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-112">In the Service Model, the [Service Host](service-host.md) provides the server side programming model, while the [Service Proxy](service-proxy.md) provides the client side programming model.</span></span> <span data-ttu-id="ea9a5-113">[內容](context.md) 會在服務模型內用來將相關的可用狀態傳遞給服務作業，並在叫用時傳遞（或）回呼。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-113">[Context](context.md) is used within the Service Model to pass in a relevant state available to the service operation and/or the callback when it is invoked.</span></span> <span data-ttu-id="ea9a5-114">和 [服務合約](contract.md) 用來指定服務上公開之端點的服務合約。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-114">And [Service Contract](contract.md) is used to specify a service contract on an endpoint exposed on the service.</span></span> <span data-ttu-id="ea9a5-115">下列元件和作業是服務層的一部分：</span><span class="sxs-lookup"><span data-stu-id="ea9a5-115">The following components and operations are part of the Service Layer:</span></span>

-   [<span data-ttu-id="ea9a5-116">服務主機</span><span class="sxs-lookup"><span data-stu-id="ea9a5-116">Service Host</span></span>](service-host.md)
-   [<span data-ttu-id="ea9a5-117">服務 Proxy</span><span class="sxs-lookup"><span data-stu-id="ea9a5-117">Service Proxy</span></span>](service-proxy.md)
-   [<span data-ttu-id="ea9a5-118">內容</span><span class="sxs-lookup"><span data-stu-id="ea9a5-118">Context</span></span>](context.md)
-   [<span data-ttu-id="ea9a5-119">合約</span><span class="sxs-lookup"><span data-stu-id="ea9a5-119">Contract</span></span>](contract.md)
-   [<span data-ttu-id="ea9a5-120">服務中繼資料</span><span class="sxs-lookup"><span data-stu-id="ea9a5-120">Service Metadata</span></span>](service-metadata.md)

## <a name="channel-layer"></a><span data-ttu-id="ea9a5-121">通道層</span><span class="sxs-lookup"><span data-stu-id="ea9a5-121">Channel Layer</span></span>

<span data-ttu-id="ea9a5-122">服務模型建基於通道層，可提供完整的彈性，但更難使用。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-122">The Service Model is built upon a Channel Layer, which provides full flexibility but is more difficult to use.</span></span> <span data-ttu-id="ea9a5-123">下列元件和作業是通道層的一部分：</span><span class="sxs-lookup"><span data-stu-id="ea9a5-123">The following components and operations are part of the Channel Layer:</span></span>

-   [<span data-ttu-id="ea9a5-124">訊息</span><span class="sxs-lookup"><span data-stu-id="ea9a5-124">Message</span></span>](message.md)
-   [<span data-ttu-id="ea9a5-125">通道</span><span class="sxs-lookup"><span data-stu-id="ea9a5-125">Channel</span></span>](channel.md)
-   [<span data-ttu-id="ea9a5-126">接聽程式</span><span class="sxs-lookup"><span data-stu-id="ea9a5-126">Listener</span></span>](listener.md)
-   [<span data-ttu-id="ea9a5-127">錯誤</span><span class="sxs-lookup"><span data-stu-id="ea9a5-127">Faults</span></span>](faults.md)
-   [<span data-ttu-id="ea9a5-128">Url</span><span class="sxs-lookup"><span data-stu-id="ea9a5-128">Url</span></span>](url.md)
-   [<span data-ttu-id="ea9a5-129">安全性</span><span class="sxs-lookup"><span data-stu-id="ea9a5-129">Security</span></span>](security-overview.md)
-   [<span data-ttu-id="ea9a5-130">中繼資料匯入</span><span class="sxs-lookup"><span data-stu-id="ea9a5-130">Metadata Import</span></span>](metadata-import.md)

## <a name="xml-layer"></a><span data-ttu-id="ea9a5-131">XML 層</span><span class="sxs-lookup"><span data-stu-id="ea9a5-131">XML Layer</span></span>

<span data-ttu-id="ea9a5-132">通道層級接著建基於輕量的 XML 架構，包括 C 資料類型的還原序列化。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-132">The Channel Layer is in turn built upon a lightweight XML framework, which includes deserialization of C data types.</span></span> <span data-ttu-id="ea9a5-133">下列元件和作業是 XML 層的一部分：</span><span class="sxs-lookup"><span data-stu-id="ea9a5-133">The following components and operations are part of the XML Layer:</span></span>

-   [<span data-ttu-id="ea9a5-134">XML 寫入器</span><span class="sxs-lookup"><span data-stu-id="ea9a5-134">XML Writer</span></span>](xml-writer.md)
-   [<span data-ttu-id="ea9a5-135">XML 讀取器</span><span class="sxs-lookup"><span data-stu-id="ea9a5-135">XML Reader</span></span>](xml-reader.md)
-   [<span data-ttu-id="ea9a5-136">XML 緩衝區</span><span class="sxs-lookup"><span data-stu-id="ea9a5-136">XML Buffer</span></span>](xml-buffer.md)
-   [<span data-ttu-id="ea9a5-137">序列 化</span><span class="sxs-lookup"><span data-stu-id="ea9a5-137">Serialization</span></span>](serialization.md)
-   [<span data-ttu-id="ea9a5-138">XML 語言支援</span><span class="sxs-lookup"><span data-stu-id="ea9a5-138">XML Language Support</span></span>](xml-language-support.md)

## <a name="common-to-all-layers"></a><span data-ttu-id="ea9a5-139">所有層級通用</span><span class="sxs-lookup"><span data-stu-id="ea9a5-139">Common to all layers</span></span>

<span data-ttu-id="ea9a5-140">以下是適用于三個階層中任一層的主題：</span><span class="sxs-lookup"><span data-stu-id="ea9a5-140">The following are topics that apply to any of the three layers:</span></span>

-   [<span data-ttu-id="ea9a5-141">錯誤</span><span class="sxs-lookup"><span data-stu-id="ea9a5-141">Errors</span></span>](errors.md)
-   [<span data-ttu-id="ea9a5-142">非同步模型</span><span class="sxs-lookup"><span data-stu-id="ea9a5-142">Asynchronous Model</span></span>](asynchronous-model.md)
-   [<span data-ttu-id="ea9a5-143">執行緒安全性</span><span class="sxs-lookup"><span data-stu-id="ea9a5-143">Thread Safety</span></span>](thread-safety.md)
-   [<span data-ttu-id="ea9a5-144">追蹤</span><span class="sxs-lookup"><span data-stu-id="ea9a5-144">Tracing</span></span>](tracing.md)
-   [<span data-ttu-id="ea9a5-145">取消</span><span class="sxs-lookup"><span data-stu-id="ea9a5-145">Cancellation</span></span>](cancellation.md)
-   [<span data-ttu-id="ea9a5-146">公用程式</span><span class="sxs-lookup"><span data-stu-id="ea9a5-146">Utilities</span></span>](utilities.md)
-   [<span data-ttu-id="ea9a5-147">偵錯</span><span class="sxs-lookup"><span data-stu-id="ea9a5-147">Debugging</span></span>](debugging.md)
-   [<span data-ttu-id="ea9a5-148">Wsutil 編譯器工具</span><span class="sxs-lookup"><span data-stu-id="ea9a5-148">Wsutil Compiler tool</span></span>](wsutil-compiler-tool.md)
-   [<span data-ttu-id="ea9a5-149">堆積</span><span class="sxs-lookup"><span data-stu-id="ea9a5-149">Heap</span></span>](heap.md)

## <a name="examples"></a><span data-ttu-id="ea9a5-150">範例</span><span class="sxs-lookup"><span data-stu-id="ea9a5-150">Examples</span></span>

<span data-ttu-id="ea9a5-151">如需 API 元素的詳細資訊，請參閱 [Windows Web 服務參考](windows-web-services-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-151">For more information about API elements, see [Windows Web Services Reference](windows-web-services-reference.md).</span></span> <span data-ttu-id="ea9a5-152">如需使用 API 的範例，請參閱 [使用 Windows Web 服務](using-windows-web-services.md)。</span><span class="sxs-lookup"><span data-stu-id="ea9a5-152">For examples of using the API, see [Using Windows Web Services](using-windows-web-services.md).</span></span>

 

 




