---
description: 協同作業 API 函數
ms.assetid: 00c3c1f1-c36c-469a-a644-0ec60f02d25e
title: 協同作業 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803e492a378b3f5b04c9f894cefa679cfbd77aff305874a706f668b970d7b53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794566"
---
# <a name="collaboration-api-functions"></a>協同作業 API 函數

對等共同作業基礎結構支援下列功能。



| 函式                                                                                       | 描述                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCollabAddContact**](/windows/desktop/api/P2P/nf-p2p-peercollabaddcontact)                                           | 將連絡人加入至對等的連絡人清單。                                                                                                                                                   |
| [**PeerCollabAsyncInviteContact**](/windows/desktop/api/P2P/nf-p2p-peercollabasyncinvitecontact)                           | 傳送邀請給受信任的對等連絡人，以透過安全的連接來加入傳送者的對等共同作業活動。                                                                       |
| [**PeerCollabAsyncInviteEndpoint**](/windows/desktop/api/P2P/nf-p2p-peercollabasyncinviteendpoint)                         | 將邀請傳送至指定的對等端點，以加入傳送者的對等共同作業活動。 邀請的回應可用性會透過非同步事件進行更新。 |
| [**PeerCollabCancelInvitation**](/windows/desktop/api/P2P/nf-p2p-peercollabcancelinvitation)                               | 取消呼叫者先前傳送給連絡人的邀請。                                                                                                                               |
| [**PeerCollabCloseHandle**](/windows/desktop/api/P2P/nf-p2p-peercollabclosehandle)                                         | 關閉對等共同作業活動邀請的控制碼。                                                                                                                                  |
| [**PeerCollabDeleteContact**](/windows/desktop/api/P2P/nf-p2p-peercollabdeletecontact)                                     | 從目前的對等刪除連絡人。                                                                                                                                                        |
| [**PeerCollabDeleteEndpointData**](/windows/desktop/api/P2P/nf-p2p-peercollabdeleteendpointdata)                           | 刪除符合所提供端點資料之呼叫端節點上的對等端點資料。                                                                                                |
| [**PeerCollabDeleteObject**](/windows/desktop/api/P2P/nf-p2p-peercollabdeleteobject)                                       | 刪除呼叫端點中的對等物件。                                                                                                                                                |
| [**PeerCollabEnumApplications**](/windows/desktop/api/P2P/nf-p2p-peercollabenumapplications)                               | 傳回列舉的控制碼，其中包含註冊至特定對等端點 (s) 的功能。                                                                                |
| [**PeerCollabEnumApplicationRegistrationInfo**](/windows/desktop/api/P2P/nf-p2p-peercollabenumapplicationregistrationinfo) | 取得用來取得對等應用程式資訊的列舉控制碼。                                                                                                                   |
| [**PeerCollabEnumContacts**](/windows/desktop/api/P2P/nf-p2p-peercollabenumcontacts)                                       | 傳回列舉集合的控制碼，其中包含目前可在呼叫端上取得的所有對等共同作業網路連絡人。                                                     |
| [**PeerCollabEnumEndpoints**](/windows/desktop/api/P2P/nf-p2p-peercollabenumendpoints)                                     | 傳回列舉的控制碼，其中包含與特定對等連絡人相關聯的端點。                                                                                       |
| [**PeerCollabEnumObjects**](/windows/desktop/api/P2P/nf-p2p-peercollabenumobjects)                                         | 傳回列舉的控制碼，其中包含與特定對等端點相關聯的對等物件。                                                                                 |
| [**PeerCollabEnumPeopleNearMe**](/windows/desktop/api/P2P/nf-p2p-peercollabenumpeoplenearme)                               | 傳回列舉集合的控制碼，其中包含目前可在呼叫端對等的子網上使用的所有對等共同作業網路「近端分享」端點。                     |
| [**PeerCollabExportContact**](/windows/desktop/api/P2P/nf-p2p-peercollabexportcontact)                                     | 將與對等名稱相關聯的連絡人資料匯出至 contact XML 資料字串緩衝區。                                                                                                       |
| [**PeerCollabGetAppLaunchInfo**](/windows/desktop/api/P2P/nf-p2p-peercollabgetapplaunchinfo)                               | 取得對等應用程式啟動資訊，包括連絡人名稱、對等端點和邀請要求。                                                                     |
| [**PeerCollabGetApplicationRegistrationInfo**](/windows/desktop/api/P2P/nf-p2p-peercollabgetapplicationregistrationinfo)   | 取得特定的應用程式註冊資訊。                                                                                                                                          |
| [**PeerCollabGetContact**](/windows/desktop/api/P2P/nf-p2p-peercollabgetcontact)                                           | 根據連絡人的對等名稱，取得特定對等連絡人的資訊。                                                                                                         |
| [**PeerCollabGetEndpointName**](/windows/desktop/api/P2P/nf-p2p-peercollabgetendpointname)                                 | 抓取先前由呼叫 PeerCollabSetEndpointName 所設定之呼叫對等目前端點的名稱。                                                                           |
| [**PeerCollabGetEventData**](/windows/desktop/api/P2P/nf-p2p-peercollabgeteventdata)                                       | 取得與對等上引發之對等共同作業事件相關聯的資料。                                                                                                                 |
| [**PeerCollabGetInvitationResponse**](/windows/desktop/api/P2P/nf-p2p-peercollabgetinvitationresponse)                     | 取得先前受邀加入對等共同作業活動的對等回應。                                                                                                        |
| [**PeerCollabGetPresenceInfo**](/windows/desktop/api/P2P/nf-p2p-peercollabgetpresenceinfo)                                 | 抓取與特定連絡人相關聯之端點的顯示狀態資訊。                                                                                                         |
| [**PeerCollabGetSigninOptions**](/windows/desktop/api/P2P/nf-p2p-peercollabgetsigninoptions)                               | 取得對等的目前已登入對等共同作業網路目前狀態選項。                                                                                                               |
| [**PeerCollabInviteContact**](/windows/desktop/api/P2P/nf-p2p-peercollabinvitecontact)                                     | 傳送邀請以將對等共同作業活動加入至信任的連絡人。 此呼叫是同步的，如果成功，就會取得連絡人的回應。                               |
| [**PeerCollabInviteEndpoint**](/windows/desktop/api/P2P/nf-p2p-peercollabinviteendpoint)                                   | 將邀請傳送至指定的對等端點，以加入傳送者的對等共同作業活動。 此呼叫是同步的，如果成功，則會從對等端點取得回應。      |
| [**PeerCollabParseContact**](/windows/desktop/api/P2P/nf-p2p-peercollabparsecontact)                                       | 將包含 contact XML 資料的 Unicode 字串緩衝區剖析為 [**對等 \_ 連絡人**](/windows/desktop/api/P2P/ns-p2p-peer_contact) 資料結構。                                                                         |
| [**PeerCollabQueryContactData**](/windows/desktop/api/P2P/nf-p2p-peercollabquerycontactdata)                               | 抓取提供的對等端點的連絡人資訊。                                                                                                                               |
| [**PeerCollabRefreshEndpointData**](/windows/desktop/api/P2P/nf-p2p-peercollabrefreshendpointdata)                         | 以新的端點資料更新呼叫的對等節點。                                                                                                                                           |
| [**PeerCollabRegisterApplication**](/windows/desktop/api/P2P/nf-p2p-peercollabregisterapplication)                         | 在本機電腦上註冊應用程式，使其可在對等共同作業活動中啟動。                                                                                   |
| [**PeerCollabRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peercollabregisterevent)                                     | 使用對等共同作業基礎結構註冊應用程式，以接收特定對等共同作業事件的回呼。                                                                |
| [**PeerCollabSetEndpointName**](/windows/desktop/api/P2P/nf-p2p-peercollabsetendpointname)                                 | 設定對等應用程式所使用之目前端點的名稱。                                                                                                                             |
| [**PeerCollabSetObject**](/windows/desktop/api/P2P/nf-p2p-peercollabsetobject)                                             | 建立或更新對等共同作業網路中使用的對等資料物件。                                                                                                                     |
| [**PeerCollabSetPresenceInfo**](/windows/desktop/api/P2P/nf-p2p-peercollabsetpresenceinfo)                                 | 將呼叫者的存在資訊更新為任何監看的連絡人。                                                                                                                          |
| [**PeerCollabSignIn**](/windows/desktop/api/P2P/nf-p2p-peercollabsignin)                                                   | 將對等登入裝載的網際網路 (無伺服器存在) 或子網 ( "近端分享" ) 對等共同作業網路狀態提供者。                                                          |
| [**PeerCollabSignOut**](/windows/desktop/api/P2P/nf-p2p-peercollabsignout)                                                 | 簽署特定類型的對等共同作業網路存在性提供者的對等。                                                                                                            |
| [**PeerCollabShutdown**](/windows/desktop/api/P2P/nf-p2p-peercollabshutdown)                                               | 關閉對等共同作業基礎結構，並釋放任何與其相關聯的資源。                                                                                                 |
| [**PeerCollabStartup**](/windows/desktop/api/P2P/nf-p2p-peercollabstartup)                                                 | 初始化對等共同作業基礎結構。                                                                                                                                              |
| [**PeerCollabSubscribeEndpointData**](/windows/desktop/api/P2P/nf-p2p-peercollabsubscribeendpointdata)                     | 建立可用端點的訂用帳戶。                                                                                                                                                |
| [**PeerCollabUnregisterApplication**](/windows/desktop/api/P2P/nf-p2p-peercollabunregisterapplication)                     | 從本機電腦取消註冊對等的特定應用程式。                                                                                                                        |
| [**PeerCollabUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peercollabunregisterevent)                                 | 從有關特定對等共同作業事件的通知取消註冊應用程式。                                                                                                          |
| [**PeerCollabUnsubscribeEndpointData**](/windows/desktop/api/P2P/nf-p2p-peercollabunsubscribeendpointdata)                 | 移除使用 PeerCollabSubscribeEndpointData 建立之端點的訂用帳戶。                                                                                                             |
| [**PeerCollabUpdateContact**](/windows/desktop/api/P2P/nf-p2p-peercollabupdatecontact)                                     | 使用對等連絡人的新資訊，更新參與對等共同作業網路的對等。                                                                                            |



 

 

 



