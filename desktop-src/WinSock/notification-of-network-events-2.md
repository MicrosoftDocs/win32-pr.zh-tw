---
description: 資料傳輸服務提供者最重要的責任之一，就是在發生某些網路事件時，提供用戶端的指示。
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: 網路事件的通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848006"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="daf65-103">網路事件的通知</span><span class="sxs-lookup"><span data-stu-id="daf65-103">Notification of Network Events</span></span>

<span data-ttu-id="daf65-104">資料傳輸服務提供者最重要的責任之一，就是在發生某些網路事件時，提供用戶端的指示。</span><span class="sxs-lookup"><span data-stu-id="daf65-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="daf65-105">定義的網路事件清單包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="daf65-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="daf65-106">**FD \_連接**-遠端主機或多播會話的連接已完成。</span><span class="sxs-lookup"><span data-stu-id="daf65-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="daf65-107">**FD \_接受**-遠端主機正在進行連線要求。</span><span class="sxs-lookup"><span data-stu-id="daf65-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="daf65-108">**FD \_讀取**-網路資料已抵達，可供讀取。</span><span class="sxs-lookup"><span data-stu-id="daf65-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="daf65-109">**FD \_寫入**：服務提供者的緩衝區中已有空間可供使用，因此現在可能會傳送額外的資料。</span><span class="sxs-lookup"><span data-stu-id="daf65-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="daf65-110">**FD \_OOB**-頻外資料可供讀取。</span><span class="sxs-lookup"><span data-stu-id="daf65-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="daf65-111">**FD \_關閉**-遠端主機已關閉連接。</span><span class="sxs-lookup"><span data-stu-id="daf65-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="daf65-112">**FD \_QOS**-已協商的 qos 層級發生變更。</span><span class="sxs-lookup"><span data-stu-id="daf65-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="daf65-113">**FD \_將 \_ QOS 分組**（保留）。</span><span class="sxs-lookup"><span data-stu-id="daf65-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="daf65-114">**FD \_路由 \_ 介面 \_ 變更**：應用來存取 **SIO \_ 路由 \_ 介面 \_ 變更 IOCTL** 中指定之目的地的本機介面已變更。</span><span class="sxs-lookup"><span data-stu-id="daf65-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="daf65-115">**FD \_位址 \_ 清單 \_ 變更**-應用程式可以系結的本機地址清單已變更。</span><span class="sxs-lookup"><span data-stu-id="daf65-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="daf65-116">以上列舉的網路事件集有時稱為 **FD \_ XXX** 事件。</span><span class="sxs-lookup"><span data-stu-id="daf65-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="daf65-117">根據用戶端要求通知的方式，可能會有幾種方式指出出現一或多個這類網路事件。</span><span class="sxs-lookup"><span data-stu-id="daf65-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



