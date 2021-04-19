---
description: 對等名稱解析通訊協定會使用對等名稱解析通訊協定 (PNRP) 、對等身分識別管理員以及對等群組基礎結構。
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: 對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18774939d5e0e9bad208999fbc6ca1e5f624300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000123"
---
# <a name="peer-names"></a>對等名稱

對等名稱解析通訊協定會使用對等名稱解析通訊協定 (PNRP) 、對等身分識別管理員以及對等群組基礎結構。 對等名稱是資源的穩定名稱，例如電腦、使用者、群組或服務。 PNRP 會使用對等名稱來識別對等網路中的節點。

> [!Note]  
> 對等基礎結構所使用的端點實際上是包含 IPv4 或 IPv6 位址、埠和通訊協定 (TCP 或 UDP) 的元組。 一個對等名稱可以有一個以上的元組。

 

對等名稱是具有下列格式的文字字串：

-   「授權單位。分類器」

授權單位的值取決於名稱是安全的還是不安全的。 對等名稱的分類器是字串。 分類器可以是包含150或更少 UNICODE 字元的任何名稱。 對等名稱會區分大小寫，而且可以註冊為安全或不安全的。 下列清單會識別對等名稱的一些範例：

-   "0. MyUnsecuredPeerName"
-   "0. JohnDoe"
-   "6520c005f63fc1864b7d8f3cabebd4916ae7f33d.JohnDoe

## <a name="secure-peer-names"></a>安全對等名稱

若為安全名稱，授權單位為安全雜湊演算法 (SHA) 對等名稱公開金鑰的雜湊，並產生40個字元的十六進位字串。 安全的對等名稱只能透過對等名稱擁有者的擁有者或委派向 PNRP 註冊。 您必須藉由呼叫 [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)來建立安全的對等名稱。

## <a name="unsecured-peer-names"></a>不安全的對等名稱

若為不安全的名稱，授權單位為零 (0) ，而且分類器是對等名稱的唯一重要部分，這會在沒有相關聯的身分 [識別](identity-manager-api.md)的情況下建立不安全的對等名稱。 不安全的對等名稱是在 PNRP 名稱註冊和解析中使用。 不安全的對等名稱提供了一種實用的方法，可用來註冊及解析不需要安全名稱解析的資源。 不過，任何節點都可以發佈任何不安全的名稱。 關心安全性的應用程式必須確保它們在取用不安全的對等名稱時是穩固且安全的。

> [!Note]  
> 任何人都可以使用 PNRP 註冊不安全的對等名稱。

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP 和最接近的對等名稱實例

對等名稱可以有一個以上的實例。 使用 [PNRP](pnrp-namespace-provider-api.md)解析對等名稱時，會有 **最接近** 的對等名稱實例的概念，表示名稱的服務位置最接近 [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)或 [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))中指定的 **saHint** 成員。 如果未提供任何提示，則最接近其中一個本機 IP 位址。

 

 
