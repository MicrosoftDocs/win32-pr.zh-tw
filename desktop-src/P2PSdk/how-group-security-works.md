---
description: 對等群組需要每個成員都有特定的憑證，稱為群組成員憑證 (GMC) 。
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: 群組安全性的運作方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941b4bded19b914218d5c011e8696cdd9c92612a493954dc5dd45d91e59006a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675208"
---
# <a name="how-group-security-works"></a>群組安全性的運作方式

對等群組需要每個成員都有特定的憑證，稱為群組成員憑證 (GMC) 。 GMC 憑證可確保對等之間交換的所有記錄都經過數位簽署。 對等的公開金鑰會包含在傳遞的結構中，這些結構會在對等之間進行通訊時傳遞，包括 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)。

GMC 可以在鏈中發出。 例如，建立者可以發出 GMC 給系統管理員 A，讓誰可以向系統管理員 B 發出 GMC，他們可以將 GMC 發給成員 M。產生的 GMC 鏈是： creator->A->B->M，其長度為4。 連鎖長度很重要，因為它的長度不能超過24。 如果鏈中的24日系統管理員嘗試將 GMC 發給成員， [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 或 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) 會傳回對等 \_ E \_ 鏈 \_ 太長的 \_ 時間。

GMC 也可以藉由呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)來發出。 GMC 意指 GMC 發出的群組中的使用者成員資格，而且可以有有限或無限的存留期。 群組成員活動的長度不能超過 GMC 中指定的存留期。

> [!Note]  
> 無限 GMC 存留期目前設定為1000年。

 

群組成員活動會受限於 GMC 存留期，並包含下列各項：

-   **記錄作業** ：當群組成員資格到期之後，對等無法在群組中發行資訊，或發行存留期超過對等群組成員資格存留期的記錄。
-   **成員資格作業** -群組系統管理員無法發行存留期超過群組管理員成員資格中指定之日期的成員資格。 例如，如果系統管理員在其 GMC 存留期內剩餘500小時，則所有發行的成員資格都必須小於500小時。

因為群組成員的存留期不能超過邀請該群組成員的系統管理員，建議您將系統管理員的 GMC 存留期設為無限期，或設定為很長的存留期。 群組建立者預設為無限存留期。

## <a name="renewing-group-membership"></a>更新群組成員資格

若要更新 GMC 存留期已準備好到期的系統管理員或成員的認證，您有下列兩個選項：

-   呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 並傳遞其存留期已準備好到期的成員身分識別。 如果認證已指定為 **Null** ，且對等的成員資格資訊可供群組使用，則會將更新時間設定為先前發佈的成員認證中所指定的相同持續時間。 如果必須指定不同的持續期間，則必須提供新的 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) 結構，其中包含新的存留期持續時間，然後為該成員發行新的 GMC。

    [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)函式會選擇性地採用對等 \_ 群組 \_ 存放區 \_ 認證旗標，此旗標會自動發行群組資料庫中成員的新認證。 當成員下次連接到群組時，在第一次或離線之後，成員會從資料庫取得更新的 GMC。

-   呼叫 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ，以傳遞 GMC 存留期已就緒即將到期之成員的身分識別。 如果邀請中指定的到期日為 **Null**，則 GMC 的存留期間會與發出成員資格的系統管理員 GMC 相同。 如果建立者將到期指定為 **Null**，則會發出無限存留期的 GMC。

    如果對等發出的 GMC 是在存在存留期值之前過期，則對等體的位址就無法在由 [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)呼叫所起始的列舉中傳回的 [**對等 \_ 成員**](/windows/desktop/api/P2P/ns-p2p-peer_member)結構中使用。 發生這種情況是因為在此情況下，即使未設定對等 \_ 停用狀態旗標，也不會發佈存在性資訊 \_ 。

 

 



