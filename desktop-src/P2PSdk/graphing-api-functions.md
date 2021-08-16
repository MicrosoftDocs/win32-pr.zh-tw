---
description: 對等圖形 API 使用下列功能：
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: 圖形 API 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26c40770e8fcbc18b08ccb73dcfea5f1f6c4eab65be615ed76d8088ddc90954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776218"
---
# <a name="graphing-api-functions"></a>圖形 API 函數

對等圖形 API 使用下列功能：

## <a name="initialization-and-cleanup-functions"></a>初始化和清除函數



| 函式                                       | 描述                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | 清除呼叫 [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)所配置的任何資源。                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | 向對等圖形基礎結構指出呼叫應用程式所需的對等通訊協定版本。 |



 

## <a name="graph-creation-and-access-functions"></a>Graph建立和存取函式



| 函式                                   | 描述                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | 使對 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) 或 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)的呼叫所傳回的對等圖形控制碼失效，並關閉指定之對等圖表的所有網路連接。 |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | 建立新的對等圖形。                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | 刪除與指定之對等圖形相關聯的資料。                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | 表示對等圖形應開始接聽傳入連接。                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | 開啟先前由本機節點或遠端節點所建立的對等圖形。                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Graph 和節點資訊函數



| 函式                                                         | 描述                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | 建立並傳回列舉控制碼，用來列舉對等圖形中的節點。                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | 抓取特定節點的相關資訊。                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | 抓取目前的對等圖形屬性。                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | 傳回對等圖形的目前狀態。                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | 設定本機節點的 [**對等 \_ 節點 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) 結構的屬性。                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | 明確開啟或關閉特定節點的狀態記錄發行集。 此函數可以覆寫對等圖形屬性中的存在性設定。 |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | 設定對等圖形屬性。                                                                                                                                    |



 

## <a name="record-management-functions"></a>記錄管理功能



| 函式                                                                     | 描述                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | 將新記錄加入至對等圖形。 使用此函式加入的記錄會傳送到對等圖形中的每個節點。                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | 將記錄標示為在對等圖形內刪除。                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | 建立並傳回列舉控制碼，這個控制碼可用來列舉特定記錄類型的記錄、使用者或兩者的記錄。                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | 根據指定的記錄識別碼抓取特定記錄。                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | 在對等圖形中搜尋特定記錄。                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | 更新對等圖形中的記錄，然後將記錄氾濫至對等圖形中的每個節點。                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | 向對等圖形基礎結構表示要重新提交任何安全性模組的延遲記錄以進行驗證。 |



 

## <a name="export-and-import-functions"></a>匯出和匯入函式



| 函式                                                   | 描述                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | 將對等圖形資料庫匯出至可移至不同電腦的檔案。 |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | 從對等圖形資料庫匯入包含資訊的檔案。             |



 

## <a name="utility-and-support-functions"></a>公用程式和支援功能



| 函式                                                                     | 描述                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | 釋放列舉控制碼，並釋出與列舉相關聯的資源。                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | 釋出數個對等圖形 API 函數傳回的資源。                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | 捕獲列舉中的專案數。                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | 取得列舉型別中的下一個專案，也就是呼叫特定函式所建立的專案，傳回對等列舉。        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | 將對等圖表維護的參考時間值轉換為適當的當地語系化時間值，以便顯示在對等電腦上。 |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | 將來自對等電腦的通用時間值轉換為一般對等圖形時間值。                                       |



 

## <a name="connection-functions"></a>連接函數



| 函式                                                                 | 描述                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | 關閉指定的直接連接。                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | 嘗試建立對等圖形中指定節點的連接。 此函數會啟動非同步作業。                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | 建立並傳回用來列舉本機節點之連接的列舉控制碼。                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | 允許應用程式與對等圖形中的節點建立直接連接。 只有當應用程式所連接的節點已訂閱 **對等 \_ 圖形 \_ 事件 \_ 直接 \_** 線上活動時，才能建立連接。 |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | 將資料傳送至鄰近節點或直接連接的節點。                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>事件基礎結構函數



| 函式                                                     | 描述                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | 抓取對等事件。                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | 註冊對等圖形和事件種類相關聯之變更的通知對等要求。            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | 要求應用程式不會再收到與對等圖表和記錄類型相關聯之變更的通知。 |



 

 

 



