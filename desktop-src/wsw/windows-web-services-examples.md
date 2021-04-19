---
title: Windows Web 服務範例
description: 下列範例示範如何使用 Windows Web 服務 API。
ms.assetid: 8a557ef0-a88a-4257-a181-57f2dca9022f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e74aec03c4822fb9ba270076b5127dd37d145fb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966786"
---
# <a name="windows-web-services-examples"></a><span data-ttu-id="46e1d-103">Windows Web 服務範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-103">Windows Web Services Examples</span></span>

<span data-ttu-id="46e1d-104">下列範例示範如何使用 Windows Web 服務 API。</span><span class="sxs-lookup"><span data-stu-id="46e1d-104">The following examples show how to use Windows Web Services API.</span></span>

-   [<span data-ttu-id="46e1d-105">服務模型範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-105">Service Model Examples</span></span>](service-model-examples.md)
-   [<span data-ttu-id="46e1d-106">TCP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-106">TCP Channel Layer Examples</span></span>](tcp-channel-layer-examples.md)
-   [<span data-ttu-id="46e1d-107">HTTP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-107">HTTP Channel Layer Examples</span></span>](http-channel-layer-examples.md)
-   [<span data-ttu-id="46e1d-108">UDP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-108">UDP Channel Layer Examples</span></span>](udp-channel-layer-examples.md)
-   [<span data-ttu-id="46e1d-109">具名管道通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-109">Named Pipe Channel Layer Examples</span></span>](named-pipes-channel-layer-examples.md)
-   [<span data-ttu-id="46e1d-110">訊息範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-110">Message Examples</span></span>](message-examples.md)
-   [<span data-ttu-id="46e1d-111">XML 範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-111">XML Examples</span></span>](xml-examples.md)
-   [<span data-ttu-id="46e1d-112">非同步模型範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-112">Async Model Examples</span></span>](async-model-examples.md)
-   [<span data-ttu-id="46e1d-113">安全性通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-113">Security Channel Layer Examples</span></span>](security-channel-layer-examples.md)
-   [<span data-ttu-id="46e1d-114">檔案複寫範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-114">File Replication Examples</span></span>](file-replication-examples.md)

## <a name="service-model-examples"></a><span data-ttu-id="46e1d-115">服務模型範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-115">Service Model Examples</span></span>

<span data-ttu-id="46e1d-116">計算機服務：用戶端： [HttpCalculatorClientExample](httpcalculatorclientexample.md)，伺服器： [HttpCalculatorServiceExample](httpcalculatorserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-116">Calculator Service: Client: [HttpCalculatorClientExample](httpcalculatorclientexample.md), Server: [HttpCalculatorServiceExample](httpcalculatorserviceexample.md).</span></span>

<span data-ttu-id="46e1d-117">具有 SSL 傳輸安全性的計算機服務：用戶端： [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md)、伺服器： [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-117">Calculator Service with SSL transport security: Client: [HttpCalculatorWithSslClientExample](httpcalculatorwithsslclientexample.md), Server: [HttpCalculatorWithSslServiceExample](httpcalculatorwithsslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-118">具有使用者名稱（SSL 混合模式安全性）的計算機服務：用戶端： [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md)，伺服器： [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-118">Calculator Service with Username over SSL mixed-mode security: Client: [HttpCalculatorWithUsernameOverSslClientExample](httpcalculatorwithusernameoversslclientexample.md), Server: [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-119">具有 Kerberos over SSL 混合模式安全性的計算機服務：用戶端： [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md)、伺服器： [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-119">Calculator Service with Kerberos over SSL mixed-mode security: Client: [HttpCalculatorWithKerberosOverSslClientExample](httpcalculatorwithkerberosoversslclientexample.md), Server: [HttpCalculatorWithKerberosOverSslServiceExample](httpcalculatorwithkerberosoversslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-120">採購單服務：用戶端： [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md)，伺服器： [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-120">Purchase Order Service: Client: [HttpPurchaseOrderClientExample](httppurchaseorderclientexample.md), Server: [HttpPurchaseOrderServiceExample](httppurchaseorderserviceexample.md).</span></span>

<span data-ttu-id="46e1d-121">具有 SSL 傳輸安全性的採購訂單服務：用戶端： [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md)、伺服器： [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-121">Purchase Order Service with SSL transport security: Client: [HttpPurchaseOrderWithSslClientExample](httppurchaseorderwithsslclientexample.md), Server: [HttpPurchaseOrderWithSslServiceExample](httppurchaseorderwithsslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-122">具有透過 SSL 混合模式安全性之使用者名稱的訂單服務：用戶端： [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md)、伺服器： [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-122">Purchase Order Service with Username over SSL mixed-mode security: Client: [HttpPurchaseOrderWithUsernameOverSslClientExample](httppurchaseorderwithusernameoversslclientexample.md), Server: [HttpPurchaseOrderWithUserNameOverSslServiceExample](httppurchaseorderwithusernameoversslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-123">具有 Kerberos over SSL 混合模式安全性的訂單服務：用戶端： [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md)、伺服器： [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-123">Purchase Order Service with Kerberos over SSL mixed-mode security: Client: [HttpPurchaseOrderWithKerberosOverSslClientExample](httppurchaseorderwithkerberosoversslclientexample.md), Server: [HttpPurchaseOrderWithKerberosOverSslServiceExample](httppurchaseorderwithkerberosoversslserviceexample.md).</span></span>

<span data-ttu-id="46e1d-124">不具類型的訂單服務：伺服器： [UnTypedServiceExample](untypedserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-124">UnTyped Purchase Order Service: Server: [UnTypedServiceExample](untypedserviceexample.md).</span></span> <span data-ttu-id="46e1d-125">用戶端： [UnTypedClientExample](untypedclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-125">Client: [UnTypedClientExample](untypedclientexample.md)</span></span>

<span data-ttu-id="46e1d-126">會話計算機： Server： [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-126">Sessionful Calculator: Server: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span> <span data-ttu-id="46e1d-127">用戶端：[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-127">Client:[SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md).</span></span>

<span data-ttu-id="46e1d-128">使用自訂通道和接聽程式執行的計算機：伺服器：[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-128">Calculator using a custom channel and listener implementation: Server:[HttpCalculatorWithLayeredChannelServiceExample](httpcalculatorwithlayeredchannelserviceexample.md).</span></span> <span data-ttu-id="46e1d-129">用戶端：[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-129">Client:[HttpCalculatorWithLayeredChannelClientExample](httpcalculatorwithlayeredchannelclientexample.md).</span></span>

<span data-ttu-id="46e1d-130">使用編碼通道的計算機：伺服器：[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-130">Calculator using a encoded channel: Server:[HttpCalculatorWithEncodedChannelServiceExample](httpcalculatorwithencodedchannelserviceexample.md).</span></span> <span data-ttu-id="46e1d-131">用戶端：[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-131">Client:[HttpCalculatorWithEncodedChannelClientExample](httpcalculatorwithencodedchannelclientexample.md).</span></span>

<span data-ttu-id="46e1d-132">處理原始 (非 SOAP) HTTP 要求的服務：用戶端：[HttpRawClientExample](httprawclientexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-132">Service that handles raw (non-SOAP) HTTP requests: Client:[HttpRawClientExample](httprawclientexample.md).</span></span> <span data-ttu-id="46e1d-133">伺服器：[HttpRawServiceExample](httprawserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-133">Server:[HttpRawServiceExample](httprawserviceexample.md).</span></span>

<span data-ttu-id="46e1d-134">服務操作中止通知：伺服器： [BlockingServiceExample](blockingserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-134">Service Operation Abort Notification: Server: [BlockingServiceExample](blockingserviceexample.md).</span></span> <span data-ttu-id="46e1d-135">用戶端：[ServiceCancellationExample](servicecancellationexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-135">Client:[ServiceCancellationExample](servicecancellationexample.md).</span></span>

<span data-ttu-id="46e1d-136">呼叫取消：伺服器： [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-136">Call Cancellation: Server: [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span> <span data-ttu-id="46e1d-137">用戶端：[CallAbandonExample](callabandonexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-137">Client:[CallAbandonExample](callabandonexample.md).</span></span>

<span data-ttu-id="46e1d-138">手動建立原則描述，並用它來建立服務 proxy： [PolicyTemplateExample](policytemplateexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-138">Manually create a policy description and use it to create a service proxy: [PolicyTemplateExample](policytemplateexample.md).</span></span>

## <a name="tcp-channel-layer-examples"></a><span data-ttu-id="46e1d-139">TCP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-139">TCP Channel Layer Examples</span></span>

<span data-ttu-id="46e1d-140">使用單向模式傳送訊息的 TCP 範例：用戶端： [OneWayTcpClientExample](onewaytcpclientexample.md)、伺服器： [OneWayTcpServerExample](onewaytcpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-140">A TCP example that sends messages using a one-way pattern: Client: [OneWayTcpClientExample](onewaytcpclientexample.md), Server: [OneWayTcpServerExample](onewaytcpserverexample.md)</span></span>

<span data-ttu-id="46e1d-141">使用要求-回復模式傳送訊息的 TCP 範例：用戶端： [RequestReplyTcpClientExample](requestreplytcpclientexample.md)，伺服器： [RequestReplyTcpServerExample](requestreplytcpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-141">A TCP example that sends messages using a request-reply pattern: Client: [RequestReplyTcpClientExample](requestreplytcpclientexample.md), Server: [RequestReplyTcpServerExample](requestreplytcpserverexample.md)</span></span>

<span data-ttu-id="46e1d-142">串流 TCP 範例：用戶端： [StreamingTcpClientExample](streamingtcpclientexample.md)，伺服器： [StreamingTcpServerExample](streamingtcpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-142">A streaming TCP example: Client: [StreamingTcpClientExample](streamingtcpclientexample.md), Server: [StreamingTcpServerExample](streamingtcpserverexample.md)</span></span>

<span data-ttu-id="46e1d-143">非同步資料流程 TCP 範例： Client： [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md)，Server： [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-143">An async streaming TCP example: Client: [AsyncStreamingTcpClientExample](asyncstreamingtcpclientexample.md), Server: [AsyncStreamingTcpServerExample](asyncstreamingtcpserverexample.md)</span></span>

## <a name="http-channel-layer-examples"></a><span data-ttu-id="46e1d-144">HTTP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-144">HTTP Channel Layer Examples</span></span>

<span data-ttu-id="46e1d-145">HTTP 範例： Client： [HttpClientExample](httpclientexample.md)，Server： [HttpServerExample](httpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-145">An HTTP example: Client: [HttpClientExample](httpclientexample.md), Server: [HttpServerExample](httpserverexample.md)</span></span>

<span data-ttu-id="46e1d-146">使用串流 Api 的 HTTP 範例： Client： [StreamingHttpClientExample](streaminghttpclientexample.md)，Server： [StreamingHttpServerExample](streaminghttpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-146">An HTTP example that uses the streaming APIs: Client: [StreamingHttpClientExample](streaminghttpclientexample.md), Server: [StreamingHttpServerExample](streaminghttpserverexample.md)</span></span>

## <a name="udp-channel-layer-examples"></a><span data-ttu-id="46e1d-147">UDP 通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-147">UDP Channel Layer Examples</span></span>

<span data-ttu-id="46e1d-148">使用單向模式傳送訊息的 UDP 範例：用戶端： [OneWayUdpClientExample](onewayudpclientexample.md)、伺服器： [OneWayUdpServerExample](onewayudpserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-148">A UDP example that sends messages using a one-way pattern: Client: [OneWayUdpClientExample](onewayudpclientexample.md), Server: [OneWayUdpServerExample](onewayudpserverexample.md)</span></span>

<span data-ttu-id="46e1d-149">使用多播要求回應模式傳送訊息的 UDP 範例：用戶端： [MulticastUdpClientExample](multicastudpclientexample.md)、伺服器： [MulticastUdpServerExample](multicastudpserverexample.md) 以下是相同的範例，但使用 IPv6 位址： Client： [MulticastUdpClientExample6](multicastudpclientexample6.md)，Server： [MulticastUdpServerExample6](multicastudpserverexample6.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-149">A UDP example that sends messages using a multicast request response pattern: Client: [MulticastUdpClientExample](multicastudpclientexample.md), Server: [MulticastUdpServerExample](multicastudpserverexample.md) The following is the same example, but using IPv6 addressing: Client: [MulticastUdpClientExample6](multicastudpclientexample6.md), Server: [MulticastUdpServerExample6](multicastudpserverexample6.md)</span></span>

## <a name="named-pipes-channel-layer-examples"></a><span data-ttu-id="46e1d-150">具名管道通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-150">Named Pipes Channel Layer Examples</span></span>

<span data-ttu-id="46e1d-151">使用要求-回復模式傳送訊息的具名管道範例：用戶端： [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md)，伺服器： [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-151">A named pipes example that sends messages using a request-reply pattern: Client: [RequestReplyNamedPipesClientExample](requestreplynamedpipesclientexample.md), Server: [RequestReplyNamedPipesServerExample](requestreplynamedpipesserverexample.md)</span></span>

<span data-ttu-id="46e1d-152">串流具名管道範例： Client： [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md)，Server： [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-152">A streaming named pipes example: Client: [StreamingNamedPipesClientExample](streamingnamedpipesclientexample.md), Server: [StreamingNamedPipesServerExample](streamingnamedpipesserverexample.md)</span></span>

## <a name="message-examples"></a><span data-ttu-id="46e1d-153">訊息範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-153">Message Examples</span></span>

<span data-ttu-id="46e1d-154">使用自訂訊息標頭的範例： [CustomHeaderExample](customheaderexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-154">An example that uses custom message headers: [CustomHeaderExample](customheaderexample.md)</span></span>

<span data-ttu-id="46e1d-155">編碼和解碼訊息的範例： [MessageEncodingExample](messageencodingexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-155">An example that encodes and decodes a message: [MessageEncodingExample](messageencodingexample.md)</span></span>

<span data-ttu-id="46e1d-156">轉送訊息的範例： [ForwardMessageExample](forwardmessageexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-156">An example that forwards a message: [ForwardMessageExample](forwardmessageexample.md)</span></span>

## <a name="xml-examples"></a><span data-ttu-id="46e1d-157">XML 範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-157">XML Examples</span></span>

<span data-ttu-id="46e1d-158">使用 XML 緩衝區來寫入和讀取 xml 的範例 [ReadWriteXmlExample](readwritexmlexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-158">An example that writes and reads xml using an XML buffer [ReadWriteXmlExample](readwritexmlexample.md)</span></span>

<span data-ttu-id="46e1d-159">使用 MTOM、WsWriteBytes、WsPushBytes 和 WsPullBytes 寫入和讀取二進位資料的範例 [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-159">An example that writes and reads binary data using MTOM, WsWriteBytes, WsPushBytes, and WsPullBytes [ReadWriteBytesXmlExample](readwritebytesxmlexample.md)</span></span>

<span data-ttu-id="46e1d-160">流覽 XML 緩衝區的範例 [NavigateXmlExample](navigatexmlexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-160">An example that navigates an XML buffer [NavigateXmlExample](navigatexmlexample.md)</span></span>

<span data-ttu-id="46e1d-161">依節點[ReadXmlExample](readxmlexample.md)讀取 XML 檔節點的範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-161">An example that reads an XML document node by node [ReadXmlExample](readxmlexample.md)</span></span>

<span data-ttu-id="46e1d-162">尋找並顯示 XML 屬性的範例 [ReadAttributeExample](readattributeexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-162">An example that find and displays an XML attribute [ReadAttributeExample](readattributeexample.md)</span></span>

<span data-ttu-id="46e1d-163">寫入和讀取元素陣列的範例 [ReadWriteArrayExample](readwritearrayexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-163">An example that writes and reads an array of elements [ReadWriteArrayExample](readwritearrayexample.md)</span></span>

<span data-ttu-id="46e1d-164">將元素插入至 XML 緩衝區的範例 [InsertElementExample](insertelementexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-164">An example that inserts an element into an XML buffer [InsertElementExample](insertelementexample.md)</span></span>

<span data-ttu-id="46e1d-165">示範如何使用某些 XML 緩衝區 helper 函數的範例 [XmlBufferExample](xmlbufferexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-165">An example that shows the use of some XML buffer helper functions [XmlBufferExample](xmlbufferexample.md)</span></span>

<span data-ttu-id="46e1d-166">使用 wsutil 產生的 helper 函式來寫入和讀取衍生類型的範例 [DerivedTypeExample](derivedtypeexample.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-166">An example that writes and reads derived type using wsutil generated helper functions [DerivedTypeExample](derivedtypeexample.md)</span></span>

## <a name="async-model-examples"></a><span data-ttu-id="46e1d-167">非同步模型範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-167">Async Model Examples</span></span>

<span data-ttu-id="46e1d-168">說明非同步函式之模型的範例。</span><span class="sxs-lookup"><span data-stu-id="46e1d-168">An example that illustrates the model for asynchronous functions.</span></span> [<span data-ttu-id="46e1d-169">AsyncModelExample</span><span class="sxs-lookup"><span data-stu-id="46e1d-169">AsyncModelExample</span></span>](asyncmodelexample.md)

## <a name="security-channel-layer-examples"></a><span data-ttu-id="46e1d-170">安全性通道層範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-170">Security Channel Layer Examples</span></span>

<span data-ttu-id="46e1d-171">透過 TCP 的 Windows 傳輸安全性：用戶端： [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-171">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="46e1d-172">具名管道上的 Windows 傳輸安全性：用戶端： [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md)，伺服器： [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-172">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="46e1d-173">SSL 傳輸安全性：用戶端： [HttpClientWithSslExample](httpclientwithsslexample.md)，伺服器： [HttpServerWithSslExample](httpserverwithsslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-173">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="46e1d-174">透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md)，伺服器： [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-174">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="46e1d-175">透過 SSL 混合模式安全性的使用者名稱：用戶端： [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md)，伺服器： [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-175">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

## <a name="metadata-example"></a><span data-ttu-id="46e1d-176">中繼資料範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-176">Metadata Example</span></span>

<span data-ttu-id="46e1d-177">下列範例顯示如何處理 WSDL 和原則檔，其目標是將端點所支援的通訊協定相關資訊解壓縮。</span><span class="sxs-lookup"><span data-stu-id="46e1d-177">The following examples show how to process WSDL and Policy documents with the goal of extracting information about what protocol an endpoint supports.</span></span>

<span data-ttu-id="46e1d-178">透過 SSL 混合模式安全性的使用者名稱： [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-178">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="46e1d-179">透過 SSL 混合模式安全性發出的權杖： [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-179">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="46e1d-180">透過 SSL 混合模式安全性的 X509 憑證： [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-180">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="ws-metadata-exchange-example"></a><span data-ttu-id="46e1d-181">WS-Metadata Exchange 範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-181">WS-Metadata Exchange Example</span></span>

<span data-ttu-id="46e1d-182">下列範例示範如何在 [WS \_ 服務 \_ 主機](ws-service-host.md)上啟用 WS-MetadataExchange。</span><span class="sxs-lookup"><span data-stu-id="46e1d-182">The following examples show how to enable WS-MetadataExchange on [WS\_SERVICE\_HOST](ws-service-host.md).</span></span>

<span data-ttu-id="46e1d-183">啟用 WS-MetadataExchange 的 TCP 服務： [MetadataExchangeSample](metadataexchangesample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-183">TCP service with WS-MetadataExchange enabled: [MetadataExchangeSample](metadataexchangesample.md).</span></span> <span data-ttu-id="46e1d-184">WCF 服務的標記用戶端，其會呼叫已啟用 WS-MetadataExchange 的 TCP 服務： [ServiceMonikerSample](servicemonikersample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-184">WCF service moniker client which calls into the TCP service with WS-MetadataExchange enabled: [ServiceMonikerSample](servicemonikersample.md).</span></span>

## <a name="custom-headers-and-service-model"></a><span data-ttu-id="46e1d-185">自訂標頭和服務模型</span><span class="sxs-lookup"><span data-stu-id="46e1d-185">Custom headers and Service model</span></span>

<span data-ttu-id="46e1d-186">下列範例示範如何將自訂標頭分別搭配 [ws \_ 服務 \_ PROXY](ws-service-proxy.md) 和 [ws \_ 服務 \_ 主機](ws-service-host.md) 使用。</span><span class="sxs-lookup"><span data-stu-id="46e1d-186">The following examples show how to use custom headers with [WS\_SERVICE\_PROXY](ws-service-proxy.md) and [WS\_SERVICE\_HOST](ws-service-host.md) respectively.</span></span>

<span data-ttu-id="46e1d-187">Client： [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md)，Server： [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-187">Client: [HttpCustomHeaderPurchaseOrderClientExample](httpcustomheaderpurchaseorderclientexample.md), Server: [HttpCustomHeaderPurchaseOrderServiceExample](httpcustomheaderpurchaseorderserviceexample.md).</span></span>

## <a name="file-replication-sample"></a><span data-ttu-id="46e1d-188">檔案複寫範例</span><span class="sxs-lookup"><span data-stu-id="46e1d-188">File Replication Sample</span></span>

<span data-ttu-id="46e1d-189">示範如何執行檔案複寫服務的完整範例：工具： [FileRepToolExample](filereptoolexample.md)、服務： [FileRepServiceExample](filerepserviceexample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-189">A comprehensive sample that demonstrates how to implement a file replication service: Tool: [FileRepToolExample](filereptoolexample.md), Service: [FileRepServiceExample](filerepserviceexample.md).</span></span>

## <a name="wcf-public-service-interoperation"></a><span data-ttu-id="46e1d-190">WCF 公用服務交互操作</span><span class="sxs-lookup"><span data-stu-id="46e1d-190">WCF Public Service Interoperation</span></span>

<span data-ttu-id="46e1d-191">Windows Web 服務用戶端與 WCF 服務用戶端通訊： [WcfPublicServiceSample](wcfpublicservicesample.md)。</span><span class="sxs-lookup"><span data-stu-id="46e1d-191">A Windows Web Services client communicates with a WCF service Client: [WcfPublicServiceSample](wcfpublicservicesample.md).</span></span>

## <a name="custom-http-proxy"></a><span data-ttu-id="46e1d-192">自訂 HTTP Proxy</span><span class="sxs-lookup"><span data-stu-id="46e1d-192">Custom HTTP Proxy</span></span>

<span data-ttu-id="46e1d-193">Windows Web 服務用戶端與使用自訂 proxy 用戶端的 .ASMX TerraService 服務通訊： [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)</span><span class="sxs-lookup"><span data-stu-id="46e1d-193">A Windows Web Services client communicates with a ASMX TerraService service using custom proxy Client: [AsmxTerraServiceSampleWithCustomProxy](asmxterraservicesamplewithcustomproxy.md)</span></span>

 

 




