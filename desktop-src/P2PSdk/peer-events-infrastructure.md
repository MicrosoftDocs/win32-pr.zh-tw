---
description: 對等基礎結構會使用事件來通知應用程式發生在對等網路內的變更，例如，從圖形新增或移除的節點。
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: 對等事件基礎結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a889f59e4429e64258c047dfbf0249bb4dca125bfc3f9d659e6042dd40be9443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775948"
---
# <a name="peer-events-infrastructure"></a>對等事件基礎結構

對等基礎結構會使用事件來通知應用程式發生在對等網路內的變更，例如，從圖形新增或移除的節點。 對等圖表和對等群組基礎結構會使用對等的事件基礎結構。

## <a name="receiving-peer-event-notification"></a>正在接收對等事件通知

當圖形或群組的屬性變更時，或發生特定的對等事件時，對等可以註冊來接收通知。 對等應用程式會呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) 或 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) 函式，並將事件處理常式傳遞給對等基礎結構，此基礎結構會在先前由 [**CreateEvent**](graphing-reference-links.md)的呼叫所建立。 對等基礎結構會使用控制碼來指示應用程式已發生對等事件。

應用程式也會傳遞一系列的 [**對等 \_ 圖形 \_ 事件 \_ 註冊**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) 或 [**對等 \_ 群組 \_ 事件 \_ 註冊**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) 結構，向對等基礎結構指出應用程式要求通知的特定對等事件。 應用程式也必須明確指定要傳遞的結構數目。

## <a name="peer-graphing-events"></a>對等圖形事件

對等圖形應用程式可以註冊以接收9對等圖形事件的通知。 每個事件名稱前面都會加上 **對等 \_ 圖形 \_ 事件 \_**，例如，**對等 \_ 圖形 \_ 狀態 \_ 已變更**。 除非另有說明，否則會使用 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)抓取變更的相關資訊。

-   **對等 \_圖形 \_ 事件 \_ 狀態 \_ 變更** 表示圖形的狀態已變更，例如節點已與圖形同步處理。
-   **對等 \_\_ \_ \_ 變更 graph 事件屬性** 表示圖形或群組的屬性已變更，例如圖表的易記名稱已變更。
    > [!Note]  
    > 應用程式必須呼叫 [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) 來取得變更的資訊。

     

-   **對等 \_圖形 \_ 事件 \_ 記錄 \_ 變更** 表示記錄已變更，例如刪除記錄。
-   **對等 \_圖形 \_ 事件 \_ 直接 \_ 連接** 指出直接連接已變更，例如節點已連線。
-   **對等 \_圖形 \_ 事件 \_ 鄰近 \_ 連接** 指出連至鄰近節點的連接已變更，例如節點已連線。
-   **對等 \_圖形 \_ 事件 \_ \_** 內送資料表示已從直接或鄰近連接接收資料。
-   **對等 \_\_ \_ \_ 需要 GRAPH 事件連接**，表示圖形基礎結構需要新的連接。
    > [!Note]  
    > 對 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 的呼叫會連接到新的節點。 對 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) 的呼叫不會傳回資料。

     

-   **對等 \_圖形 \_ 事件 \_ 節點 \_ 已變更** 表示節點目前狀態資訊已變更，例如 IP 位址已變更。
-   **對等 \_已 \_ \_ 同步處理的圖表事件** 表示已同步處理特定的記錄類型。

當應用程式收到對等事件發生的通知之後，應用程式會呼叫 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)，並傳遞 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)所傳回的對等事件控制碼。 對等的基礎結構會傳回對 [**等 \_ 圖形 \_ 事件 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) 結構的指標，其中包含所要求的資料。 在 **對等 \_ S \_ 沒有傳回任何 \_ 事件 \_ 資料** 的情況下，應該呼叫這個函數。

應用程式不需要對等事件通知之後，應用程式會呼叫 [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)，並在註冊應用程式時傳遞 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) 所傳回的對等事件控制碼。

## <a name="handling-graph-connection-referrals"></a>處理 Graph 連接參考

當呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 時，連接的對等會透過非同步 **對等 \_ 圖形 \_ 事件 \_ 鄰近 \_ 連接** 事件收到成功或失敗的通知。 如果連接因特定的網路問題而失敗 (例如，防火牆設定錯誤) ，就會引發 **對等 \_ 圖形 \_ 事件 \_ 鄰近 \_ 連接** 事件，並將線上狀態設為「 **對等 \_ 連接 \_ 失敗**」。

不過，當對等嘗試連接到忙碌的節點時，當對等端收到參考時，會在連接的對等上引發 **對等 \_ 圖形 \_ 事件 \_ 相鄰 \_ 連接** ，而連接狀態會設定為 [ **對等 \_ 連接 \_**]。 連接的對等可能會被參考另一個節點，而該節點本身處於忙碌狀態且可能會傳送參考，並且在連接的對等上引發相同的事件和狀態。 導致 **對等 \_ 連接 \_ 失敗** 事件狀態的這一鏈的參考會繼續，直到最大的連線嘗試數目已用盡為止。 對等沒有判斷完整連接嘗試與連接參考之間差異的機制。

若要解決此問題，開發人員應該考慮使用對等圖形狀態變更事件，以判斷連接嘗試是否成功。 如果未在特定時間內收到事件，則應用程式可以假設正在參考連接的對等，而且對等應用程式應該將連線嘗試視為失敗。

## <a name="peer-grouping-events"></a>對等群組事件

對等群組應用程式可以註冊以接收8對等事件的通知。 每個事件名稱前面都會加上 **對等 \_ 群組 \_ 事件 \_**，例如，**對等 \_ 群組 \_ 事件 \_ 狀態 \_ 已變更**。 除非另有說明，否則會使用 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)抓取變更的相關資訊。

-   **對等 \_群組 \_ 事件 \_ 狀態 \_ 變更** 指出群組狀態已變更。 可能有兩個狀態值： **對等 \_ 群組 \_ 狀態 \_ 接聽**，表示群組沒有連線，且正在等候新的成員，而 **對等 \_ 群組 \_ 狀態 \_ 具有連線**，表示群組至少有一個連接。 這個狀態值可以藉由在引發此事件之後呼叫 [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) 來取得。
-   **對等 \_群組 \_ 事件 \_ 屬性已 \_ 變更** 指出群組建立者已變更或更新了群組屬性。
-   **對等 \_群組 \_ 事件 \_ 記錄 \_ 變更** 表示已執行記錄作業。 參與群組的對等發行、更新或刪除記錄時，就會引發此事件。 例如，當聊天應用程式傳送聊天訊息時，就會引發此事件。
-   **對等 \_群組 \_ 事件 \_ 成員 \_ 變更** 指出成員在群組內的狀態已變更。 狀態變更包括：
    -   **對等 \_成員 \_ 已連接**。 對等已連接到群組。
    -   **對等 \_成員已 \_ 中斷** 連線。 對等已與群組中斷連接。
    -   **對等 \_\_加入的成員**。 已針對對等發行新的成員資格資訊。
    -   **對等 \_\_已更新成員**。 對等已更新為新的資訊，例如新的 IP 位址。
-   **對等 \_將 \_ 事件 \_ 鄰居 \_ 連接分組**。 將參與群組內鄰近連接的對等必須註冊此事件。 請注意，註冊這個事件並不會讓對等接收資料;此事件的註冊只會在收到鄰近連接的要求時，確保通知。
-   **對等 \_群組 \_ 事件 \_ 直接 \_ 連接**。 將參與群組內直接連線的對等必須註冊此事件。 請注意，註冊這個事件並不會讓對等接收資料;此事件的註冊只會確保收到直接連線要求時的通知。
-   **對等 \_群組 \_ 事件 \_ \_** 內送資料。 將透過鄰近或直接連接接收資料的對等，必須註冊此事件。 當引發這個事件時，可以藉由呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)來取得其他參與對等互連所傳送的不透明資料。 請注意，若要接收此事件，對等體必須先前已註冊對 **等 \_ 群組 \_ 事件 \_ 直接 \_ 連接** 或 **對等 \_ 群組 \_ 事件 \_ 相鄰 \_ 連接**。
-   **對等 \_群組 \_ 事件 \_ 連接 \_ 失敗**。 連接因某些原因而失敗。 當引發這個事件時，不會提供任何資料，也不應該呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) 。

當應用程式收到發生對等事件的通知之後 (排除 **對等 \_ 群組 \_ 事件 \_ 連接 \_ 失敗**) ，應用程式會呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)，並傳遞 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)所傳回的對等事件控制碼。 對等的基礎結構會傳回 [**對等 \_ 群組 \_ 事件 \_ 資料**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) 結構的指標，其中包含所要求的資料。 必須先呼叫此函式，直到 **對等 \_ S \_ 沒有傳回任何 \_ 事件 \_ 資料** 為止。 當應用程式不再需要對等事件的通知時，必須呼叫 [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent)，然後在應用程式註冊特定事件時，傳遞 **PeerGroupRegisterEvent** 所傳回的對等事件控制碼。

## <a name="example-of-registering-for-peer-graphing-events"></a>註冊對等圖形事件的範例

下列程式碼範例會示範如何向對等圖形事件進行註冊。


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



