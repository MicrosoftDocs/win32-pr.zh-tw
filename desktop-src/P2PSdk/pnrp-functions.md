---
description: PNRP 命名空間提供者 API 會使用下列函數。
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: PNRP 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979156"
---
# <a name="pnrp-functions"></a>PNRP 函數

PNRP 命名空間提供者 API 會使用下列函數。



| 函式                                                             | 描述                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | 將提供的對等名稱編碼為可搭配後續呼叫 [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows 通訊端函式使用的格式。 |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | 將 [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) 傳回的主機名稱解碼成它所代表的對等名稱字串。                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | 啟動呼叫端的對等名稱解析通訊協定 (PNRP) 服務。                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | 關閉執行中的對等名稱解析通訊協定實例 (PNRP) 服務，並釋放與其相關聯的所有資源。                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | 使用 PNRP 雲端註冊對等，並傳回可用於註冊更新的控制碼。                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | 更新名稱的 PNRP 註冊資訊。                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | 從 PNRP 雲端取消註冊對等。                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | 針對特定的對等名稱，取得 (es) 註冊的端點位址。                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | 開始非同步對等名稱解析作業。                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | 抓取呼叫端所參與之對等名稱解析通訊協定 (PNRP) 雲端的相關資訊。                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | 關閉使用先前的 [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)呼叫所起始的非同步 PNRP 解析作業的控制碼。      |
| [PNRP 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | 啟動可讓應用程式解析名稱和列舉網路雲端的進程。                                                                 |
| [PNRP 和 WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | 終止在先前呼叫 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)時起始的查詢。                                             |
| [PNRP 和 WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | 符合先前呼叫 [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)所指定的查詢。                                                |
| [PNRP 和 WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | 接收網路雲端清單變更的相關通知，以及名稱解析要求的結果可用性。                                     |
| [PNRP 和 WSASetService](pnrp-and-wsasetservice.md)                 | 註冊或移除 [對等名稱](peer-names.md)。                                                                                                           |



 

 

 
