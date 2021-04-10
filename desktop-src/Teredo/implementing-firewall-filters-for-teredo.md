---
title: 執行 Teredo 的防火牆篩選器
description: Windows 可讓應用程式設定通訊端選項，以允許應用程式指示透過 Windows 篩選平台，接收傳送至主機防火牆的 Teredo 流量的明確意圖。
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682796"
---
# <a name="implementing-firewall-filters-for-teredo"></a><span data-ttu-id="521bd-103">執行 Teredo 的防火牆篩選器</span><span class="sxs-lookup"><span data-stu-id="521bd-103">Implementing Firewall Filters for Teredo</span></span>

<span data-ttu-id="521bd-104">Windows 可讓應用程式設定通訊端選項，以允許應用程式指示透過 Windows 篩選平台，接收傳送至主機防火牆的 Teredo 流量的明確意圖。</span><span class="sxs-lookup"><span data-stu-id="521bd-104">Windows allows applications to set a socket option that allows applications to indicate an explicit intent to receive Teredo traffic sent to the host firewall via the Windows Filtering Platform.</span></span> <span data-ttu-id="521bd-105">在 Windows 中，用來設定保護層級的通訊端選項，可讓應用程式定義其願意接收的流量類型。</span><span class="sxs-lookup"><span data-stu-id="521bd-105">In Windows, a socket option for setting a protection level is used to allow an application to define what type of traffic it is willing to receive.</span></span> <span data-ttu-id="521bd-106">更具體來說，在涉及 Teredo 流量的案例中，會指定 [IPV6 \_ 保護 \_ 等級](/windows/desktop/WinSock/ipv6-protection-level) 通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="521bd-106">More specifically, in scenarios involving Teredo traffic, the [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option is specified.</span></span> <span data-ttu-id="521bd-107">建議主機防火牆執行維護下列篩選器，以選擇性地允許應用程式的 Teredo 流量，同時封鎖沒有豁免的任何應用程式的流量。</span><span class="sxs-lookup"><span data-stu-id="521bd-107">It is recommended that host firewall implementations maintain the following filters to selectively allow Teredo traffic for an application, while blocking traffic by default for any application without an exemption.</span></span>

## <a name="default-block-filter-for-edge-traversed-traffic"></a><span data-ttu-id="521bd-108">Edge 已通過流量的預設區塊篩選</span><span class="sxs-lookup"><span data-stu-id="521bd-108">Default Block Filter for Edge Traversed Traffic</span></span>

<span data-ttu-id="521bd-109">如果 \_ \_ \_ \_ 流量符合指定的 **介面類別型** 通道和通道 **類型 Teredo** 條件，主機防火牆一律必須在 ALE 驗證接收接受 V6 篩選層內維護預設的區塊篩選。</span><span class="sxs-lookup"><span data-stu-id="521bd-109">A host firewall must always maintain a default block filter within the ALE\_AUTH\_RECV\_ACCEPT\_V6 filtering layer for traffic matching the specified **Interface Type Tunnel** and **Tunnel Type Teredo** conditions.</span></span> <span data-ttu-id="521bd-110">執行時，此篩選準則會指出系統中有 edge 遍歷感知主機防火牆。</span><span class="sxs-lookup"><span data-stu-id="521bd-110">When implemented, this filter indicates the presence of an edge traversal aware host firewall in the system.</span></span> <span data-ttu-id="521bd-111">此篩選器會視為主機防火牆和 Windows 之間的 API 合約。</span><span class="sxs-lookup"><span data-stu-id="521bd-111">This filter is viewed as an API contract between the host firewall and Windows.</span></span> <span data-ttu-id="521bd-112">根據預設，此篩選準則會封鎖 edge 將流量流向任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="521bd-112">By default, this filter will block edge traversed traffic to any application.</span></span>

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> <span data-ttu-id="521bd-113">介面條件的「傳遞」、「抵達」和「下一個躍點」類別可用來控制跨介面的弱式主機模型和封包轉送。</span><span class="sxs-lookup"><span data-stu-id="521bd-113">The 'Delivery', 'Arrival', and 'Next Hop' classes of interface conditions are used to control a weak-host model and packet forwarding across interfaces.</span></span> <span data-ttu-id="521bd-114">上述範例會利用「傳遞」類別。</span><span class="sxs-lookup"><span data-stu-id="521bd-114">The example above utilizes the 'Delivery' class.</span></span> <span data-ttu-id="521bd-115">請參閱 WFP SDK 檔中 [每個篩選層級的可用篩選準則](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) ，因為您的安全性設計必須考慮每個案例。</span><span class="sxs-lookup"><span data-stu-id="521bd-115">Please review [Filtering Conditions Available at Each Filtering Layer](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in the WFP SDK documentation, as your security design must take each case into consideration.</span></span>

 

## <a name="allow-filter-for-exempt-applications"></a><span data-ttu-id="521bd-116">允許篩選豁免應用程式</span><span class="sxs-lookup"><span data-stu-id="521bd-116">Allow Filter for Exempt Applications</span></span>

<span data-ttu-id="521bd-117">如果應用程式豁免于接聽通訊端上的 Teredo 流量，則必須在「ALE \_ 驗證 \_ RCV 在 \_ \_ 主機防火牆上接受 V6 篩選層」中實作為「允許」篩選準則。</span><span class="sxs-lookup"><span data-stu-id="521bd-117">If an application is exempt from receiving Teredo traffic on a listening socket, a permit filter must be implemented within the ALE\_AUTH\_RCV\_ACCEPT\_V6 filtering layer on the host firewall.</span></span> <span data-ttu-id="521bd-118">請務必注意，根據使用者或應用程式如何設定豁免，主機防火牆可以包含通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="521bd-118">It is important to note that depending on how the exemption is configured by the user or application, the host firewall can include a socket option.</span></span>

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a><span data-ttu-id="521bd-119">活動標注篩選</span><span class="sxs-lookup"><span data-stu-id="521bd-119">Dormancy Callout Filter</span></span>

<span data-ttu-id="521bd-120">Windows 中的 Teredo 服務會實行活動模型。</span><span class="sxs-lookup"><span data-stu-id="521bd-120">The Teredo service in Windows implements a dormancy model.</span></span> <span data-ttu-id="521bd-121">在任何指定的時間，如果沒有任何應用程式在啟用邊緣遍歷的 UDP 或 TCP 通訊端上接聽，則服務會移至休眠狀態。</span><span class="sxs-lookup"><span data-stu-id="521bd-121">At any given time, if no applications are listening on a UDP or TCP socket with edge traversal enabled, the service moves to a dormant state.</span></span> <span data-ttu-id="521bd-122">若要讓活動機制運作，主機防火牆必須針對在 TCP 的 ALE 驗證接聽 V6 篩選層內指定的每個豁免應用程式 \_ \_ \_ ，以及 \_ \_ \_ 針對以 UDP 為基礎的應用程式建立 ale 資源指派 V6 篩選層，以維護其注標篩選器。</span><span class="sxs-lookup"><span data-stu-id="521bd-122">For the dormancy mechanism to work, the host firewall must maintain a callout filter for each exempt application specified within the ALE\_AUTH\_LISTEN\_V6 filtering layer for TCP, and ALE\_RESOURCE\_ASSIGNMENT\_V6 filtering layer for UDP based applications.</span></span> <span data-ttu-id="521bd-123">下列範例示範 **TCP** 應用程式的活動標注。</span><span class="sxs-lookup"><span data-stu-id="521bd-123">The following sample below demonstrates a dormancy callout for a **TCP** application.</span></span>

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 