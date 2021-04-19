---
description: WS-Discovery 使用以 urn： uuid：格式為基礎的 Uri 定義邏輯定址。
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: 使用邏輯與實體位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973262"
---
# <a name="using-logical-and-physical-addresses"></a><span data-ttu-id="ce913-103">使用邏輯與實體位址</span><span class="sxs-lookup"><span data-stu-id="ce913-103">Using Logical and Physical Addresses</span></span>

<span data-ttu-id="ce913-104">[Ws-management](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 會使用以格式為基礎的 uri 來定義邏輯定址 `urn:uuid:` 。</span><span class="sxs-lookup"><span data-stu-id="ce913-104">[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) defines logical addressing using URIs based on the `urn:uuid:` format.</span></span> <span data-ttu-id="ce913-105">此定址配置的目的是要區分裝置的身分識別與目前的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ce913-105">The purpose of this addressing scheme is to differentiate the identity of the device from its current IP address.</span></span> <span data-ttu-id="ce913-106">此配置基本上提供 DNS 名稱的功能，而不需要名稱伺服器。</span><span class="sxs-lookup"><span data-stu-id="ce913-106">This scheme essentially provides the functionality of DNS names without requiring a name server.</span></span> <span data-ttu-id="ce913-107">[Web 服務 (DPWS 的裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)) 建議裝置使用此定址配置。</span><span class="sxs-lookup"><span data-stu-id="ce913-107">[Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) recommends that devices use this addressing scheme.</span></span>

<span data-ttu-id="ce913-108">DPWS 也建議服務使用實體 (也稱為傳輸) 位址。</span><span class="sxs-lookup"><span data-stu-id="ce913-108">DPWS also recommends that services use physical (also called transport) addresses.</span></span> <span data-ttu-id="ce913-109">這可讓原本不支援 WS-Discovery 定址機制的用戶端與 DPWS 服務通訊。</span><span class="sxs-lookup"><span data-stu-id="ce913-109">This enables clients that do not natively support WS-Discovery addressing mechanisms to communicate with DPWS services.</span></span> <span data-ttu-id="ce913-110">此外，每個服務都可以定義其位址，以針對在較低層管理服務分派的裝置執行，啟用傳輸層級定址。</span><span class="sxs-lookup"><span data-stu-id="ce913-110">Also, each service can define its addresses, which enables transport level addressing for device implementations that manage service dispatch at a lower layer.</span></span> <span data-ttu-id="ce913-111">最後，使用實體位址會將互通性最大化。</span><span class="sxs-lookup"><span data-stu-id="ce913-111">Finally, using physical addresses maximizes interoperability.</span></span>

<span data-ttu-id="ce913-112">實體定址的缺點是，它會增加裝置執行的複雜度，因為必須追蹤目前的 IP 或傳輸位址，而且必須據以修改裝置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ce913-112">The disadvantage of physical addressing is that it adds complexity to device implementations, as the current IP or transport address must be tracked and device metadata must be modified accordingly.</span></span> <span data-ttu-id="ce913-113">基於這個理由，DPWS 不需要服務就能使用傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="ce913-113">For this reason, DPWS does not require services to use transport addresses.</span></span>

<span data-ttu-id="ce913-114">如果使用邏輯位址，則會在某些情況下未定義執行行為。</span><span class="sxs-lookup"><span data-stu-id="ce913-114">If logical addresses are used, then there are some scenarios where the implementation behavior is undefined.</span></span> <span data-ttu-id="ce913-115">WS-Discovery 規格不會描述服務在邏輯位址中的意義。</span><span class="sxs-lookup"><span data-stu-id="ce913-115">The WS-Discovery specification does not describe what it means for a service to reside at a logical address.</span></span> <span data-ttu-id="ce913-116">由於相關聯的網路 chatter，WS-Discovery 規格的 R1001 建議您不要在託管服務上使用 WS-Discovery。</span><span class="sxs-lookup"><span data-stu-id="ce913-116">R1001 of the WS-Discovery specification recommends against using WS-Discovery on hosted services because of the associated network chatter.</span></span>

<span data-ttu-id="ce913-117">不建議服務位於邏輯位址，因為這樣會降低互通性。</span><span class="sxs-lookup"><span data-stu-id="ce913-117">It is not recommended that services reside at logical addresses as this reduces interoperability.</span></span> <span data-ttu-id="ce913-118">如果實作為絕對必須位於邏輯位址，則服務應該使用與裝置相同的邏輯位址。</span><span class="sxs-lookup"><span data-stu-id="ce913-118">If an implementation absolutely must reside at a logical address, then the service should use the same logical address as the device.</span></span> <span data-ttu-id="ce913-119">如果這對裝置上的分派模型增加了太多複雜性，則建議的解決方案是使用參考參數來區分服務。</span><span class="sxs-lookup"><span data-stu-id="ce913-119">If this adds too much complexity to the dispatch model on the device, then the recommended solution is to use reference parameters to differentiate the services.</span></span> <span data-ttu-id="ce913-120">如果 WSDAPI 使用與裝置相同的端點位址，則會正確地將訊息傳送至服務。</span><span class="sxs-lookup"><span data-stu-id="ce913-120">WSDAPI will correctly send messages to services if they use the same endpoint address as the device.</span></span>

 

 



