---
description: 對等圖表和對等群組基礎結構可讓應用程式直接連接到一個節點 (圖形) 或成員 (群組) ，然後直接與節點交換資料。 此連接稱為直接連接。
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: 直接連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983499"
---
# <a name="direct-connections"></a>直接連接

對等圖表和對等群組基礎結構可讓應用程式直接連接到一個節點 (圖形) 或成員 (群組) ，然後直接與節點交換資料。 此連接稱為 **直接連接**。

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>使用對等圖形基礎結構的直接連接

在圖形中的兩個節點之間建立直接連線之前，這兩個節點都必須針對 **對等 \_ 圖形 \_ 事件 \_ 直接 \_ 連接** 事件進行註冊。 若要透過直接連接接收資料，也必須針對 **對等 \_ 圖形 \_ 事件 \_ 傳入 \_ 資料** 事件註冊節點。

**對等 \_GRAPH \_ 事件 \_ 直接 \_** 連線是一種事件，會通知應用程式是否有直接連接嘗試成功或失敗。 [**對等 \_ 圖形 \_ 事件 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data)結構中會傳回對 [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)呼叫的實際成功或失敗狀態。

若要建立直接連線，應用程式會呼叫 [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)，然後將控制碼傳遞給圖形、參與連接之另一個節點的身分識別指標，以及參與節點的 IPv6 位址結構指標。 在 **PeerGraphOpenDirectConnection** 的呼叫中指定的節點身分識別和 IPv6 位址必須針對 **對等 \_ 圖形事件內送 \_ \_ \_ 資料** 事件進行註冊，否則無法接收由呼叫端傳送的資料。 成功時， **PeerGraphOpenDirectConnection** 會傳回64位的連接識別碼。 但是，對等 **\_ 群組 \_ 事件 \_ 直接 \_ 連接** 事件必須等到直接連線識別碼可以識別為有效的情況。

建立連線並確認有效的連接識別碼之後，應用程式可以呼叫 [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) ，以透過有效連接識別碼所指定的連接，將資料傳送到參與的對等互連-如果參與對等 **\_ 圖形事件內送 \_ \_ \_ 資料** 事件已註冊。 不透明的資料會以對等的資料結構形式提供給對等 **\_ 圖形 \_ 事件 \_ 傳入 \_ 資料** 事件 [**所傳回的對等 \_ \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) [**\_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_data)結構。

當不需要連線時，應用程式會以圖形控制碼和連接識別碼呼叫 [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) 。

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>使用對等群組基礎結構的直接連接

對等群組基礎結構內的直接連接會以類似于對等圖形基礎結構的方式處理。

在群組中的兩個成員之間可以建立直接連線之前，這兩個成員都必須註冊對 **等 \_ 群組 \_ 事件 \_ 直接 \_ 連接** 事件。 如果群組成員想要透過直接連接接收資料，群組成員也必須註冊對 **等群組事件內送 \_ \_ \_ \_ 資料** 事件。

**對等 \_群組 \_ 事件 \_ 直接 \_** 連線是一種事件，它會通知應用程式是否有直接連接嘗試成功或失敗。 [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)呼叫的實際成功或失敗狀態會在 [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1)結構中傳回。

若要建立直接連線，應用程式會呼叫 [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)，然後將控制碼傳遞給群組、將參與此連接之另一個成員的身分識別指標，以及參與成員的 IPv6 位址結構指標。 在 **PeerGroupOpenDirectConnection** 的呼叫中指定的身分識別和 IPv6 位址的成員，必須針對 **對等群組事件內送 \_ \_ \_ \_ 資料** 事件進行註冊，否則成員無法接收呼叫端所傳送的資料。 成功時， **PeerGroupOpenDirectConnection** 會傳回64位的連接識別碼。 但是，對等必須等待對 **等 \_ 圖形 \_ 事件 \_ 直接 \_ 連接** 事件，才能將直接連接識別碼識別為有效。

在建立連接並確認有效的連接識別碼之後，應用程式就可以呼叫 [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) ，以將資料傳送至參與對等互連的有效連接識別碼所指定的連接，如果參與對等 **群組事件的內送 \_ \_ \_ \_ 資料** 事件已註冊。 在對等 **\_ 群組事件內送 \_ \_ \_ 資料** 事件所傳回的對等 [**\_ 事件 \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)內送資料中，不透明資料會以 [**對等 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_data)結構的形式提供。

當不需要連線時，應用程式會使用群組控制碼和連線識別碼來呼叫 [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) 。

## <a name="example-of-a-direct-connection-for-graphing"></a>圖形直接連接的範例


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



