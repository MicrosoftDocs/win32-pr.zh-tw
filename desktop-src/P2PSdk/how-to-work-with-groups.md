---
description: 對等群組是一種技術，可讓開發人員快速且有效地建立安全的對等網路。
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: 如何使用群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513412"
---
# <a name="how-to-work-with-groups"></a>如何使用群組

對等群組是一種技術，可讓開發人員快速且有效地建立安全的對等網路。 下列清單指出建立對等群組應用程式的主要考慮。

-   [取得對等身分識別](#obtaining-a-peer-identity)
-   [啟動對等群組](#starting-up-the-peer-grouping-infrastructure)
-   [註冊群組事件](#registering-for-peer-grouping-events)
-   [連接到群組](#obtaining-a-group-handle)
-   [建立系統管理員和成員角色](#creating-administrator-and-member-roles)
-   [尋找對等](#finding-a-peer)
-   [直接連接至對等](#connecting-directly-to-a-peer)
-   [關閉和關閉群組](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>取得對等身分識別

在建立或連接到群組之前，對等必須取得對等身分識別，這是用來唯一識別群組對等的名稱。 若要取得對等上定義之所有對等身分識別的列舉清單，請呼叫 [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)，它會傳回列舉的控制碼。 若要取得對等身分識別，請使用列舉控制碼和要取出的成員數目來呼叫 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) 。 繼續呼叫 **PeerGetNextItem** ，直到 *pCount* 參數傳回的值小於要求的對等身分識別數目。

如果對等的對等身分識別不存在，則可以藉由呼叫 [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)來建立。 建立對等身分識別之後，對等會產生身分識別 XML blob，其中包含指派給它的公開金鑰。

呼叫 [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)可取得對等身分識別資訊。 群組建立者或系統管理員會使用此對等身分識別資訊，來發出加入群組所需的認證，作為邀請 XML blob。

如需對等身分識別的詳細資訊，請參閱 [Identity MANAGER API](identity-manager-api.md) 檔

## <a name="starting-up-the-peer-grouping-infrastructure"></a>啟動對等群組基礎結構

在對等群組 API 中的任何函式由應用程式呼叫之前，必須先呼叫 [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) 。 此函數會初始化應用程式的對等群組基礎結構，並設定支援的版本。

## <a name="obtaining-a-group-handle"></a>取得群組控制碼

若要連接到群組並開始參與，必須取得對等群組的控制碼。 下列清單會識別用來連接到對等群組的三種方式：

-   藉由呼叫 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)來建立對等群組，這會初始化新的對等群組，並以擁有者和唯一系統管理員的對等來傳回有效的控制碼。
-   藉由呼叫 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)來加入對等群組。 若要加入對等群組，對等必須收到對等群組系統管理員的邀請。 若要取得邀請，請將身分識別資訊 XML blob 傳送給建立邀請的系統管理員，並使用外部機制（例如電子郵件或 FTP）將它傳送給您。 邀請和對等身分識別會傳遞至 **PeerGroupJoin**，這會將有效的控制碼傳回給群組。
-   藉由呼叫 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)，開啟對等互連先前已加入的對等群組。 在此情況下，不需要取得邀請。

從上述其中一個函式取得有效的對等群組控制碼之後，您可以使用新的控制碼呼叫 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) ，以連接到對等群組。

> [!Note]  
> 如果對等群組的連接失敗， \_ 就會發生「對等群組 \_ 事件 \_ 連接 \_ 失敗」事件。 處理常式可以嘗試重新建立對等群組的連接。

 

## <a name="registering-for-peer-grouping-events"></a>註冊對等群組事件

對等互連參與對等群組之前，對等體必須註冊對等群組事件。 若要註冊特定的對等事件，請呼叫 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)，然後傳入對等 \_ 群組 \_ 事件種類中定義的一或多個對等事件種類 \_ 。 您必須註冊適用于應用程式的每個對等事件;例如，若要透過直接連接接收資料，請註冊對等 \_ 群組 \_ 事件 \_ 直接 \_ 連接和對等 \_ 群組事件內送 \_ \_ \_ 資料事件。 每個呼叫都會接受一個事件控制碼，並傳回該對等事件的 **HPEEREVENT** 控制碼。

事件處理常式可以將已註冊之對等事件的控制碼傳遞至 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)，以取得與對等事件相關聯的資料。 此對等事件資料會以對等 \_ 群組 \_ 事件資料聯集的形式傳回 \_ 。 如果對等事件佇列是空的，則此函式會傳回對等 \_ S \_ 沒有任何 \_ 事件 \_ 資料。

您可以藉由呼叫 [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) 並提供您想要取消註冊之對等事件的控制碼，以取消註冊對等事件。 呼叫函式之後，與控制碼相關聯的對等事件就不再註冊。

## <a name="creating-administrator-and-member-roles"></a>建立系統管理員和成員角色

建立對等群組的對等稱為「對等群組建立者」，預設為「系統管理員」角色。 只有對等群組建立者可以設定群組屬性。

受邀至對等群組的對等可以是系統管理員或成員。 如果系統管理員將發出邀請的系統管理員角色指派給他們，他們可以邀請新成員加入對等群組，並同樣地將系統管理員角色指派給其他成員。

對等群組成員的角色是在系統管理員提供給成員的邀請中設定。 若要新增更多系統管理員，請 [](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) \_ \_ \_ 在建立邀請時，將 PeerGroupCreateInvitation 的 pRoles 參數值設定為對等群組角色系統管理員。

成員可以參與對等群組，但無法邀請及授權新的成員、設定群組屬性，或更新或刪除他們未特別建立的群組記錄。 若要將成員狀態指派給參與的對等，請 [](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) \_ \_ \_ 在建立該對等的邀請時，將 PeerGroupCreateInvitation 的 pRoles 參數值設定為對等群組角色成員。

若要變更成員的角色，必須將包含新角色的新認證發行給該成員。 若要完成此動作，請從 PeerGroupEnumMembers 傳回的對等成員結構取得這個成員的 [**對等 \_ 認證 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info)結構 \_ 。 [](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) 將 **對等 \_ 認證 \_ 資訊** 中的 **pRoles** 欄位變更為新的角色，並將結構傳遞至 [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)。

新的認證在連線到對等群組之前，將不會對對等的作用。 如果目前已連線，則必須關閉群組並重新連線，以取得更新的認證。

## <a name="finding-a-peer"></a>尋找對等

若要取得參與對等群組之所有對等的列舉清單，請使用群組控制碼呼叫 [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) ，此控制碼會傳回列舉的控制碼。 若要取得成員，請使用列舉控制碼和要取出的成員數目來呼叫 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) 。 繼續呼叫 **PeerGetNextItem** ，直到 *pCount* 參數傳回的值小於要求的成員數目。 請注意，可能不會傳回可用成員的完整清單。

每個成員都會表示為 [**對等 \_ 成員**](/windows/desktop/api/P2P/ns-p2p-peer_member) 結構，其中包含作用中對等的對等、節點識別碼和 IP 位址的識別。

完成時，請藉由呼叫 [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)來關閉列舉並釋放相關聯的記憶體。

## <a name="connecting-directly-to-a-peer"></a>直接連接至對等

當對等互連連線至對等群組時，會藉由呼叫 [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) 並提供另一個對等的身分識別，來初始化與其他連接的成員進行的直接交換。 此呼叫是非同步，而且會傳回64位的連接識別碼。 如果呼叫成功，您會收到對等 \_ 群組 \_ 事件 \_ DIRECT \_ 連接 \_ 事件對等事件，指出連接成功。 如果連接成功，連接識別碼會是有效的，而且可用來透過直接連接來傳送和接收資料。

若要能夠接收直接連接，另一個對等也必須先前註冊對等 \_ 群組 \_ 事件 \_ 直接 \_ 連接對等事件。

若要將資料傳送給對等，請使用有效的連接識別碼呼叫 [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) 。 若要接收資料，必須為對等 \_ 群組 \_ 事件 \_ 傳入 \_ 資料對等事件註冊另一個對等。 同樣地，如果傳送對等想要接收資料，它也必須針對對等 \_ 群組事件內送 \_ \_ \_ 資料對等事件註冊。

若要接收群組中其他對等目前作用中直接連接的總集合，請呼叫 [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) 開啟列舉，然後使用 [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)來逐一查看連接清單。

若要關閉直接連接，請呼叫 [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) 並傳入連接識別碼。

## <a name="closing-and-shutting-down-a-peer-group"></a>關閉和關閉對等群組

若要關閉對等群組的連接，請呼叫 [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)，使群組控制碼失效，但不關閉對等群組基礎結構。 呼叫 [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)會刪除對等群組資料。

當應用程式使用對等群組基礎結構完成時，必須呼叫 [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown)。

 

 



