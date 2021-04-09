---
description: IP 協助程式可讓您存取在本機電腦上使用之網路通訊協定的相關資訊。
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: 正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695871"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="96786-103">正在抓取傳輸控制通訊協定和使用者資料包協定的相關資訊</span><span class="sxs-lookup"><span data-stu-id="96786-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="96786-104">IP 協助程式可讓您存取在本機電腦上使用之網路通訊協定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96786-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="96786-105">使用下列段落中所述的函式，在本機電腦上取得傳輸控制通訊協定 (TCP) 和使用者資料包協定 (UDP) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="96786-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="96786-106">[**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics)函數會抓取 TCP 目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="96786-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="96786-107">如需涉及 **GetTcpStatistics** 的程式碼範例，請參閱 [使用 GetTcpStatistics 抓取資訊](retrieving-information-using-gettcpstatistics.md)。</span><span class="sxs-lookup"><span data-stu-id="96786-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="96786-108">[**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics)函式會捕獲 UDP 目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="96786-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="96786-109">[**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable)函數會抓取 TCP 連接資料表。</span><span class="sxs-lookup"><span data-stu-id="96786-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="96786-110">[**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable)會捕獲 UDP 接聽程式資料表。</span><span class="sxs-lookup"><span data-stu-id="96786-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="96786-111">[**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry)函式可讓開發人員將指定 TCP 連接的狀態設定為 MIB \_ tcp \_ 狀態 \_ 刪除 \_ TCB。</span><span class="sxs-lookup"><span data-stu-id="96786-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



