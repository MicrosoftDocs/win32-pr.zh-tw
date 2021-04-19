---
description: 對等基礎結構會使用事件來通知應用程式發生在對等網路內的變更，例如，從圖形新增或移除的節點。
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: 對等事件基礎結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971801"
---
# <a name="peer-events-infrastructure"></a><span data-ttu-id="33c51-103">對等事件基礎結構</span><span class="sxs-lookup"><span data-stu-id="33c51-103">Peer Events Infrastructure</span></span>

<span data-ttu-id="33c51-104">對等基礎結構會使用事件來通知應用程式發生在對等網路內的變更，例如，從圖形新增或移除的節點。</span><span class="sxs-lookup"><span data-stu-id="33c51-104">The Peer Infrastructure uses events to notify applications of changes that have occurred within a peer network, for example, a node that is added or removed from a graph.</span></span> <span data-ttu-id="33c51-105">對等圖表和對等群組基礎結構會使用對等的事件基礎結構。</span><span class="sxs-lookup"><span data-stu-id="33c51-105">The Peer Graphing and Peer Grouping Infrastructures use the peer events infrastructure.</span></span>

## <a name="receiving-peer-event-notification"></a><span data-ttu-id="33c51-106">正在接收對等事件通知</span><span class="sxs-lookup"><span data-stu-id="33c51-106">Receiving Peer Event Notification</span></span>

<span data-ttu-id="33c51-107">當圖形或群組的屬性變更時，或發生特定的對等事件時，對等可以註冊來接收通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-107">A peer can register to receive notification when an attribute of a graph or group changes, or a specific peer event occurs.</span></span> <span data-ttu-id="33c51-108">對等應用程式會呼叫 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) 或 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) 函式，並將事件處理常式傳遞給對等基礎結構，此基礎結構會在先前由 [**CreateEvent**](graphing-reference-links.md)的呼叫所建立。</span><span class="sxs-lookup"><span data-stu-id="33c51-108">A peer application calls the [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) or [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) function, and passes an event handle to the Peer Infrastructure, which is created previously by a call to [**CreateEvent**](graphing-reference-links.md).</span></span> <span data-ttu-id="33c51-109">對等基礎結構會使用控制碼來指示應用程式已發生對等事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-109">The Peer Infrastructure uses the handle to signal an application that a peer event has occurred.</span></span>

<span data-ttu-id="33c51-110">應用程式也會傳遞一系列的 [**對等 \_ 圖形 \_ 事件 \_ 註冊**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) 或 [**對等 \_ 群組 \_ 事件 \_ 註冊**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) 結構，向對等基礎結構指出應用程式要求通知的特定對等事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-110">The application also passes a series of [**PEER\_GRAPH\_EVENT\_REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) or [**PEER\_GROUP\_EVENT\_REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) structures that indicate to the Peer Infrastructure the specific peer events for which the application is requesting notification.</span></span> <span data-ttu-id="33c51-111">應用程式也必須明確指定要傳遞的結構數目。</span><span class="sxs-lookup"><span data-stu-id="33c51-111">The application must also specify exactly how many structures are being passed.</span></span>

## <a name="peer-graphing-events"></a><span data-ttu-id="33c51-112">對等圖形事件</span><span class="sxs-lookup"><span data-stu-id="33c51-112">Peer Graphing Events</span></span>

<span data-ttu-id="33c51-113">對等圖形應用程式可以註冊以接收9對等圖形事件的通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-113">A Peer Graphing application can register to receive notification for 9 peer graph events.</span></span> <span data-ttu-id="33c51-114">每個事件名稱前面都會加上 **對等 \_ 圖形 \_ 事件 \_**，例如，**對等 \_ 圖形 \_ 狀態 \_ 已變更**。</span><span class="sxs-lookup"><span data-stu-id="33c51-114">Each event name is prefaced with **PEER\_GRAPH\_EVENT\_**, for example, **PEER\_GRAPH\_STATUS\_CHANGED**.</span></span> <span data-ttu-id="33c51-115">除非另有說明，否則會使用 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)抓取變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33c51-115">Unless otherwise noted, information about a change is retrieved by using [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).</span></span>

-   <span data-ttu-id="33c51-116">**對等 \_圖形 \_ 事件 \_ 狀態 \_ 變更** 表示圖形的狀態已變更，例如節點已與圖形同步處理。</span><span class="sxs-lookup"><span data-stu-id="33c51-116">**PEER\_GRAPH\_EVENT\_STATUS\_CHANGED** indicates that the status of a graph is changed, for example, a node has synchronized with a graph.</span></span>
-   <span data-ttu-id="33c51-117">**對等 \_\_ \_ \_ 變更 graph 事件屬性** 表示圖形或群組的屬性已變更，例如圖表的易記名稱已變更。</span><span class="sxs-lookup"><span data-stu-id="33c51-117">**PEER\_GRAPH\_EVENT\_PROPERTY\_CHANGED** indicates that a property of a graph or group is changed, for example, the friendly name of a graph has changed.</span></span>
    > [!Note]  
    > <span data-ttu-id="33c51-118">應用程式必須呼叫 [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) 來取得變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="33c51-118">The application must call [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) to obtain the changed information.</span></span>

     

-   <span data-ttu-id="33c51-119">**對等 \_圖形 \_ 事件 \_ 記錄 \_ 變更** 表示記錄已變更，例如刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="33c51-119">**PEER\_GRAPH\_EVENT\_RECORD\_CHANGED** indicates that a record is changed, for example, a record is deleted.</span></span>
-   <span data-ttu-id="33c51-120">**對等 \_圖形 \_ 事件 \_ 直接 \_ 連接** 指出直接連接已變更，例如節點已連線。</span><span class="sxs-lookup"><span data-stu-id="33c51-120">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** indicates that a direct connection is changed, for example, a node has connected.</span></span>
-   <span data-ttu-id="33c51-121">**對等 \_圖形 \_ 事件 \_ 鄰近 \_ 連接** 指出連至鄰近節點的連接已變更，例如節點已連線。</span><span class="sxs-lookup"><span data-stu-id="33c51-121">**PEER\_GRAPH\_EVENT\_NEIGHBOR\_CONNECTION** indicates that a connection to a neighbor node is changed, for example, a node has connected.</span></span>
-   <span data-ttu-id="33c51-122">**對等 \_圖形 \_ 事件 \_ \_** 內送資料表示已從直接或鄰近連接接收資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-122">**PEER\_GRAPH\_EVENT\_INCOMING\_DATA** indicates that data has been received from a direct or neighbor connection.</span></span>
-   <span data-ttu-id="33c51-123">**對等 \_\_ \_ \_ 需要 GRAPH 事件連接**，表示圖形基礎結構需要新的連接。</span><span class="sxs-lookup"><span data-stu-id="33c51-123">**PEER\_GRAPH\_EVENT\_CONNECTION\_REQUIRED** indicates that the Graphing Infrastructure requires a new connection.</span></span>
    > [!Note]  
    > <span data-ttu-id="33c51-124">對 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 的呼叫會連接到新的節點。</span><span class="sxs-lookup"><span data-stu-id="33c51-124">A call to [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) connects to a new node.</span></span> <span data-ttu-id="33c51-125">對 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) 的呼叫不會傳回資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-125">A call to [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) does not return data.</span></span>

     

-   <span data-ttu-id="33c51-126">**對等 \_圖形 \_ 事件 \_ 節點 \_ 已變更** 表示節點目前狀態資訊已變更，例如 IP 位址已變更。</span><span class="sxs-lookup"><span data-stu-id="33c51-126">**PEER\_GRAPH\_EVENT\_NODE\_CHANGED** indicates that node presence information is changed, for example, an IP address has changed.</span></span>
-   <span data-ttu-id="33c51-127">**對等 \_已 \_ \_ 同步處理的圖表事件** 表示已同步處理特定的記錄類型。</span><span class="sxs-lookup"><span data-stu-id="33c51-127">**PEER\_GRAPH\_EVENT\_SYNCHRONIZED** indicates that a specific record type is synchronized.</span></span>

<span data-ttu-id="33c51-128">當應用程式收到對等事件發生的通知之後，應用程式會呼叫 [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)，並傳遞 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)所傳回的對等事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="33c51-128">After an application receives notification that a peer event has occurred, the application calls [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata), and passes the peer event handle returned by [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).</span></span> <span data-ttu-id="33c51-129">對等的基礎結構會傳回對 [**等 \_ 圖形 \_ 事件 \_ 資料**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) 結構的指標，其中包含所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-129">The Peer Infrastructure returns a pointer to a [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure that contains the requested data.</span></span> <span data-ttu-id="33c51-130">在 **對等 \_ S \_ 沒有傳回任何 \_ 事件 \_ 資料** 的情況下，應該呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="33c51-130">This function should be called until **PEER\_S\_NO\_EVENT\_DATA** is returned.</span></span>

<span data-ttu-id="33c51-131">應用程式不需要對等事件通知之後，應用程式會呼叫 [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)，並在註冊應用程式時傳遞 [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) 所傳回的對等事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="33c51-131">After an application does not require a peer event notification, the application calls either [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent), and passes the peer event handle returned by [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) when the application registered.</span></span>

## <a name="handling-graph-connection-referrals"></a><span data-ttu-id="33c51-132">處理圖形連接參考</span><span class="sxs-lookup"><span data-stu-id="33c51-132">Handling Graph Connection Referrals</span></span>

<span data-ttu-id="33c51-133">當呼叫 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) 時，連接的對等會透過非同步 **對等 \_ 圖形 \_ 事件 \_ 鄰近 \_ 連接** 事件收到成功或失敗的通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-133">When [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) is called, the connecting peer is notified of success or failure through the asynchronous **PEER\_GRAPH\_EVENT\_NEIGHBOR\_CONNECTION** event.</span></span> <span data-ttu-id="33c51-134">如果連接因特定的網路問題而失敗 (例如，防火牆設定錯誤) ，就會引發 **對等 \_ 圖形 \_ 事件 \_ 鄰近 \_ 連接** 事件，並將線上狀態設為「 **對等 \_ 連接 \_ 失敗**」。</span><span class="sxs-lookup"><span data-stu-id="33c51-134">If the connection failed due to a specific networking issues (such as a misconfigured firewall), the **PEER\_GRAPH\_EVENT\_NEIGHBOR\_CONNECTION** event is raised, with the connection status set to **PEER\_CONNECTION\_FAILED**.</span></span>

<span data-ttu-id="33c51-135">不過，當對等嘗試連接到忙碌的節點時，當對等端收到參考時，會在連接的對等上引發 **對等 \_ 圖形 \_ 事件 \_ 相鄰 \_ 連接** ，而連接狀態會設定為 [ **對等 \_ 連接 \_**]。</span><span class="sxs-lookup"><span data-stu-id="33c51-135">However, when a peer receives a referral when it attempts to connect to a busy node, the **PEER\_GRAPH\_EVENT\_NEIGHBOR\_CONNECTION** is raised on the connecting peer, with the connection status set to **PEER\_CONNECTION\_FAILED**.</span></span> <span data-ttu-id="33c51-136">連接的對等可能會被參考另一個節點，而該節點本身處於忙碌狀態且可能會傳送參考，並且在連接的對等上引發相同的事件和狀態。</span><span class="sxs-lookup"><span data-stu-id="33c51-136">The connecting peer may be referred to another node which itself is busy and may send a referral, and the same event and status are raised on the connecting peer.</span></span> <span data-ttu-id="33c51-137">導致 **對等 \_ 連接 \_ 失敗** 事件狀態的這一鏈的參考會繼續，直到最大的連線嘗試數目已用盡為止。</span><span class="sxs-lookup"><span data-stu-id="33c51-137">This chain of referrals that result in **PEER\_CONNECTION\_FAILED** event statuses can continue until the maximum number of connection attempts has been exhausted.</span></span> <span data-ttu-id="33c51-138">對等沒有判斷完整連接嘗試與連接參考之間差異的機制。</span><span class="sxs-lookup"><span data-stu-id="33c51-138">The peer does not have a mechanism to determine the difference between a full connection attempt and the connection referral.</span></span>

<span data-ttu-id="33c51-139">若要解決此問題，開發人員應該考慮使用對等圖形狀態變更事件，以判斷連接嘗試是否成功。</span><span class="sxs-lookup"><span data-stu-id="33c51-139">To address this issue, developers should consider using the peer graph status change events to determine if the connection attempt suceeded.</span></span> <span data-ttu-id="33c51-140">如果未在特定時間內收到事件，則應用程式可以假設正在參考連接的對等，而且對等應用程式應該將連線嘗試視為失敗。</span><span class="sxs-lookup"><span data-stu-id="33c51-140">If the event is not received within a specific amount of time, the application can assume that the connecting peer is being referred and that the peer application should consider the connection attempt a failure.</span></span>

## <a name="peer-grouping-events"></a><span data-ttu-id="33c51-141">對等群組事件</span><span class="sxs-lookup"><span data-stu-id="33c51-141">Peer Grouping Events</span></span>

<span data-ttu-id="33c51-142">對等群組應用程式可以註冊以接收8對等事件的通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-142">A Peer Grouping application can register to receive notification for 8 peer events.</span></span> <span data-ttu-id="33c51-143">每個事件名稱前面都會加上 **對等 \_ 群組 \_ 事件 \_**，例如，**對等 \_ 群組 \_ 事件 \_ 狀態 \_ 已變更**。</span><span class="sxs-lookup"><span data-stu-id="33c51-143">Each event name is prefaced with **PEER\_GROUP\_EVENT\_**; for example, **PEER\_GROUP\_EVENT\_STATUS\_CHANGED**.</span></span> <span data-ttu-id="33c51-144">除非另有說明，否則會使用 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)抓取變更的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="33c51-144">Unless otherwise noted, information about a change is retrieved by using [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).</span></span>

-   <span data-ttu-id="33c51-145">**對等 \_群組 \_ 事件 \_ 狀態 \_ 變更** 指出群組狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="33c51-145">**PEER\_GROUP\_EVENT\_STATUS\_CHANGED** indicates that the group status has changed.</span></span> <span data-ttu-id="33c51-146">可能有兩個狀態值： **對等 \_ 群組 \_ 狀態 \_ 接聽**，表示群組沒有連線，且正在等候新的成員，而 **對等 \_ 群組 \_ 狀態 \_ 具有連線**，表示群組至少有一個連接。</span><span class="sxs-lookup"><span data-stu-id="33c51-146">There are two status values possible: **PEER\_GROUP\_STATUS\_LISTENING**, which indicates that the group has no connections and is waiting for new members; and **PEER\_GROUP\_STATUS\_HAS CONNECTIONS**, which indicates that the group has at least one connection.</span></span> <span data-ttu-id="33c51-147">這個狀態值可以藉由在引發此事件之後呼叫 [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) 來取得。</span><span class="sxs-lookup"><span data-stu-id="33c51-147">This status value can be obtained by calling [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) after this event is raised.</span></span>
-   <span data-ttu-id="33c51-148">**對等 \_群組 \_ 事件 \_ 屬性已 \_ 變更** 指出群組建立者已變更或更新了群組屬性。</span><span class="sxs-lookup"><span data-stu-id="33c51-148">**PEER\_GROUP\_EVENT\_PROPERTY\_CHANGED** indicates that the group properties have been changed or updated by the group creator.</span></span>
-   <span data-ttu-id="33c51-149">**對等 \_群組 \_ 事件 \_ 記錄 \_ 變更** 表示已執行記錄作業。</span><span class="sxs-lookup"><span data-stu-id="33c51-149">**PEER\_GROUP\_EVENT\_RECORD\_CHANGED** indicates that a record operation has been performed.</span></span> <span data-ttu-id="33c51-150">參與群組的對等發行、更新或刪除記錄時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-150">This event is raised when a peer participating in the group publishes, updates, or deletes a record.</span></span> <span data-ttu-id="33c51-151">例如，當聊天應用程式傳送聊天訊息時，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-151">For example, this event is raised when a chat application sends a chat message.</span></span>
-   <span data-ttu-id="33c51-152">**對等 \_群組 \_ 事件 \_ 成員 \_ 變更** 指出成員在群組內的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="33c51-152">**PEER\_GROUP\_EVENT\_MEMBER\_CHANGED** indicates that a member's status within the group has changed.</span></span> <span data-ttu-id="33c51-153">狀態變更包括：</span><span class="sxs-lookup"><span data-stu-id="33c51-153">Status changes include:</span></span>
    -   <span data-ttu-id="33c51-154">**對等 \_成員 \_ 已連接**。</span><span class="sxs-lookup"><span data-stu-id="33c51-154">**PEER\_MEMBER\_CONNECTED**.</span></span> <span data-ttu-id="33c51-155">對等已連接到群組。</span><span class="sxs-lookup"><span data-stu-id="33c51-155">A peer has connected to the group.</span></span>
    -   <span data-ttu-id="33c51-156">**對等 \_成員已 \_ 中斷** 連線。</span><span class="sxs-lookup"><span data-stu-id="33c51-156">**PEER\_MEMBER\_DISCONNECTED**.</span></span> <span data-ttu-id="33c51-157">對等已與群組中斷連接。</span><span class="sxs-lookup"><span data-stu-id="33c51-157">A peer has disconnected from the group.</span></span>
    -   <span data-ttu-id="33c51-158">**對等 \_\_加入的成員**。</span><span class="sxs-lookup"><span data-stu-id="33c51-158">**PEER\_MEMBER\_JOINED**.</span></span> <span data-ttu-id="33c51-159">已針對對等發行新的成員資格資訊。</span><span class="sxs-lookup"><span data-stu-id="33c51-159">New membership information has been published for a peer.</span></span>
    -   <span data-ttu-id="33c51-160">**對等 \_\_已更新成員**。</span><span class="sxs-lookup"><span data-stu-id="33c51-160">**PEER\_MEMBER\_UPDATED**.</span></span> <span data-ttu-id="33c51-161">對等已更新為新的資訊，例如新的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="33c51-161">A peer has updated with new information, such as a new IP address.</span></span>
-   <span data-ttu-id="33c51-162">**對等 \_將 \_ 事件 \_ 鄰居 \_ 連接分組**。</span><span class="sxs-lookup"><span data-stu-id="33c51-162">**PEER\_GROUP\_EVENT\_NEIGHBOR\_CONNECTION**.</span></span> <span data-ttu-id="33c51-163">將參與群組內鄰近連接的對等必須註冊此事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-163">Peers who will participate in neighbor connections within the group must register for this event.</span></span> <span data-ttu-id="33c51-164">請注意，註冊這個事件並不會讓對等接收資料;此事件的註冊只會在收到鄰近連接的要求時，確保通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-164">Note that registering for this event does not enable the peer to receive data; registration for this event only ensures notification when a request for a neighbor connection is received.</span></span>
-   <span data-ttu-id="33c51-165">**對等 \_群組 \_ 事件 \_ 直接 \_ 連接**。</span><span class="sxs-lookup"><span data-stu-id="33c51-165">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION**.</span></span> <span data-ttu-id="33c51-166">將參與群組內直接連線的對等必須註冊此事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-166">Peers who will participate in direct connections within the group must register for this event.</span></span> <span data-ttu-id="33c51-167">請注意，註冊這個事件並不會讓對等接收資料;此事件的註冊只會確保收到直接連線要求時的通知。</span><span class="sxs-lookup"><span data-stu-id="33c51-167">Note that registering for this event does not enable the peer to receive data; registration for this event only ensures notification when a request for a direct connection is received.</span></span>
-   <span data-ttu-id="33c51-168">**對等 \_群組 \_ 事件 \_ \_** 內送資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-168">**PEER\_GROUP\_EVENT\_INCOMING\_DATA**.</span></span> <span data-ttu-id="33c51-169">將透過鄰近或直接連接接收資料的對等，必須註冊此事件。</span><span class="sxs-lookup"><span data-stu-id="33c51-169">Peers who will receive data over a neighbor or direct connection must register for this event.</span></span> <span data-ttu-id="33c51-170">當引發這個事件時，可以藉由呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)來取得其他參與對等互連所傳送的不透明資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-170">When this event is raised, the opaque data transmitted by the other participating peer can be obtained by calling [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).</span></span> <span data-ttu-id="33c51-171">請注意，若要接收此事件，對等體必須先前已註冊對 **等 \_ 群組 \_ 事件 \_ 直接 \_ 連接** 或 **對等 \_ 群組 \_ 事件 \_ 相鄰 \_ 連接**。</span><span class="sxs-lookup"><span data-stu-id="33c51-171">Note that to receive this event, the peer must have previously registered for **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** or **PEER\_GROUP\_EVENT\_NEIGHBOR\_CONNECTION**.</span></span>
-   <span data-ttu-id="33c51-172">**對等 \_群組 \_ 事件 \_ 連接 \_ 失敗**。</span><span class="sxs-lookup"><span data-stu-id="33c51-172">**PEER\_GROUP\_EVENT\_CONNECTION\_FAILED**.</span></span> <span data-ttu-id="33c51-173">連接因某些原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="33c51-173">A connection failed for some reason.</span></span> <span data-ttu-id="33c51-174">當引發這個事件時，不會提供任何資料，也不應該呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) 。</span><span class="sxs-lookup"><span data-stu-id="33c51-174">No data is provided when this event is raised, and [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) should not be called.</span></span>

<span data-ttu-id="33c51-175">當應用程式收到發生對等事件的通知之後 (排除 **對等 \_ 群組 \_ 事件 \_ 連接 \_ 失敗**) ，應用程式會呼叫 [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)，並傳遞 [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)所傳回的對等事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="33c51-175">After an application receives notification that a peer event has occurred (excluding **PEER\_GROUP\_EVENT\_CONNECTION\_FAILED**), the application calls [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata), and passes the peer event handle returned by [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).</span></span> <span data-ttu-id="33c51-176">對等的基礎結構會傳回 [**對等 \_ 群組 \_ 事件 \_ 資料**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) 結構的指標，其中包含所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="33c51-176">The Peer Infrastructure returns a pointer to a [**PEER\_GROUP\_EVENT\_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure that contains the requested data.</span></span> <span data-ttu-id="33c51-177">必須先呼叫此函式，直到 **對等 \_ S \_ 沒有傳回任何 \_ 事件 \_ 資料** 為止。</span><span class="sxs-lookup"><span data-stu-id="33c51-177">This function must be called until **PEER\_S\_NO\_EVENT\_DATA** is returned.</span></span> <span data-ttu-id="33c51-178">當應用程式不再需要對等事件的通知時，必須呼叫 [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent)，然後在應用程式註冊特定事件時，傳遞 **PeerGroupRegisterEvent** 所傳回的對等事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="33c51-178">When an application no longer requires notification for a peer event, a call must be made to [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), passing the peer event handle returned by **PeerGroupRegisterEvent** when the application registered for the particular event.</span></span>

## <a name="example-of-registering-for-peer-graphing-events"></a><span data-ttu-id="33c51-179">註冊對等圖形事件的範例</span><span class="sxs-lookup"><span data-stu-id="33c51-179">Example of Registering for Peer Graphing Events</span></span>

<span data-ttu-id="33c51-180">下列程式碼範例會示範如何向對等圖形事件進行註冊。</span><span class="sxs-lookup"><span data-stu-id="33c51-180">The following code sample shows you how to register with the Peer Graphing events.</span></span>


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



 

 



