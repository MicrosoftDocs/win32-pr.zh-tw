---
description: 本節中所述的分類會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面區分開來。
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Multipoint 分類法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848011"
---
# <a name="multipoint-taxonomy"></a><span data-ttu-id="3851c-103">Multipoint 分類法</span><span class="sxs-lookup"><span data-stu-id="3851c-103">Multipoint Taxonomy</span></span>

<span data-ttu-id="3851c-104">本節中所述的分類會先從處理在會話參與者間傳送資料的資料平面，將關注本身與 multipoint 會話建立方式的控制平面區分開來。</span><span class="sxs-lookup"><span data-stu-id="3851c-104">The taxonomy described in this section first distinguishes the control plane that concerns itself with the way a multipoint session is established, from the data plane that deals with the transfer of data among session participants.</span></span>

## <a name="session-establishment-in-the-control-plane"></a><span data-ttu-id="3851c-105">控制平面中的會話建立</span><span class="sxs-lookup"><span data-stu-id="3851c-105">Session Establishment in the Control Plane</span></span>

<span data-ttu-id="3851c-106">在控制平面中，有兩種不同類型的會話建立：</span><span class="sxs-lookup"><span data-stu-id="3851c-106">In the control plane there are two distinct types of session establishment:</span></span>

-   <span data-ttu-id="3851c-107">植根</span><span class="sxs-lookup"><span data-stu-id="3851c-107">rooted</span></span>
-   <span data-ttu-id="3851c-108">nonrooted</span><span class="sxs-lookup"><span data-stu-id="3851c-108">nonrooted</span></span>

<span data-ttu-id="3851c-109">在進行根控制項的情況下，有一個特殊的參與者（c \_ 根）與這個 multipoint 會話的其餘成員不同，每一個都稱為 c 分 \_ 葉。</span><span class="sxs-lookup"><span data-stu-id="3851c-109">In the case of rooted control, a special participant, c\_root, exists that is different from the rest of the members of this multipoint session, each of which are called a c\_leaf.</span></span> <span data-ttu-id="3851c-110">\_針對 multipoint 會話的整個持續期間，c 根必須保持存在，因為會話會在沒有 c 根的情況下中斷 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3851c-110">The c\_root must remain present for the whole duration of the multipoint session, as the session is broken up in the absence of the c\_root.</span></span> <span data-ttu-id="3851c-111">C \_ 根通常會藉由設定與 c 分葉的連接 \_ ，或多個 c 葉子來起始 multipoint 會話 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3851c-111">The c\_root usually initiates the multipoint session by setting up the connection to a c\_leaf, or a number of c\_leafs.</span></span> <span data-ttu-id="3851c-112">在 \_ 某些情況下，c 根可能會新增更多 \_ 的 c 葉子或 () c 分 \_ 葉可以 \_ 在稍後加入 c 根。</span><span class="sxs-lookup"><span data-stu-id="3851c-112">The c\_root may add more c\_leafs, or (in some cases) a c\_leaf can join the c\_root at a later time.</span></span> <span data-ttu-id="3851c-113">您可以在 ATM 和聖 II 中找到根控制項平面的範例。</span><span class="sxs-lookup"><span data-stu-id="3851c-113">Examples of the rooted control plane can be found in ATM and ST-II.</span></span>

<span data-ttu-id="3851c-114">針對 nonrooted 控制平面，屬於 multipoint 會話的所有成員都是離開的，也就是說，沒有任何特殊的參與者可作為 c \_ 根。</span><span class="sxs-lookup"><span data-stu-id="3851c-114">For a nonrooted control plane, all the members belonging to a multipoint session are leaves, that is, no special participant acting as a c\_root exists.</span></span> <span data-ttu-id="3851c-115">每個 c 分 \_ 葉都必須將自己新增到預先存在的 multipoint 會話，此會話永遠可用 (例如 IP 多播位址) 的情況，或已透過部分超出 Windows 通訊端規格範圍的頻外 (OOB) 機制來進行設定。</span><span class="sxs-lookup"><span data-stu-id="3851c-115">Each c\_leaf must add itself to a preexisting multipoint session that is always available (as in the case of an IP multicast address), or has been set up through some out-of-band (OOB) mechanism that is outside the scope of the Windows Sockets specification.</span></span>

<span data-ttu-id="3851c-116">另一種查看方法的方法是，c \_ 根仍然存在，但是可以被視為是在網路雲端中，而不是其中一個參與者。</span><span class="sxs-lookup"><span data-stu-id="3851c-116">Another way to look at this is that a c\_root still exists, but can be considered to be in the network cloud as opposed to one of the participants.</span></span> <span data-ttu-id="3851c-117">由於控制項根目錄仍然存在，因此也可以將 nonrooted 控制平面視為隱含根。</span><span class="sxs-lookup"><span data-stu-id="3851c-117">Because a control root still exists, a nonrooted control plane could also be considered to be implicitly rooted.</span></span> <span data-ttu-id="3851c-118">這種隱含根目錄的 multipoint 配置範例如下：</span><span class="sxs-lookup"><span data-stu-id="3851c-118">Examples for this kind of implicitly rooted multipoint schemes are:</span></span>

-   <span data-ttu-id="3851c-119">電話會議橋接器。</span><span class="sxs-lookup"><span data-stu-id="3851c-119">A teleconferencing bridge.</span></span>
-   <span data-ttu-id="3851c-120">IP 多播系統。</span><span class="sxs-lookup"><span data-stu-id="3851c-120">The IP multicast system.</span></span>
-   <span data-ttu-id="3851c-121">Multipoint 控制項單位 (MCU) 在 320 video 會議中。</span><span class="sxs-lookup"><span data-stu-id="3851c-121">A Multipoint Control Unit (MCU) in an H.320 video conference.</span></span>

## <a name="data-transfer-in-the-data-plane"></a><span data-ttu-id="3851c-122">資料平面中的資料傳輸</span><span class="sxs-lookup"><span data-stu-id="3851c-122">Data Transfer in the Data Plane</span></span>

<span data-ttu-id="3851c-123">在資料平面中，有兩種類型的資料傳輸樣式：</span><span class="sxs-lookup"><span data-stu-id="3851c-123">In the data plane, there are two types of data transfer styles:</span></span>

-   <span data-ttu-id="3851c-124">植根</span><span class="sxs-lookup"><span data-stu-id="3851c-124">rooted</span></span>
-   <span data-ttu-id="3851c-125">nonrooted</span><span class="sxs-lookup"><span data-stu-id="3851c-125">nonrooted</span></span>

<span data-ttu-id="3851c-126">在根資料平面中，有一個稱為 d root 的特殊參與者 \_ 存在。</span><span class="sxs-lookup"><span data-stu-id="3851c-126">In a rooted data plane, a special participant called d\_root exists.</span></span> <span data-ttu-id="3851c-127">資料傳輸只會發生在 d \_ 根和這個 multipoint 會話的其餘成員之間，每個都稱為 d 分 \_ 葉。</span><span class="sxs-lookup"><span data-stu-id="3851c-127">Data transfer only occurs between the d\_root and the rest of the members of this multipoint session, each of which are referred to as a d\_leaf.</span></span> <span data-ttu-id="3851c-128">流量可能是單向或雙向。</span><span class="sxs-lookup"><span data-stu-id="3851c-128">The traffic could be unidirectional or bidirectional.</span></span> <span data-ttu-id="3851c-129">從 d 根目錄送出的資料 \_ 會在必要時重複 (如有需要) 並傳遞至每個 d 分 \_ 葉，而 d 葉子的資料 \_ 只會移至 d \_ 根。</span><span class="sxs-lookup"><span data-stu-id="3851c-129">The data sent out from the d\_root is duplicated (if required) and delivered to every d\_leaf, while the data from d\_leafs only goes to the d\_root.</span></span> <span data-ttu-id="3851c-130">在根資料平面的情況下，d 葉子之間不允許流量 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3851c-130">In the case of a rooted data plane, no traffic is allowed among d\_leafs.</span></span> <span data-ttu-id="3851c-131">位於資料平面中的通訊協定範例是 ST-II。</span><span class="sxs-lookup"><span data-stu-id="3851c-131">An example of a protocol that is rooted in the data plane is ST-II.</span></span>

<span data-ttu-id="3851c-132">在 nonrooted 資料平面中，所有參與者都相等，也就是它們傳送的任何資料都會傳遞給相同 multipoint 會話中的所有其他參與者。</span><span class="sxs-lookup"><span data-stu-id="3851c-132">In a nonrooted data plane, all the participants are equal, that is, any data they send is delivered to all the other participants in the same multipoint session.</span></span> <span data-ttu-id="3851c-133">同樣地，每個 d 分 \_ 葉節點都可以接收來自其他所有 d 葉子的資料 \_ ，而在某些情況下，則是從其他未參與 multipoint 會話的節點接收。</span><span class="sxs-lookup"><span data-stu-id="3851c-133">Likewise each d\_leaf node can receive data from all other d\_leafs, and in some cases, from other nodes that are not participating in the multipoint session.</span></span> <span data-ttu-id="3851c-134">沒有特殊 \_ 的 d 根節點。</span><span class="sxs-lookup"><span data-stu-id="3851c-134">No special d\_root node exists.</span></span> <span data-ttu-id="3851c-135">IP-多播是在資料平面中 nonrooted。</span><span class="sxs-lookup"><span data-stu-id="3851c-135">IP-multicast is nonrooted in the data plane.</span></span>

<span data-ttu-id="3851c-136">請注意，資料單位重複發生的位置，或共用的單一樹狀結構或多個最短路徑樹狀結構是否用於 multipoint 分佈是通訊協定問題，以及應用程式用來執行 multipoint 通訊的介面不相關的問題。</span><span class="sxs-lookup"><span data-stu-id="3851c-136">Note that the question of where data unit duplication occurs, or whether a shared single tree or multiple shortest-path trees are used for multipoint distribution are protocol issues, and irrelevant to the interface the application would use to perform multipoint communications.</span></span> <span data-ttu-id="3851c-137">因此，這些問題不會在此附錄或 Windows 通訊端介面中解決。</span><span class="sxs-lookup"><span data-stu-id="3851c-137">Therefore these issues are not addressed in this appendix or the Windows Sockets interface.</span></span>

<span data-ttu-id="3851c-138">下表描述上述的分類，並指出現有的配置如何符合每個類別。</span><span class="sxs-lookup"><span data-stu-id="3851c-138">The following table depicts the taxonomy described above and indicates how existing schemes fit into each of the categories.</span></span> <span data-ttu-id="3851c-139">請注意，沒有任何現有的配置會採用 nonrooted 控制平面以及根資料平面。</span><span class="sxs-lookup"><span data-stu-id="3851c-139">Note that there do not appear to be any existing schemes that employ a nonrooted control plane along with a rooted data plane.</span></span>

|                      | <span data-ttu-id="3851c-140">根控制項平面</span><span class="sxs-lookup"><span data-stu-id="3851c-140">Rooted control plane</span></span> | <span data-ttu-id="3851c-141">Nonrooted (隱含根目錄) 控制平面</span><span class="sxs-lookup"><span data-stu-id="3851c-141">Nonrooted (implicit rooted) control plane</span></span> |
|----------------------|----------------------|-------------------------------------------|
| <span data-ttu-id="3851c-142">根資料平面</span><span class="sxs-lookup"><span data-stu-id="3851c-142">Rooted data plane</span></span>    | <span data-ttu-id="3851c-143">ATM，聖 II</span><span class="sxs-lookup"><span data-stu-id="3851c-143">ATM, ST-II</span></span>           | <span data-ttu-id="3851c-144">沒有已知的範例。</span><span class="sxs-lookup"><span data-stu-id="3851c-144">No known examples.</span></span>                        |
| <span data-ttu-id="3851c-145">Nonrooted 資料平面</span><span class="sxs-lookup"><span data-stu-id="3851c-145">Nonrooted data plane</span></span> | <span data-ttu-id="3851c-146">T. 120</span><span class="sxs-lookup"><span data-stu-id="3851c-146">T.120</span></span>                | <span data-ttu-id="3851c-147">IP-多播、.H 320 (MCU) </span><span class="sxs-lookup"><span data-stu-id="3851c-147">IP-multicast, H.320 (MCU)</span></span>                 |



 

 

 



