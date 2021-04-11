---
description: 本主題說明 WSDAPI 中的多宿主裝置支援，並提供用戶端和裝置開發人員的執行建議。
ms.assetid: d30ed536-d477-4f50-8c80-aacc35f948b9
title: 執行多宿主 WSD 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3537b96a577db47419d55cb5c6f732f8f7906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194904"
---
# <a name="implementing-a-multi-homed-wsd-device"></a><span data-ttu-id="043bd-103">執行多宿主 WSD 裝置</span><span class="sxs-lookup"><span data-stu-id="043bd-103">Implementing a Multi-Homed WSD Device</span></span>

<span data-ttu-id="043bd-104">Web 服務 (DPWS) 的[WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)和[裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/)不會描述多宿主裝置的執行。</span><span class="sxs-lookup"><span data-stu-id="043bd-104">[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) and the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) do not describe the implementation of multi-homed devices.</span></span> <span data-ttu-id="043bd-105">本主題說明 WSDAPI 中的多宿主裝置支援，並提供用戶端和裝置開發人員的執行建議。</span><span class="sxs-lookup"><span data-stu-id="043bd-105">This topic describes multi-homed device support in WSDAPI, and provides implementation recommendations to client and device developers.</span></span> <span data-ttu-id="043bd-106">在本主題中，會假設探索訊息是透過 IPv4 和 IPv6 (傳送，如果可用) 具有相同的訊息識別碼和應用程式排序資訊。</span><span class="sxs-lookup"><span data-stu-id="043bd-106">In this topic, it is assumed that discovery messages are sent over both IPv4 and IPv6 (if available) with the same message ID and application sequencing information.</span></span>

## <a name="discovery-in-a-multi-homed-environment"></a><span data-ttu-id="043bd-107">多重主目錄環境中的探索</span><span class="sxs-lookup"><span data-stu-id="043bd-107">Discovery in a multi-homed environment</span></span>

<span data-ttu-id="043bd-108">As mentioned in [Hello](hello-message.md) and [XAddrs](xaddr-validation-rules.md) section of [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md), WSDAPI never provides XAddrs in a Hello message.</span><span class="sxs-lookup"><span data-stu-id="043bd-108">As mentioned in [Hello](hello-message.md) and [XAddrs](xaddr-validation-rules.md) section of [Additional WS-Discovery Functionality](additional-ws-discovery-functionality.md), WSDAPI never provides XAddrs in a Hello message.</span></span> <span data-ttu-id="043bd-109">也就是說，您可以在所有網路介面上，使用相同的訊息識別碼和應用程式排序資訊來傳送相同的 Hello 訊息。</span><span class="sxs-lookup"><span data-stu-id="043bd-109">That means the same Hello message can be sent on all network interfaces with the same message ID and application sequencing information.</span></span> <span data-ttu-id="043bd-110">這可讓用戶端與裝置共用一個以上的子網時，讓用戶端衝突偵測更容易從相同的裝置捨棄多個 Hello 訊息。</span><span class="sxs-lookup"><span data-stu-id="043bd-110">This makes it easier for client collision detection to discard multiple Hello messages from the same device when a client and the device share more than one subnet.</span></span>

<span data-ttu-id="043bd-111">由於 [XAddrs](xaddr-validation-rules.md) 不會在 [Hello](hello-message.md) 訊息中傳送，因此用戶端必須傳送 [解析](resolve-message.md) 訊息以取得相關的裝置位址。</span><span class="sxs-lookup"><span data-stu-id="043bd-111">Because the [XAddrs](xaddr-validation-rules.md) are not sent in the [Hello](hello-message.md) message, client implementations must send a [Resolve](resolve-message.md) message to get the relevant device address.</span></span> <span data-ttu-id="043bd-112">解析應該在具有相同訊息識別碼的所有用戶端介面上傳送，且裝置應該視需要篩選重複的訊息。</span><span class="sxs-lookup"><span data-stu-id="043bd-112">The Resolve should be sent on all client interfaces with the same message ID, and the device should filter duplicate messages as needed.</span></span> <span data-ttu-id="043bd-113">針對解析訊息使用相同的訊息識別碼，可讓裝置挑選慣用的介面，以便在必要時與用戶端進行通訊。</span><span class="sxs-lookup"><span data-stu-id="043bd-113">Using the same message ID for the Resolve message allows the device to pick a preferred interface for communicating with clients if necessary.</span></span>

<span data-ttu-id="043bd-114">傳送 [ResolveMatch](resolvematches-message.md) 訊息時，裝置應該提供與網路介面相關的 [XAddrs](xaddr-validation-rules.md) ，而該網路介面的訊息是透過這個介面來單播。</span><span class="sxs-lookup"><span data-stu-id="043bd-114">When sending a [ResolveMatch](resolvematches-message.md) message, a device should provide [XAddrs](xaddr-validation-rules.md) that relate to the network interface over which it is unicasting the message.</span></span> <span data-ttu-id="043bd-115">這種作法有助於避免多次用戶端連接嘗試和複雜的重試邏輯。</span><span class="sxs-lookup"><span data-stu-id="043bd-115">This practice helps to avoid multiple client connection attempts and complicated retry logic.</span></span>

## <a name="metadata-exchange-in-a-multi-homed-environment"></a><span data-ttu-id="043bd-116">多主控環境中的中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="043bd-116">Metadata exchange in a multi-homed environment</span></span>

<span data-ttu-id="043bd-117">在多重主目錄環境中執行中繼資料交換比執行探索更難，因為中繼資料版本設定。</span><span class="sxs-lookup"><span data-stu-id="043bd-117">Implementing metadata exchange in a multi-homed environment is more difficult than implementing discovery because of metadata versioning.</span></span> <span data-ttu-id="043bd-118">如果用戶端透過多個介面要求中繼資料，則用戶端可以透過不同的介面接收多個 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="043bd-118">If a client requests metadata over multiple interfaces, then the client can receive multiple [GetResponse](getresponse--metadata-exchange--message.md) messages over different interfaces.</span></span> <span data-ttu-id="043bd-119">這些 GetResponse 訊息可以包含具有相同中繼資料版本的不同 **關聯** 性中繼資料區段。</span><span class="sxs-lookup"><span data-stu-id="043bd-119">These GetResponse messages can contain different **Relationship** metadata sections with the same metadata version.</span></span> <span data-ttu-id="043bd-120">這會減少中繼資料版本號碼的值。</span><span class="sxs-lookup"><span data-stu-id="043bd-120">This reduces the value of the metadata version number.</span></span>

<span data-ttu-id="043bd-121">有一個替代方法，其中會傳送單一 [GetResponse](getresponse--metadata-exchange--message.md) 訊息以回應服務的所有位址。</span><span class="sxs-lookup"><span data-stu-id="043bd-121">There is an alternative approach, where a single [GetResponse](getresponse--metadata-exchange--message.md) message is sent in response with all addresses for the service.</span></span> <span data-ttu-id="043bd-122">這種方法的缺點是可能會洩漏私用資訊，例如可間接存取網路的拓撲。</span><span class="sxs-lookup"><span data-stu-id="043bd-122">The disadvantage of this method is that private information, such as the topology of indirectly accessible networks, may be disclosed.</span></span>

<span data-ttu-id="043bd-123">在 Windows Vista 中，WSDAPI 提供的中繼資料只包含對接收到中繼資料要求的介面有效的位址。</span><span class="sxs-lookup"><span data-stu-id="043bd-123">On Windows Vista, the metadata provided by WSDAPI contains only addresses that are valid for the interface upon which the metadata request was received.</span></span>

 

 



