---
title: 複寫、主機和資料庫服務的服務連接點
description: 當您使用服務連接點發佈服務時 (SCP) ，請考慮用戶端如何找到服務的 SCP。
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- 複寫、主機型和資料庫服務 AD 的服務連接點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7658cc60704dbfc37009272e5f14f997d213ea993054fa22c1c5e0c307794b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024896"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>複寫、主機和資料庫服務的服務連接點

當您使用服務連接點發佈服務時 (SCP) ，請考慮用戶端如何找到服務的 SCP。 如果有多個服務實例存在，請考慮用戶端如何使用具有不同功能的類似服務來區別服務與所需的功能。 如果您發行複寫的服務，請考慮用戶端將如何選擇複本。 本主題討論各種服務類型的這些問題。

## <a name="replicable-services"></a>可複製服務

針對可複製服務，服務可以有一或多個實例（或複本），而用戶端不在意它們所連接的複本，因為每一個都提供相同的服務。 Active Directory Domain Services 是複寫服務的範例：指定網域的所有網域控制站都會保存相同的資料、受限於複寫延遲，並提供相同的服務。

可複寫的服務可以將多個複本的 Scp 和其他服務特定物件儲存在單一容器中。 第一個複本的設定應用程式可以建立容器做為本機網域系統容器的子系。 如需詳細資訊，請參閱 [在網域系統容器中發行](publishing-in-a-domain-system-container.md)。 確定容器的安全描述項允許後續複本的安裝程式在相同的容器中建立其物件。 授與安裝系統管理員的許可權，以指定可建立或修改容器中物件的使用者或群組。

可複製服務的其中一個策略是為每個複本建立 SCP。 當用戶端查詢服務的產品 GUID 或其他標識關鍵字時，它會尋找所有複本的 SCP 物件，並隨機選取一個或使用某些負載平衡演算法。 例如，系統管理員可以指定每個複本的優先順序和負載平衡資料，類似于 DNS SRV 記錄的優先順序和權數位段。 服務的安裝應用程式可以將此資料儲存在每個複本 SCP 的 **serviceBindingInformation** 屬性中。 用戶端會從每個 SCP 取出資料，並使用它來選取複本。

另一種策略是為所有複本建立單一 SCP，並將 SCP **serviceDNSName** 屬性設定為 DNS SRV 記錄的名稱。 接著，每個複本的設定應用程式會使用該名稱註冊 SRV 記錄。 當用戶端識別服務的獨立 SCP 時，用戶端會抓取 SRV 記錄的名稱，並使用 [**DnsQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) 函式來取得複本的 srv 記錄陣列。 每個 SRV 記錄包含主機電腦的名稱，以及用戶端可用來選取複本的其他資料。

## <a name="database-services"></a>資料庫服務

資料庫服務的不同實例可能包含完全不同的資料，即使它們都是相同類型的服務，通常稱為服務類別。 若要發行這類服務，SCP 的 **關鍵字** 屬性可以識別服務類別和特定的資料庫。 一般用途的用戶端只知道服務類別的 GUID 可以查詢該服務類別所發行的所有資料庫，然後呈現使用者介面，讓使用者可以選取其中一個。 對於專門針對目標資料庫所設計的用戶端，您可以在用戶端程式代碼中將資料庫 GUID 硬式編碼。

## <a name="host-based-services"></a>以主機為基礎的服務

以主機為基礎的服務是與單一主機電腦緊密系結的服務。 您可以在多部電腦上安裝服務類別的實例，而且每個實例都會提供使用其主機電腦識別的服務。

以主機為基礎的服務的每個實例都應該在其主機的電腦物件下建立自己的 SCP。 使用產品 GUID 來搜尋主機服務之 SCP 的用戶端，通常會在整個企業樹系中尋找服務類別的許多實例。 然後，用戶端可以使用 Scp 的 **serviceDNSName** 屬性，在所需的主機電腦上尋找服務實例的 SCP。

 

 