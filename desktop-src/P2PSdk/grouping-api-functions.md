---
description: 群組 API 會使用下列功能：
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: 群組 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976904"
---
# <a name="grouping-api-functions"></a>群組 API 函數

群組 API 會使用下列功能：

## <a name="group-initialization-and-cleanup-functions"></a>群組初始化和清除函數



| 函式                                       | 描述                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | 關閉使用 [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) 所建立的對等群組，並處置任何已配置的資源。 |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | 使用要求的對等基礎結構版本，初始化對等群組。                                        |



 

## <a name="group-creation-and-access-functions"></a>群組建立和存取功能



| 函式                                                                       | 描述                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | 使先前呼叫 [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)、 [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)或 [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) 函數所取得的對等群組控制碼失效。 |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | 初始化對等群組的 PNRP 搜尋，並嘗試連接到該群組。 成功呼叫這個函式之後，對等可以與對等群組的其他成員進行通訊。                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | 嘗試連接到具有已知 IPv6 位址的其他對等群組。                                                                                                       |
| [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | 建立新的對等群組。                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | 傳回可供指定的對等聯結群組的 XML 字串。                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | 傳回 XML 字串，這個字串可供指定的對等聯結使用相符密碼的群組。                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | 刪除與對等群組相關聯的本機資料和憑證。                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | 抓取群組的目前狀態。                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | 將認證（包括 GMC）發行至特定身分識別，並選擇性地傳回受邀的對等互連可用於加入對等群組的邀請 XML 字串。                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | 允許對等的邀請加入現有的對等群組。                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | 開啟對等互連已建立或聯結的對等群組。                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | 傳回 [**對等 \_ 邀請 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) 結構，其中包含特定邀請的詳細資料。                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | 允許對等具有邀請和正確的密碼，以聯結受密碼保護的對等群組。                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>群組和成員資訊函數



| 函式                                                 | 描述                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | 建立可用對等群組成員的列舉，以及相關聯的成員資格資訊。                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | 抓取指定群組之屬性的資訊。                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | 設定目前的對等群組屬性。 在此 API 的1.0 版中，只有對等群組的建立者可以執行這項作業。 |



 

## <a name="records-and-record-management-functions"></a>記錄和記錄管理功能



| 函式                                                 | 描述                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | 將新記錄加入至對等群組，此群組會傳播到所有參與的對等群組。 |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | 從對等群組刪除記錄。 只有記錄的建立者可以將其刪除。      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | 建立對等群組記錄的列舉。                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | 抓取特定的群組記錄。                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | 搜尋本機對等群組資料庫中是否有符合所提供準則的記錄。 |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | 更新特定對等群組內的記錄。                                       |



 

## <a name="group-database-importexport-functions"></a>群組資料庫匯入/匯出函數



| 函式                                                   | 描述                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | 將對等群組資料庫匯出至特定檔案，該檔案可以傳輸到另一部電腦，並使用 [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) 函式匯入。 |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | 從本機檔案匯入對等群組資料庫。                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>直接連接函數



| 函式                                                                 | 描述                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | 關閉兩個對等之間的特定直接連接。              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | 建立目前對等的作用中連接的列舉。 |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | 在對等群組中建立與另一個對等的直接連接。  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | 透過鄰近或直接連線將資料傳送至成員。        |



 

## <a name="group-events-infrastructure"></a>群組事件基礎結構



| 函式                                                     | 描述                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | 允許應用程式取出群組事件所傳回的資料。                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | 針對特定的對等群組事件註冊對等。                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | 從與提供的事件控制碼相關聯的對等事件的通知中取消註冊對等。 |



 

## <a name="group-time-conversion-functions"></a>群組時間轉換函數



| 函式                                                                     | 描述                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | 將對等群組維護的參考時間值轉換成適合在對等電腦上顯示的當地語系化時間值。 |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | 將本機時間值從對等電腦轉換為一般對等群組時間值。                                         |



 

## <a name="group-configuration-functions"></a>群組設定函數



| 函式                                               | 描述                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | 將對等的群組設定匯出為 XML 字串，其中包含身分識別、組名和身分識別的 GMC。 |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | 根據提供的 XML 設定字串中的特定設定，匯入身分識別的對等群組設定。         |



 

 

 



