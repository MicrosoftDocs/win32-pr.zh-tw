---
description: 對等圖形 API 可讓應用程式有效率且可靠地在對等之間傳遞資料。 對等圖形技術的核心概念是對等圖形的節點，以及事件通知。
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: 關於圖形 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979787"
---
# <a name="about-the-graphing-api"></a><span data-ttu-id="7b5d3-104">關於圖形 API</span><span class="sxs-lookup"><span data-stu-id="7b5d3-104">About the Graphing API</span></span>

<span data-ttu-id="7b5d3-105">對等圖形 API 可讓應用程式有效率且可靠地在對等之間傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-105">The Peer Graphing API allows applications to pass data between peers efficiently and reliably.</span></span> <span data-ttu-id="7b5d3-106">對等圖形技術的核心概念是對等圖形的 **節點** ，以及事件通知。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-106">The core concepts of peer graph technology are the **nodes** of a peer graph, and event notices.</span></span>

## <a name="nodes"></a><span data-ttu-id="7b5d3-107">節點</span><span class="sxs-lookup"><span data-stu-id="7b5d3-107">Nodes</span></span>

<span data-ttu-id="7b5d3-108">節點代表網路上對等的特定實例。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-108">A node represents a specific instance of a peer on a network.</span></span> <span data-ttu-id="7b5d3-109">對等圖形 API 基礎結構可確保每個節點在圖形中都具有一致的資料檢視。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-109">The Peer Graphing API infrastructure ensures that each node has a consistent view of the data in a graph.</span></span> <span data-ttu-id="7b5d3-110">節點有下列功能：</span><span class="sxs-lookup"><span data-stu-id="7b5d3-110">A node has the following features:</span></span>

-   <span data-ttu-id="7b5d3-111">可以連接到不同的節點，並形成稱為對等圖形的相互關聯網路。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-111">Can connect to a different node, and form an interrelated network called a peer graph.</span></span>
-   <span data-ttu-id="7b5d3-112">可以與圖形中的其他節點以 [記錄](records.md)形式共用資料。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-112">Can share data with other nodes in a graph in the form of a [record](records.md).</span></span>
-   <span data-ttu-id="7b5d3-113">可以建立與使用對等 [群組 API](about-the-grouping-api.md)所建立之對等圖形分開的直接連接。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-113">Can create direct connections separate from the peer graphs established by using the Peer [Grouping API](about-the-grouping-api.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="7b5d3-114">直接連接可讓節點將私用資料傳送給彼此。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-114">Direct connections allow nodes to send private data to each other.</span></span>

     

## <a name="event-notices"></a><span data-ttu-id="7b5d3-115">事件通知</span><span class="sxs-lookup"><span data-stu-id="7b5d3-115">Event Notices</span></span>

<span data-ttu-id="7b5d3-116">對等圖形 API 有一個事件基礎結構，可讓應用程式在對等圖形 API 基礎結構內註冊及接收對等事件的通知。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-116">The Peer Graphing API has an event infrastructure that allows an application to register and receive notice of a peer event within the Peer Graphing API infrastructure.</span></span> <span data-ttu-id="7b5d3-117">當對等圖形中的某個專案發生變更時，應用程式會傳送事件通知，以識別已發生變更。</span><span class="sxs-lookup"><span data-stu-id="7b5d3-117">When something changes within a peer graph, an application sends an event notice to identify that a change has occurred.</span></span>

 

 



