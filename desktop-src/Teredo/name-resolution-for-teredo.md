---
title: Teredo 的名稱解析
ms.assetid: eb0cf6d5-f093-46f6-8995-d01971de8241
description: 深入瞭解： Teredo 的名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d9c41685977ef5a4ae3e94996a8d1a59db5f9812e2ed8efe758878a9055c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001686"
---
# <a name="name-resolution-for-teredo"></a>Teredo 的名稱解析

Teredo 介面目前會利用下列通訊協定來進行名稱解析：

## <a name="domain-name-system"></a>網域名稱系統

網域名稱系統 (DNS) 目前是網際網路上最顯著的名稱解析技術。 大部分的網頁伺服器都會向 DNS 伺服器註冊 URL 位址。 不過，家用網路的位址並不會登錄到 DNS 伺服器，因為大部分的家庭使用者透過動態主機設定通訊協定 (DHCP) 從其網際網路服務提供者取得 IP 位址。 DHCP 租用的持續時間相對較短，而從48到72小時的任何時間都需要將名稱傳播到整個 DNS 雲端。 如此一來，DNS 已證明成為取得家庭使用者的公用 IP 位址的無效方法。 Teredo 位址包含公用 IPv4 位址，因此至少會繼承相同的 IPv4 位址變動性。 因此，Teredo 位址目前未在 DNS 中註冊。

## <a name="peer-name-resolution-protocol"></a>對等名稱解析通訊協定

對等名稱解析通訊協定 (PNRP) 是一種分散式 DNS 技術，可將 IP 位址儲存在屬於 PNRP 雲端一部分的數千部使用者電腦上。 使用 Windows Vista，任何家庭使用者都可以選擇成為 pnrp 雲端的成員，並在 pnrp 網路上通告其 Teredo IPv6 位址。 不同于提供給 DNS 伺服器的位址，PNRP 網路上的位址通常需要不到一分鐘的時間來傳播。 由於 Teredo 位址可以經常變更 (ISP 提供的外部 IPv4 位址可能會變更，或者使用者的網際網路閘道裝置所使用的外部埠可能會變更) ，PNRP 已證明是適用于家庭使用者的有效機制。 PNRP 名稱是以 ". pnrp.net" 結尾的位址，是以不會變更的唯一系統屬性為基礎。 因此，PNRP 名稱是連接到家庭使用者的可靠方式。 [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamea) API 可用來取得使用 PNRP 技術 (DNS 名稱結尾為 ". pnrp.net" ) 的 IP 位址，並建立與其他主機的連接。

 

 
