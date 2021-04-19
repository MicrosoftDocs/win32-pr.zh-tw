---
description: 對等身分識別管理員 API 會使用下列功能。
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Identity Manager 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea56df6500239141038f76ba312b84148581f8f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974684"
---
# <a name="identity-manager-functions"></a>Identity Manager 函數

對等身分識別管理員 API 會使用下列功能。



| 函式                                                           | 描述                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | 根據指定之對等身分識別和分類器的現有名稱，建立新的名稱。 但是，不會呼叫 [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)來建立新的身分識別。                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | 建立並傳回對等列舉控制碼，用來列舉與特定對等身分識別相關聯的所有對等群組。                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | 建立並傳回對等列舉控制碼，用來列舉屬於特定使用者的所有對等身分識別。                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | 釋出列舉，例如記錄或成員列舉，並解除配置與列舉相關聯的所有資源。                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | 解除配置資料區塊，並將其傳回記憶體集區。                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | 傳回對等列舉中的專案計數。                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | 從對等列舉傳回特定數目的專案。                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | 建立新的對等身分識別，並傳回其名稱。 對等身分識別的名稱必須在所有後續呼叫中傳遞給對等身分識別管理員、對等群組，或代表對等身分識別的 PNRP 函數。 對等身分識別名稱會指定正在使用的對等身分識別。 |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | 刪除對等身分識別。 這包括移除所有與指定之對等身分識別相關聯的憑證、私密金鑰和所有群組資訊。                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | 允許使用者匯出一個對等身分識別。 然後使用者可以將對等身分識別傳送到不同的電腦。                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         |  (CSP) 抓取密碼編譯服務提供者的控制碼。                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | 抓取目前使用者的預設對等名稱集。                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | 傳回對等身分識別的易記名稱。                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | 傳回對等身分識別的描述，然後可將其傳遞給協力廠商，並用來邀請對等群組的對等身分識別。 這項資訊會以 XML 片段的形式傳回。                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | 匯入一個對等身分識別。 如果對等身分識別存在於電腦上，則會傳回 **對等 \_ \_ \_** 互連。                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | 修改指定之對等身分識別的易記名稱。 易記名稱是人們可讀取的名稱。                                                                                                                                                                                                |



 

 

 



