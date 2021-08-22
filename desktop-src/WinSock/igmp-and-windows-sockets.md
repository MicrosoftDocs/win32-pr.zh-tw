---
description: Windows通訊端可透過使用通訊端選項和 IOCTLs，在 IPv6 和網際網路群組管理通訊協定上 (MLD) 啟用多播接聽程式探索，以 (IGMP) IPv4 上的多播應用程式。
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: 使用 Windows 通訊端的 MLD 和 IGMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051646"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>使用 Windows 通訊端的 MLD 和 IGMP

Windows通訊端可透過使用通訊端選項和 IOCTLs，在 IPv6 和網際網路群組管理通訊協定上 (MLD) 啟用多播接聽程式探索，以 (IGMP) IPv4 上的多播應用程式。 此頁面說明啟用多播程式設計的通訊端選項，並說明其使用方式。 如需每個通訊端選項的定義，請參閱 [ [通訊端選項](socket-options.md) ] 頁面。

如需有關使用 IOCTLs 進行多播程式設計的詳細資訊，請參閱本節稍後的 [最終狀態式多播程式設計](final-state-based-multicast-programming.md) 。

在 Windows Vista 和更新版本上，有一組通訊端選項可用於支援 IPv6 和 IPv4 位址的多播程式設計。 這些通訊端選項與 IP 無關，而且可以同時用於 IPv6 和 IPv4。 在 IPv6 上，這些通訊端選項使用 MLDv2。 在 IPv4 上，這些通訊端選項使用 IGMPv3。 這些 IP 中立的選項是 Windows Vista 和更新版本的多播程式設計的慣用通訊端選項。 Windows通訊端會使用下列通訊端選項： 

| 通訊端選項               | 引數類型                                            |
|-----------------------------|----------------------------------------------------------|
| MCAST \_ 區塊 \_ 來源        | [**群組 \_來源 \_ 需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) 結構 |
| MCAST \_ 聯結 \_ 群組          | [**群組 \_需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) 結構                |
| MCAST \_ 聯結 \_ 來源 \_ 群組  | [**群組 \_來源 \_ 需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) 結構 |
| MCAST \_ 離開 \_ 群組         | [**群組 \_需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req) 結構                |
| MCAST \_ 離開 \_ 來源 \_ 群組 | [**群組 \_來源 \_ 需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) 結構 |
| MCAST \_ 解除封鎖 \_ 來源      | [**群組 \_來源 \_ 需求**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) 結構 |



 

一組通訊端選項適用于支援 IPv6 專用位址的多播程式設計。 這些通訊端選項使用 MLDv1 或 MLDv2。 使用的 MLD 版本取決於 Windows 的版本。 Windows Vista 和更新版本支援 MLDv2。 Windows通訊端會使用下列通訊端選項： 

| 通訊端選項          | 引數類型                             |
|------------------------|-------------------------------------------|
| IPV6 \_ 新增 \_ 成員資格  | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) 結構 |
| IPV6 \_ 捨棄 \_ 成員資格 | [**ipv6 \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) 結構 |



 

一組通訊端選項適用于僅支援 IPv4 位址的多播程式設計。 這些通訊端選項使用 IGMPv3 或 IGMPv2。 使用的 IGMP 版本取決於 Windows 的版本。 Windows Vista 和更新版本支援 IGMPv3。 Windows通訊端會使用下列通訊端選項：

| 通訊端選項                | 引數類型                                        |
|------------------------------|------------------------------------------------------|
| IP \_ 新增 \_ 成員資格          | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) 結構                |
| IP \_ 新增 \_ 來源 \_ 成員資格  | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) 結構 |
| IP \_ 區塊 \_ 來源            | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) 結構 |
| IP \_ 捨棄 \_ 成員資格         | [**ip \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq) 結構                |
| IP \_ DROP \_ SOURCE \_ 成員資格 | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) 結構 |
| IP \_ 解除封鎖 \_ 來源          | [**ip \_ mreq \_ 來源**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) 結構 |



 

當 IGMPv3 可用時， \_ \_ \_ 就會更有效率地處理 ip 新增來源成員資格、ip \_ 區塊 \_ 來源、ip \_ 放置 \_ 來源 \_ 成員資格和 ip \_ 解除封鎖 \_ 來源選項，因為路由器可以處理篩選。 當只有 IGMPv2 可用時，主機必須處理篩選。

大部分的應用程式可能會落在兩個類別中：任何來源和受控制的來源。

-   依預設，**任何來源** 應用程式都會接受所有來源，以便視需要關閉個別來源。 任何來源應用程式的範例是可讓所有收件者參與的影片會議通話。
-   **受控制的來源** 應用程式會將來源限制為指定的清單，例如網際網路無線電站，或有明顯事件的廣播。 使用通訊端選項的程式對每個選項稍有不同。

在 Windows Vista 和更新版本上，下列步驟適用于任何來源應用程式：

- 使用 **MCAST \_ 聯結 \_ 群組** 加入群組。  
- 如有需要，請使用 **MCAST \_ 區塊 \_ 來源** 來關閉指定的來源。  
- 若有需要，請使用 **MCAST \_ 解除封鎖 \_ 來源** 來重新允許封鎖的來源。  
- 使用 **MCAST \_ 離開 \_ 群組** 來離開群組。  

在 Windows Vista 和更新版本上，下列步驟適用于受控制的來源應用程式：

- 使用 **MCAST \_ 聯結 \_ 來源 \_ 群組** 來聯結每個群組/來源配對。  
- 如果所有來源都使用相同的群組位址，請使用 **MCAST \_ 保留 \_ 來源 \_ 群組** 來保留每個群組/來源，或使用 **MCAST \_ 離開 \_ 群組** 來保留所有來源。  

下列步驟適用于任何來源應用程式：

- 使用 **IP \_ 新增 \_ 成員資格** 加入群組 (ipv6) 的 **ipv6 \_ 新增 \_ 成員資格** 。  
- 如有需要，請使用 **IP \_ 區塊 \_ 來源** 來關閉指定的來源。  
- 如有需要，請使用 **IP \_ 解除封鎖 \_ 來源** 來重新允許封鎖的來源。  
- 使用 **IP \_ DROP \_ 成員資格** ，讓群組 (ipv6) 的 **ipv6 \_ 捨棄 \_ 成員資格** 。  

下列步驟適用于受控制的來源應用程式：

- 使用 **IP \_ 新增 \_ 來源 \_ 成員資格** 加入每個群組/來源配對。  
- 如果所有來源都使用相同的群組位址，請使用 **ip \_ drop \_ SOURCE \_ 成員資格** 來保留每個群組/來源，或使用 **ip \_ drop \_ 成員資格** 來保留所有來源。  

設定這些通訊端選項的順序有相關聯的規則。 如需多播通訊端選項的詳細資訊和疑難排解資訊，請參閱 [多播通訊端選項行為](multicast-socket-option-behavior.md)。
