---
description: 使用對等圖形時，必須以特定順序呼叫函數。 呼叫的流程取決於您是建立或開啟對等圖形。 本主題指出簡單對等圖形應用程式中函式呼叫的流程。
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: 使用圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975105"
---
# <a name="working-with-graphs"></a>使用圖形

使用對等圖形時，必須以特定順序呼叫函數。 呼叫的流程取決於您是建立或開啟對等圖形。 本主題指出簡單對等圖形應用程式中函式呼叫的流程。

## <a name="starting-up-a-graph"></a>啟動圖形

在應用程式呼叫對等圖形 API 中的函式之前，必須先呼叫 [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) 來初始化應用程式的對等圖形 api，然後設定支援的版本。

## <a name="creating-a-peer-graph"></a>建立對等圖形

下列程式會識別用來建立對等圖形的呼叫流程。

> [!IMPORTANT]
> 只有一個對等應該呼叫 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)。 所有其他對等都應該呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)。 對 **PeerGraphCreate** 的多個呼叫會使圖形失效。

 

-   建立對等圖形。 呼叫 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)。
-   註冊對等事件。 呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。
    > [!Note]  
    > 如需註冊對等事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。

     

-   接聽對等圖形的連接。 呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。
-   針對其餘的執行時間執行與應用程式相依的函式，例如，處理對等事件並使用連接。
-   關閉對等圖形的連接。 呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。

## <a name="opening-a-peer-graph"></a>開啟對等圖形

開啟對等圖形的函式呼叫流程，取決於呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)的傳回值。 最重要的值為 **「 \_ 確定** 」和「 **對等」 \_ \_ 資料 \_ 建立**，如本主題的下列各節所述。

> [!Note]  
> 如果呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 不會傳回所建立的「 **\_ 確定** 」或「 **對等」 \_ \_ 資料 \_**，請處理此錯誤。

 

## <a name="when-peergraphopen-returns-s_ok"></a>當 PeerGraphOpen 傳回 S \_ 正常時

當 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 的呼叫傳回時 **， \_ 對** 等圖形和現有的資料庫也會開啟。 下列程式識別當呼叫 **PeerGraphOpen** 時，您可以如何開啟對等圖形。 **\_**

-   註冊對等事件。 呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。
    > [!Note]  
    > 如需註冊事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。

     

-   找出節點。 這是使用您所識別的方法或應用程式，在對等圖形基礎結構外部執行的進程。 對等圖形 API 不會提供特定的機制來尋找要連接的初始圖形節點。 應用程式必須使用另一種機制，例如 [ (PNRP) API 的對等名稱解析通訊協定 ](pnrp-namespace-provider-api.md) ，以找出初始節點。
-   如果找到節點，請連接到該節點。 呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)，然後呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) 接聽對等圖形的連接。
    > [!Note]  
    > 如果找不到節點，請勿呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 和 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。

     

-   針對執行時間的其餘部分執行應用程式相依的函式，例如，處理對等事件和使用連接，視節點是否連接至對等圖形而定。 例如，應用程式可以選擇為圖形中的作用中節點設定 timeout 或定期執行探索。
-   關閉對等圖形的連接。 呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>當 PeerGraphOpen 傳回所建立的對等 \_ \_ 資料時 \_

當 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 傳回 **所 \_ \_ \_ 建立的對等資料** 時，表示找不到對等圖形的現有資料庫、建立新的資料庫，這是第一次開啟時。 若要在對等圖形上使用或接聽，對等必須連接至對等圖形並與其同步。

下列程式識別當呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) 傳回所 **\_ \_ \_ 建立的對等資料** 時，您可以執行的動作。

-   開啟對等圖形。 呼叫 [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)。
-   註冊對等事件。 呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)。
    > [!Note]  
    > 如需註冊對等事件的詳細資訊，請參閱 [事件基礎結構](peer-events-infrastructure.md)。

     

-   找出節點。 這是使用您所識別的方法或應用程式，在對等圖形基礎結構外部執行的進程。 對等圖形 API 不會提供特定的機制來尋找要連接的初始圖形節點。 應用程式必須使用另一種機制，例如 [ (PNRP) API 的對等名稱解析通訊協定 ](pnrp-namespace-provider-api.md) ，以找出初始節點。
-   如果找到節點，請連接到該節點。 呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)，然後呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) 接聽對等圖形的連接。
    > [!Note]  
    > 如果找不到節點，請勿呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 和 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)。

     

-   針對執行時間的其餘部分執行應用程式相依的函式，例如，處理對等事件和使用連接，視節點是否連接至對等圖形而定。 例如，應用程式可以選擇為圖形中的作用中節點設定 timeout 或定期執行探索。
-   關閉對等圖形的連接。 呼叫 [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)。

 

 



