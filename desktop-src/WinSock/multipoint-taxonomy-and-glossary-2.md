---
description: 以下所述的分類，會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面加以區別。
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Multipoint 分類法和詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ecdfe59640ec58b592aace4e46c66faf752281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967127"
---
# <a name="multipoint-taxonomy-and-glossary"></a><span data-ttu-id="f26c2-103">Multipoint 分類法和詞彙</span><span class="sxs-lookup"><span data-stu-id="f26c2-103">Multipoint Taxonomy and Glossary</span></span>

<span data-ttu-id="f26c2-104">以下所述的分類，會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面加以區別。</span><span class="sxs-lookup"><span data-stu-id="f26c2-104">The taxonomy described below first distinguishes the control plane that concerns itself with the way a multipoint session is established, from the data plane that deals with the transfer of data among session participants.</span></span>

<span data-ttu-id="f26c2-105">在控制平面中，有兩種不同類型的會話建立：</span><span class="sxs-lookup"><span data-stu-id="f26c2-105">In the control plane, there are two distinct types of session establishment:</span></span>

-   <span data-ttu-id="f26c2-106">植根</span><span class="sxs-lookup"><span data-stu-id="f26c2-106">rooted</span></span>
-   <span data-ttu-id="f26c2-107">nonrooted</span><span class="sxs-lookup"><span data-stu-id="f26c2-107">nonrooted</span></span>

<span data-ttu-id="f26c2-108">針對根控制項平面，有一個稱為 c root 的特殊參與者，與 \_ 這個 multipoint 會話的其餘成員不同，每一個都稱為 c 分 \_ 葉。</span><span class="sxs-lookup"><span data-stu-id="f26c2-108">For a rooted control plane, there exists a special participant, called c\_root, that is different from the rest of the members of this multipoint session, each of which is called a c\_leaf.</span></span> <span data-ttu-id="f26c2-109">在 \_ multipoint 會話的整個持續期間，c 根必須保持存在，因為會話將會在沒有 c 根的情況下中斷 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f26c2-109">The c\_root must remain present for the whole duration of the multipoint session, as the session will be broken up in the absence of the c\_root.</span></span> <span data-ttu-id="f26c2-110">C \_ 根通常會藉由設定與 c 分葉的連接 \_ ，或多個 c 葉子來起始 multipoint 會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f26c2-110">The c\_root usually initiates the multipoint session by setting up the connection to a c\_leaf, or a number of c\_leafs.</span></span> <span data-ttu-id="f26c2-111">在 \_ 某些情況下，c 根可能會新增更多 \_ 的 c 葉子或 () c 分 \_ 葉可以 \_ 在稍後加入 c 根。</span><span class="sxs-lookup"><span data-stu-id="f26c2-111">The c\_root may add more c\_leafs, or (in some cases) a c\_leaf can join the c\_root at a later time.</span></span> <span data-ttu-id="f26c2-112">您可以在 ATM 和聖 II 中找到根控制項平面的範例。</span><span class="sxs-lookup"><span data-stu-id="f26c2-112">Examples of the rooted control plane can be found in ATM and ST-II.</span></span>

<span data-ttu-id="f26c2-113">針對 nonrooted 控制平面，屬於 multipoint 會話的所有成員都是離開的，也就是說，沒有任何特殊的參與者可作為 c \_ 根。</span><span class="sxs-lookup"><span data-stu-id="f26c2-113">For a nonrooted control plane, all members belonging to a multipoint session are leaves, that is, no special participant acting as a c\_root exists.</span></span> <span data-ttu-id="f26c2-114">每個 c 分 \_ 葉都必須將自己新增至既有的 multipoint 會話，永遠可用 (例如 IP 多播位址) ，或已透過某些不在此 (討論範圍內的 OOB 機制進行設定，因此不會在建議的 Windows 通訊端擴充) 中解決此情況。</span><span class="sxs-lookup"><span data-stu-id="f26c2-114">Each c\_leaf needs to add itself to a pre-existing multipoint session that either is always available (as in the case of an IP multicast address), or has been set up through some OOB mechanism which is outside the scope of this discussion (and hence not addressed in the proposed Windows Sockets extensions).</span></span> <span data-ttu-id="f26c2-115">另一種查看方法的方法是，c \_ 根仍然存在，但是可以被視為是在網路雲端中，而不是其中一個參與者。</span><span class="sxs-lookup"><span data-stu-id="f26c2-115">Another way to look at this is that a c\_root still exists, but can be considered to be in the network cloud as opposed to one of the participants.</span></span> <span data-ttu-id="f26c2-116">由於控制項根目錄仍然存在，因此也可以將 nonrooted 控制平面視為隱含根。</span><span class="sxs-lookup"><span data-stu-id="f26c2-116">Because a control root still exists, a nonrooted control plane could also be considered to be implicitly rooted.</span></span> <span data-ttu-id="f26c2-117">這種隱含根目錄的 multipoint 配置範例包括：電話會議橋接器、IP 多播系統、Multipoint 控制項單位 (MCU) 在 320 video 會議中等等。</span><span class="sxs-lookup"><span data-stu-id="f26c2-117">Examples of this kind of implicitly rooted multipoint schemes are: a teleconferencing bridge, the IP multicast system, a Multipoint Control Unit (MCU) in an H.320 video conference, etc.</span></span>

<span data-ttu-id="f26c2-118">在資料平面中，也有兩種類型的資料傳輸樣式：</span><span class="sxs-lookup"><span data-stu-id="f26c2-118">In the data plane, there are also two types of data transfer styles:</span></span>

-   <span data-ttu-id="f26c2-119">植根</span><span class="sxs-lookup"><span data-stu-id="f26c2-119">rooted</span></span>
-   <span data-ttu-id="f26c2-120">nonrooted</span><span class="sxs-lookup"><span data-stu-id="f26c2-120">nonrooted</span></span>

<span data-ttu-id="f26c2-121">在根資料平面中，有一個稱為 d root 的特殊參與者 \_ 存在。</span><span class="sxs-lookup"><span data-stu-id="f26c2-121">In a rooted data plane, a special participant called d\_root exists.</span></span> <span data-ttu-id="f26c2-122">資料傳輸只會發生在 d \_ 根和這個 multipoint 會話的其餘成員之間，每個都稱為 d 分 \_ 葉。</span><span class="sxs-lookup"><span data-stu-id="f26c2-122">Data transfer only occurs between the d\_root and the rest of the members of this multipoint session, each of which is referred to as a d\_leaf.</span></span> <span data-ttu-id="f26c2-123">流量可能是單向或雙向。</span><span class="sxs-lookup"><span data-stu-id="f26c2-123">The traffic could be unidirectional, or bidirectional.</span></span> <span data-ttu-id="f26c2-124">從 d 根目錄送出的資料 \_ 將會複製 (如果需要) 並傳遞至每個 d 分 \_ 葉，而 d 葉子的資料 \_ 只會移至 d \_ 根。</span><span class="sxs-lookup"><span data-stu-id="f26c2-124">The data sent out from the d\_root will be duplicated (if required) and delivered to every d\_leaf, while the data from d\_leafs will only go to the d\_root.</span></span> <span data-ttu-id="f26c2-125">在根資料平面的案例中，d 葉子之間不允許流量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f26c2-125">In the case of a rooted data plane, there is no traffic allowed among d\_leafs.</span></span> <span data-ttu-id="f26c2-126">使用根資料平面的通訊協定範例是 ST-II。</span><span class="sxs-lookup"><span data-stu-id="f26c2-126">An example of a protocol that is uses a rooted data plane is ST-II.</span></span>

<span data-ttu-id="f26c2-127">在 nonrooted 資料平面中，所有參與者的意義都相等，因為它們傳送的任何資料都會傳遞給相同 multipoint 會話中的所有其他參與者。</span><span class="sxs-lookup"><span data-stu-id="f26c2-127">In a nonrooted data plane, all the participants are equal in the sense that any data they send will be delivered to all the other participants in the same multipoint session.</span></span> <span data-ttu-id="f26c2-128">同樣地，每個 d 分 \_ 葉節點都可以接收來自其他所有 d 葉子的資料 \_ ，而在某些情況下，也可以從其他尚未參與 multipoint 會話的節點接收資料。</span><span class="sxs-lookup"><span data-stu-id="f26c2-128">Likewise each d\_leaf node will be able to receive data from all other d\_leafs, and in some cases, from other nodes which are not participating in the multipoint session as well.</span></span> <span data-ttu-id="f26c2-129">沒有特殊 \_ 的 d 根節點。</span><span class="sxs-lookup"><span data-stu-id="f26c2-129">No special d\_root node exists.</span></span> <span data-ttu-id="f26c2-130">IP-多播是使用 nonrooted 資料平面的通訊協定範例。</span><span class="sxs-lookup"><span data-stu-id="f26c2-130">IP-multicast is an example of a protocol that uses a nonrooted data plane.</span></span>

<span data-ttu-id="f26c2-131">請注意，資料單位重複發生的問題，或共用的單一樹狀目錄或多個最短路徑樹狀結構是否用於 multipoint 分佈是通訊協定問題。</span><span class="sxs-lookup"><span data-stu-id="f26c2-131">Note that the question of where data unit duplication occurs, or whether a shared single tree or multiple shortest-path trees are used for multipoint distribution are protocol issues.</span></span> <span data-ttu-id="f26c2-132">因此，它們與用戶端用來執行 multipoint 通訊的介面無關。</span><span class="sxs-lookup"><span data-stu-id="f26c2-132">As such, they are irrelevant to the interface the client would use to perform multipoint communications.</span></span> <span data-ttu-id="f26c2-133">因此，Windows 通訊端介面不會解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="f26c2-133">Therefore these issues are not addressed by the Windows Sockets interface.</span></span>

<span data-ttu-id="f26c2-134">下表描述上述的分類，並指出現有的配置如何符合每個控制項和資料平面類別。</span><span class="sxs-lookup"><span data-stu-id="f26c2-134">The following table depicts the taxonomy described above and indicates how existing schemes fit into each of the control and data plane categories.</span></span> <span data-ttu-id="f26c2-135">請注意，沒有任何 multipoint 配置會使用 nonrooted 控制平面以及根資料平面。</span><span class="sxs-lookup"><span data-stu-id="f26c2-135">Note that there does not appear to be any multipoint schemes that employ a nonrooted control plane along with a rooted data plane.</span></span>

| <span data-ttu-id="f26c2-136">資料平面</span><span class="sxs-lookup"><span data-stu-id="f26c2-136">Data plane</span></span>           | <span data-ttu-id="f26c2-137">根控制項平面範例</span><span class="sxs-lookup"><span data-stu-id="f26c2-137">Rooted control plane examples</span></span> | <span data-ttu-id="f26c2-138">Nonrooted (隱含根目錄) 控制平面範例</span><span class="sxs-lookup"><span data-stu-id="f26c2-138">Nonrooted (implicit rooted) control plane examples</span></span> |
|----------------------|-------------------------------|----------------------------------------------------|
| <span data-ttu-id="f26c2-139">根資料平面</span><span class="sxs-lookup"><span data-stu-id="f26c2-139">Rooted data plane</span></span>    | <span data-ttu-id="f26c2-140">ATM，聖 II</span><span class="sxs-lookup"><span data-stu-id="f26c2-140">ATM, ST-II</span></span>                    | <span data-ttu-id="f26c2-141">沒有已知的範例</span><span class="sxs-lookup"><span data-stu-id="f26c2-141">No known examples</span></span>                                  |
| <span data-ttu-id="f26c2-142">Nonrooted 資料平面</span><span class="sxs-lookup"><span data-stu-id="f26c2-142">Nonrooted data plane</span></span> | <span data-ttu-id="f26c2-143">T. 120</span><span class="sxs-lookup"><span data-stu-id="f26c2-143">T.120</span></span>                         | <span data-ttu-id="f26c2-144">IP-多播、.H 320 (MCU) </span><span class="sxs-lookup"><span data-stu-id="f26c2-144">IP-multicast, H.320 (MCU)</span></span>                          |



 

 

 



