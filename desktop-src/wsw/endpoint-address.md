---
title: 端點位址
description: 端點位址代表網路上的服務位址。
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- 適用于 Windows 的端點位址 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104568240"
---
# <a name="endpoint-address"></a><span data-ttu-id="994b8-106">端點位址</span><span class="sxs-lookup"><span data-stu-id="994b8-106">Endpoint Address</span></span>

<span data-ttu-id="994b8-107">端點位址代表網路上的服務位址。</span><span class="sxs-lookup"><span data-stu-id="994b8-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="994b8-108">當您開啟 [通道](channel.md)時，藉由呼叫 [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) 函式，您必須提供要與其通訊之服務的端點位址，以及指定您要開啟的通道。</span><span class="sxs-lookup"><span data-stu-id="994b8-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="994b8-109">端點位址是由下列各項所組成：</span><span class="sxs-lookup"><span data-stu-id="994b8-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="994b8-110">[URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="994b8-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="994b8-111">一組標頭 (選用) </span><span class="sxs-lookup"><span data-stu-id="994b8-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="994b8-112"> (選擇性的一組延伸模組) </span><span class="sxs-lookup"><span data-stu-id="994b8-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="994b8-113">選用的 [識別](endpoint-identity.md) ，代表服務的安全性識別。</span><span class="sxs-lookup"><span data-stu-id="994b8-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="994b8-114">解決訊息時，URL 會變成訊息的「到」標頭。</span><span class="sxs-lookup"><span data-stu-id="994b8-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="994b8-115">任何屬於端點位址的標頭也會新增至訊息。</span><span class="sxs-lookup"><span data-stu-id="994b8-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![顯示將端點位址標頭新增至訊息的圖表。](images/endpointaddress.png)

<span data-ttu-id="994b8-117">通道會使用傳遞給 [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel)的 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)結構，自動處理任何傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="994b8-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="994b8-118">您也可以使用 [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) 函數來覆寫此預設行為。</span><span class="sxs-lookup"><span data-stu-id="994b8-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="994b8-119">當 [**ws \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) 做為參數傳遞時， [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) 和 [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) 函式會在記憶體中建立 **ws \_ 端點 \_ 位址** 參數的複本，而且其大小受限於65536個位元組。</span><span class="sxs-lookup"><span data-stu-id="994b8-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="994b8-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) 沒有這項限制，因為它不需要建立 **WS \_ 端點 \_ 位址** 參數的複本。</span><span class="sxs-lookup"><span data-stu-id="994b8-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="994b8-121">在 [**WS \_ 端點 \_ 位址**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)的 **延伸** 欄位中指定的延伸模組不會用來定址訊息，而是可以用來提供額外 (資訊的擴充性機制，例如，有關服務的中繼資料) 。</span><span class="sxs-lookup"><span data-stu-id="994b8-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="994b8-122">您可以使用 [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) 函式來讀取一般擴充功能。</span><span class="sxs-lookup"><span data-stu-id="994b8-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="994b8-123">例如，端點位址的選擇性識別欄位可以包含服務執行所在之電腦的 DNS 名稱，或執行服務之 Windows 帳戶的 UPN 等。</span><span class="sxs-lookup"><span data-stu-id="994b8-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="994b8-124">識別欄位不會用來定址訊息，但可以用來取得服務的安全性權杖 (例如，將 Kerberos 票證提供給目標 UPN) ，以及驗證服務的身分識別 (例如，用於在 SSL) 期間傳回的服務憑證上進行名稱檢查的 DNS 身分識別。</span><span class="sxs-lookup"><span data-stu-id="994b8-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="994b8-125">您可以使用 [序列化](serialization.md)和 [**Ws \_ 類型**](/windows/desktop/api/WebServices/ne-webservices-ws_type)的 **ws \_ 端點 \_ 位址 \_ 類型** 列舉值，來讀取和寫入端點位址。</span><span class="sxs-lookup"><span data-stu-id="994b8-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="994b8-126">請注意，若要序列化端點位址，您必須知道定址標頭所使用的規格版本（如同 [**Ws-addressing \_ \_ 版本**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) 列舉中所指定）。</span><span class="sxs-lookup"><span data-stu-id="994b8-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




