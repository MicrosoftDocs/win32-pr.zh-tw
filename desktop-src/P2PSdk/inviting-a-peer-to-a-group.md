---
description: 本主題討論如何使用對等群組 Api 邀請對等加入對等群組的程式。
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: 邀請對等群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760c2fb6023d5332da74402726669367fee4f5102c99269fa8e603653a1e2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612648"
---
# <a name="inviting-a-peer-to-a-group"></a>邀請對等群組

本主題討論如何使用對等群組 Api 邀請對等加入對等群組的程式。

對等群組需要有效的認證才能參與。 認證會以邀請形式從群組外部發出，或在需要認證更新時直接發給群組內的成員。

## <a name="group-member-certificates"></a>群組成員憑證

當應用程式呼叫 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)時，就會建立對等群組。

若要參與對等群組，每個對等都必須有對等身分識別。 呼叫 [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) 直到已傳回對等定義的所有對等身分識別，然後選取應該使用的對等身分識別。 如果對等身分識別不存在，請呼叫 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)來建立一個。

每個對等身分識別都與一組特定的認證相關聯，這些認證可以用來在連接時證明對等群組成員資格，以及發佈記錄或邀請其他成員的情況。 這些認證會以 [x.509](https://www.ietf.org/rfc/rfc2511.txt) 憑證的鏈形式表示，稱為群組成員資格憑證 (GMC) 。

若要建立對等身分識別的 GMC，您必須先取得其公開金鑰。 藉由在潛在的受邀者上呼叫 [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) 並傳入其對等身分識別，即可取得此金鑰。 此函式會傳回以64編碼的編碼憑證 (IDC) ，其中包含用來建立對等身分識別的 RSA 公開金鑰 (在以 XML blob 封裝的其他) 專案中，以下列格式來建立 GMC：

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

這個字串可以傳遞給 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)，它會傳回包含該對等身分識別之 GMC 的邀請。 邀請必須使用不同的程式（例如電子郵件、FTP 或安全檔案共用）傳遞給受邀者。

或者，您也可以將 IDC 本身放置在新的 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) 結構中，並傳遞給 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)，這同樣會產生邀請。

請注意，應用程式不能在 **PEERIDENTITYINFO** 標記內新增標記，或以任何方式修改此 XML 片段。 應用程式可以將這個 XML 片段併入其他 XML 檔，但必須先去除所有應用程式專屬的 XML，才能將此片段傳遞給 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) 或 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 函數。

成員 GMCs 由系統管理員和對等群組建立者所發出。 成員必須取得新的 GMCs，並在超過到期時間之前，先取得其 GMCs 的延長存留期。 對等群組系統管理員會藉由呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) 與該對等現有的認證來發出更新的認證。

[**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)結構包含對等成員資格狀態的基本資料，包括其 GMC 的公開金鑰。 您可以藉由 \_ \_ \_ 在 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)的呼叫中設定對等群組存放區認證旗標，將新發行的認證發行至對等群組。 當新認證的收件者加入對等群組時，對等群組基礎結構將會更新現有的認證。

## <a name="issuing-an-invitation"></a>發出邀請

以下列兩種方式之一，邀請成員加入對等群組：

-   對等群組系統管理員會呼叫 [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)，傳入透過一般頻外機制（例如電子郵件或 IM 會話）從潛在的受邀者取得的身分識別資訊 XML 字串。 邀請也會透過部分外部進程或機制傳遞給對等，最後會將其接收為 XML 字串或文字檔。
-   對等群組系統管理員會呼叫 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)。 若要使用此函式，對等體必須已經將成員資格資訊發行至對等群組 ([**對等 \_ 成員**](/windows/desktop/api/P2P/ns-p2p-peer_member)) ，或有用於建立主體身分識別) 之 RSA 金鑰組的可用公開金鑰 (。 在先前的案例中， **PeerGroupIssueCredentials** 所需的 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)結構可以從 **對等 \_ 成員** 結構取得，在後者的情況下，可以使用公開金鑰填入新的 **對等 \_ 認證 \_ 資訊** 結構。

收到邀請字串之後，對等會將它傳遞給 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) ，以加入對等群組。 如果 **PeerGroupJoin** 的呼叫成功，則對等可以藉由呼叫 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)來開啟對等群組。

## <a name="parsing-an-invitation"></a>剖析邀請

（選擇性）您可以藉由呼叫 [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)來剖析邀請，這會傳回 [**對等 \_ 邀請 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) 結構。 您可以輕鬆地取得結構中的欄位以供顯示之用。

 

 



