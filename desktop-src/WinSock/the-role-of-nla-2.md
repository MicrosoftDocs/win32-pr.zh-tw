---
description: 網路位置感知 (NLA) 服務提供者對於可能在不同網路間移動的電腦或裝置而言很重要，而且當有一個以上的設定可供使用時，可以選取最佳設定。
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: NLA 的角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f44d517fc9f32d4fb61eb2b4d9b61c473bc946066e670fcb51f0ca2c753e692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733338"
---
# <a name="the-role-of-nla"></a>NLA 的角色

網路位置感知 (NLA) 服務提供者對於可能在不同網路間移動的電腦或裝置而言很重要，而且當有一個以上的設定可供使用時，可以選取最佳設定。 例如，實體網路之間的無線電腦漫遊可以根據其可用網路連線的相關資訊，使用 NLA 判斷適當的設定。 當多重主目錄電腦具有一個網路的實體連線，同時透過撥號連線或通道連線到另一個網路時，NLA 也可證明有價值。

在過去，開發人員必須取得邏輯網路介面的相關資訊，因此會根據許多不同的網路資訊來決定網路連線能力。 在這些情況下，開發人員必須根據 IP 位址、介面的子網、網域名稱系統 (與介面相關聯的 DNS) 名稱、NIC 的 MAC 位址、無線網路名稱或其他網路資訊，來選擇適當的網路介面。 NLA 藉由提供用來列舉邏輯網路附件資訊的標準介面、將它與實體網路介面資訊相關聯，然後在先前傳回的資訊失效時提供通知，來減輕這個問題。

NLA 提供下列網路位置資訊：

<dl> <dt>

<span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>邏輯網路身分識別
</dt> <dd>

NLA 會先嘗試依照其 DNS 功能變數名稱來識別邏輯網路。 如果邏輯網路沒有功能變數名稱，NLA 會從儲存在登錄中的自訂靜態資訊識別網路，最後從其子網位址識別網路。

</dd> <dt>

<span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>邏輯網路介面
</dt> <dd>

針對電腦所連接的每個網路，NLA 提供可唯一識別實體介面（例如 NIC）或邏輯介面（例如 RAS 連線）的 *AdapterName* 。 然後，AdapterName 可搭配 IP 協助程式 API 中提供的函式使用，以取得進一步的介面特性。

</dd> </dl>

NLA 會使用相關聯的類別 GUID 和屬性，將邏輯網路實作為服務類別。 NLA 傳回信息的每個邏輯網路是該服務類別的實例。

 

 



