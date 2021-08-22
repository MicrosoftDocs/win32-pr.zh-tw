---
title: 執行 Teredo 的防火牆篩選器
description: Windows 可讓應用程式設定通訊端選項，讓應用程式能夠透過 Windows 篩選平台，來指示接收傳送至主機防火牆的 Teredo 流量的明確意圖。
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe854b210e6b07f0777a492d5c952f502e2f7c2b6c1c4b40497bad3a9e8248a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001804"
---
# <a name="implementing-firewall-filters-for-teredo"></a>執行 Teredo 的防火牆篩選器

Windows 可讓應用程式設定通訊端選項，讓應用程式能夠透過 Windows 篩選平台，來指示接收傳送至主機防火牆的 Teredo 流量的明確意圖。 在 Windows 中，用來設定保護層級的通訊端選項，可讓應用程式定義其願意接收的流量類型。 更具體來說，在涉及 Teredo 流量的案例中，會指定 [IPV6 \_ 保護 \_ 等級](/windows/desktop/WinSock/ipv6-protection-level) 通訊端選項。 建議主機防火牆執行維護下列篩選器，以選擇性地允許應用程式的 Teredo 流量，同時封鎖沒有豁免的任何應用程式的流量。

## <a name="default-block-filter-for-edge-traversed-traffic"></a>Edge 已通過流量的預設區塊篩選

如果 \_ \_ \_ \_ 流量符合指定的 **介面類別型 Tunnel** 以及 **Tunnel 類型的 Teredo** 條件，則主機防火牆必須在 ALE 驗證接收接受 V6 篩選層中，一律維持預設的區塊篩選。 執行時，此篩選準則會指出系統中有 edge 遍歷感知主機防火牆。 此篩選器會視為主機防火牆和 Windows 之間的 API 合約。 根據預設，此篩選準則會封鎖 edge 將流量流向任何應用程式。

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
> 介面條件的「傳遞」、「抵達」和「下一個躍點」類別可用來控制跨介面的弱式主機模型和封包轉送。 上述範例會利用「傳遞」類別。 請參閱 WFP SDK 檔中 [每個篩選層級的可用篩選準則](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) ，因為您的安全性設計必須考慮每個案例。

 

## <a name="allow-filter-for-exempt-applications"></a>允許篩選豁免應用程式

如果應用程式豁免于接聽通訊端上的 Teredo 流量，則必須在「ALE \_ 驗證 \_ RCV 在 \_ \_ 主機防火牆上接受 V6 篩選層」中實作為「允許」篩選準則。 請務必注意，根據使用者或應用程式如何設定豁免，主機防火牆可以包含通訊端選項。

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

## <a name="dormancy-callout-filter"></a>活動標注篩選

Windows 中的 Teredo 服務會執行活動模型。 在任何指定的時間，如果沒有任何應用程式在啟用邊緣遍歷的 UDP 或 TCP 通訊端上接聽，則服務會移至休眠狀態。 若要讓活動機制運作，主機防火牆必須針對在 TCP 的 ALE 驗證接聽 V6 篩選層內指定的每個豁免應用程式 \_ \_ \_ ，以及 \_ \_ \_ 針對以 UDP 為基礎的應用程式建立 ale 資源指派 V6 篩選層，以維護其注標篩選器。 下列範例示範 **TCP** 應用程式的活動標注。

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

 

 