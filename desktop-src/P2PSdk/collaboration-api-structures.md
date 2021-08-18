---
description: 下列結構支援對等共同作業功能。StructureDescriptionPEER \_ APPLICATIONContains 資料，描述可在對等共同作業網路內，向受信任的連絡人註冊並共用的本機安裝軟體應用程式或元件。對等 \_ 應用程式 \_ 註冊 \_ INFOContains 對等應用程式資訊，以向本機電腦註冊。對等應用程式 \_ \_ 啟動 \_ INFOContains 上一個對等邀請要求中的連絡人提供的對等應用程式啟動資訊。對等 \_ collaboration \_ 事件會 \_ 針對對等上引發的每個可能對等共同作業網路事件 DATAContains 變異資料。對等 \_ collaboration \_ 事件 \_ REGISTRATIONContains 對等的資料，用來註冊特定的對等共同作業網路事件。對等 \_ CONTACTContains 特定連絡人的相關資訊。對等 \_ ENDPOINTContains 對等端點的位址和易記名稱。對 \_ 等 \_ 人們 \_ MEContains 相同邏輯或虛擬子網中的對等資訊。對等事件 \_ \_ 應用程式 \_ 已變更 \_ 當對等 \_ 事件 \_ 端點 \_ 應用程式 \_ 已變更或對等 \_ 事件 \_ 我的 \_ 應用程式 \_ 已變更事件在參與對等共同作業網路的對等上引發時，所傳回的 DATAContains 資訊對等事件 \_ \_ 端點變更 \_ \_ 了當對等事件 \_ \_ 端點 \_ 變更或對等 \_ 事件「 \_ 我 \_ 的端點變更」事件在 \_ 參與對等共同作業網路的對等上引發時，所傳回的 DATAContains 資訊。對等事件 \_ \_ 物件已 \_ 變更 \_ DATAContains 當對等 \_ 事件 \_ 端點 \_ 物件 \_ 已變更或對等 \_ 事件的 \_ \_ 物件 \_ 變更事件時，所傳回的資訊會在參與對等共同作業網路的對等上引發。\_近端的對等事件 \_ 變更了 \_ \_ \_ \_ DATAContains 資訊。當對等 \_ 事件「近端分享」事件 \_ \_ \_ \_ 是在參與子網特定對等共同作業網路的對等上引發時所傳回的資訊。對等事件目前狀態已變更 \_ \_ \_ \_ DATAContains 當對等 \_ 事件端點的 \_ \_ 狀態 \_ 已變更或對等的 \_ 事件 \_ \_ \_ ，在參與對等共同作業網路的對等上引發變更時所傳回的資訊。對等 \_ 事件 \_ 要求狀態已 \_ 變更 DATAContains 當對等共同作業網路中的對等 \_ \_ \_ ，引發對等事件 \_ 要求 \_ 狀態 \_ 變更事件時所傳回的資訊。當對等共同作業 \_ \_ \_ \_ \_ \_ \_ 網路的對等上引發對等事件關注清單變更事件時，對等事件關注清單已變更的 DATAContains 資訊。對等 \_ INVITATIONContains 起始或加入對等共同作業活動的要求。對等 \_ 邀請 \_ 回應：邀請加入對等共同作業活動。對等 \_ 物件包含應用程式特定的執行時間資訊，可與對等共同作業網路內的受信任連絡人共用。對等 \_ 狀態 \_ INFOContains 特定的對等狀態資訊。
ms.assetid: 2634899c-3263-45ce-9fac-407e11e42cd4
title: 協同作業 API 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa003702b9d42202bf344f6e512a1ca42d90a2ced701dc327fdc91eefb8fdcb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011756"
---
# <a name="collaboration-api-structures"></a>協同作業 API 結構

下列結構支援對等共同作業功能。

| 結構                                                                                      | 描述                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**對等 \_ 應用程式**](/windows/desktop/api/P2P/ns-p2p-peer_application)                                                  | 包含描述本機安裝軟體應用程式或元件的資料，該應用程式或元件可在對等共同作業網路內與受信任的連絡人註冊並共用。                        |
| [**對等 \_ 應用程式 \_ 註冊 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_application_registration_info)            | 包含在本機電腦上註冊的對等應用程式資訊。                                                                                                                    |
| [**對等 \_ 應用程式 \_ 啟動 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_app_launch_info)                                        | 包含前一個對等邀請要求中的連絡人所提供的對等應用程式啟動資訊。                                                                              |
| [**PEER_COLLAB_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_collab_event_data-r1)                                    | 包含對等上引發之每個可能對等共同作業網路事件的變異數資料。                                                                                                         |
| [**對等 \_ COLLABORATION \_ 事件 \_ 註冊**](/windows/desktop/api/P2P/ns-p2p-peer_collab_event_registration)                    | 包含對等互連用來註冊特定對等共同作業網路事件的資料。                                                                                                       |
| [**對等 \_ 連絡人**](/windows/desktop/api/P2P/ns-p2p-peer_contact)                                                          | 包含特定連絡人的相關資訊。                                                                                                                                                     |
| [**對等 \_ 端點**](/windows/desktop/api/P2P/ns-p2p-peer_endpoint)                                                        | 包含對等端點的位址和易記名稱。                                                                                                                                         |
| [**近端對等 \_ 人 \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_people_near_me)                                          | 包含相同邏輯或虛擬子網中對等的相關資訊。                                                                                                                           |
| [**對等 \_ 事件 \_ 應用程式 \_ 已變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_application_changed_data)         | 包含當對等共同作業網路的對等互連時，對等事件 \_ \_ 端點 \_ 應用程式 \_ 變更或對等 \_ 事件 \_ 我 \_ 的應用程式 \_ 變更事件時所傳回的資訊。 |
| [**對等 \_ 事件 \_ 端點 \_ 已變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_endpoint_changed_data)               | 包含當對等 \_ 事件 \_ 端點 \_ 變更或對等 \_ 事件「 \_ 我 \_ \_ 的端點變更」事件在參與對等共同作業網路的對等上引發時，所傳回的資訊。                 |
| [**對等 \_ 事件 \_ 物件 \_ 已變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_object_changed_data)                   | 包含當對等 \_ 事件 \_ 端點 \_ 物件 \_ 已變更或對等 \_ 事件「 \_ 我的 \_ 物件 \_ 已變更」事件在參與對等共同作業網路的對等上引發時，所傳回的資訊。           |
| [**對等的 \_ 活動分享 \_ \_ \_ \_ 資料已變更 \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_people_near_me_changed_data) | 包含在 \_ \_ \_ \_ \_ 參與子網特定對等共同作業網路的對等上引發事件時，所傳回的資訊。                               |
| [**對等 \_ 事件 \_ 狀態 \_ 變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_presence_changed_data)               | 包含在 \_ \_ \_ \_ \_ \_ \_ \_ 參與對等共同作業網路的對等上，當對等事件端點狀態變更或對等事件的「我的目前狀態變更」事件時所傳回的資訊。       |
| [**對等 \_ 事件 \_ 要求 \_ 狀態 \_ 已變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_request_status_changed_data)  | 包含在 \_ \_ \_ \_ 參與對等共同作業網路的對等上引發對等事件要求狀態變更事件時所傳回的資訊。                                                |
| [**對等 \_ 事件 \_ 關注清單 \_ 已變更 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_event_watchlist_changed_data)             | 包含在 \_ \_ \_ 參與對等共同作業網路的對等上引發對等事件關注清單變更事件時所傳回的資訊。                                                      |
| [**對等 \_ 邀請**](/windows/desktop/api/P2P/ns-p2p-peer_invitation)                                                    | 包含起始或加入對等共同作業活動的要求。                                                                                                                              |
| [**對等 \_ 邀請 \_ 回應**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_response)                                 | 邀請加入對等共同作業活動的回應。                                                                                                                                 |
| [**對等 \_ 物件**](/windows/desktop/api/P2P/ns-p2p-peer_object)                                                            | 包含應用程式特定的執行時間資訊，可與對等共同作業網路內的受信任連絡人共用。                                                                   |
| [**對等 \_ 狀態 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_presence_info)                                             | 包含特定的對等存在資訊。                                                                                                                                                       |



 

 

 



