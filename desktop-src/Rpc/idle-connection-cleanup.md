---
title: 閒置連接清除
description: 依預設，在整個關聯關閉之前，不會關閉執行緒集區中的連接。
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839507"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="d56c9-103">閒置連接清除</span><span class="sxs-lookup"><span data-stu-id="d56c9-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="d56c9-104">依預設，在整個關聯關閉之前，不會關閉執行緒集區中的連接。</span><span class="sxs-lookup"><span data-stu-id="d56c9-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="d56c9-105">此原則可讓具有大量執行緒或安全性識別的用戶端以有效率的方式對伺服器進行 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d56c9-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="d56c9-106">缺點是可能會認可大量的資源，以維護這些連接。</span><span class="sxs-lookup"><span data-stu-id="d56c9-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="d56c9-107">為了管理進程，RPC 提供 [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) 函數。</span><span class="sxs-lookup"><span data-stu-id="d56c9-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="d56c9-108">此函式會啟用閒置連接清除;用戶端會定期掃描連接集區，並關閉最近未使用的連接。</span><span class="sxs-lookup"><span data-stu-id="d56c9-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="d56c9-109">如果關聯已維持內容控制碼，閒置連接清除會關閉所有閒置的連接，但即使連接閒置 (，還是會確定至少有一個連接保持開啟狀態，否則伺服器會取得內容控制碼執行下) 。</span><span class="sxs-lookup"><span data-stu-id="d56c9-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="d56c9-110">如果關聯未維持內容控制碼，閒置連接清除會關閉所有閒置的連接，即使這樣做不會在集區中保留任何連接。</span><span class="sxs-lookup"><span data-stu-id="d56c9-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="d56c9-111">在 Windows XP 上，RPC 執行時間會追蹤關聯中開啟的連接數目，如果任何關聯中的連接數目超過特定臨界值，就會自動開啟閒置的連線清除。</span><span class="sxs-lookup"><span data-stu-id="d56c9-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




