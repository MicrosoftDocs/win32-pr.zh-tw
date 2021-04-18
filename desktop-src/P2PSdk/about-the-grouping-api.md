---
description: 對等群組 API 結合了 PNRP 命名空間提供者 API 和圖形 API 的技術。
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: 關於群組 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989414"
---
# <a name="about-the-grouping-api"></a><span data-ttu-id="6cfc7-103">關於群組 API</span><span class="sxs-lookup"><span data-stu-id="6cfc7-103">About the Grouping API</span></span>

<span data-ttu-id="6cfc7-104">對等群組 API 結合了 [PNRP 命名空間提供者 api](pnrp-namespace-provider-api.md) 和 [圖形 API](graphing-api.md)的技術。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-104">The Peer Grouping API combines the technology of the [PNRP Name Space Provider API](pnrp-namespace-provider-api.md) and the [Graphing API](graphing-api.md).</span></span> <span data-ttu-id="6cfc7-105">群組新增下列兩項技術：</span><span class="sxs-lookup"><span data-stu-id="6cfc7-105">Grouping adds the following two pieces of technology:</span></span>

-   <span data-ttu-id="6cfc7-106">多工層，可讓多個應用程式使用一個圖形、一個埠和一個記錄資料庫。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-106">A multiplexing layer that allows multiple applications to use one graph, one port, and one record database.</span></span>
-   <span data-ttu-id="6cfc7-107">安全性可確保只有受邀加入群組的對等，才能在群組的整個存留期內加入並連接。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-107">Security that ensures only peers invited to a group can join and connect throughout the lifetime of a group.</span></span>

<span data-ttu-id="6cfc7-108">分組可讓您輕鬆存取對等網路，因為直接呼叫流程和安全訊息。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-108">Grouping provides an accessible and easy approach to peer networking because of the straightforward call flow and secure messaging.</span></span> <span data-ttu-id="6cfc7-109">此 API 會使用 PNRP 進行群組探索和標準 PKI 型安全性提供者，而不需要開發人員執行。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-109">This API utilizes PNRP for group discovery and a standard PKI-based security provider instead of requiring a developer to implement one.</span></span> <span data-ttu-id="6cfc7-110">但是，如果您的應用程式在安全性選項方面要求更大的彈性，請考慮使用 [圖形 API](about-the-graphing-api.md)。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-110">However, if your application demands greater flexibility in terms of security options, consider using the [Graphing API](about-the-graphing-api.md).</span></span>

<span data-ttu-id="6cfc7-111">下表識別此群組 API 區段中的主題：</span><span class="sxs-lookup"><span data-stu-id="6cfc7-111">The following table identifies the topics in this Grouping API section:</span></span>

| <span data-ttu-id="6cfc7-112">主題</span><span class="sxs-lookup"><span data-stu-id="6cfc7-112">Topic</span></span>                                                                | <span data-ttu-id="6cfc7-113">描述</span><span class="sxs-lookup"><span data-stu-id="6cfc7-113">Description</span></span>                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cfc7-114">如何使用群組</span><span class="sxs-lookup"><span data-stu-id="6cfc7-114">How to Work With Groups</span></span>](how-to-work-with-groups.md)               | <span data-ttu-id="6cfc7-115">說明對等群組應用程式中從啟動到關機的呼叫流程。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-115">Describes the call flow in a Peer Grouping application from startup to shutdown.</span></span>         |
| [<span data-ttu-id="6cfc7-116">群組安全性的運作方式</span><span class="sxs-lookup"><span data-stu-id="6cfc7-116">How Group Security Works</span></span>](how-group-security-works.md)             | <span data-ttu-id="6cfc7-117">描述對等群組成員資格和資料交換如何受到保護。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-117">Describes how peer group membership and data exchanges are secured.</span></span>                      |
| [<span data-ttu-id="6cfc7-118">邀請對等群組</span><span class="sxs-lookup"><span data-stu-id="6cfc7-118">Inviting a Peer to a Group</span></span>](inviting-a-peer-to-a-group.md)         | <span data-ttu-id="6cfc7-119">描述對等受邀並新增至對等群組的進程。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-119">Describes the process by which peers are invited and added to a peer group.</span></span>              |
| [<span data-ttu-id="6cfc7-120">如何連接至對等群組</span><span class="sxs-lookup"><span data-stu-id="6cfc7-120">How to Connect to a Peer Group</span></span>](how-to-connect-to-a-peer-group.md) | <span data-ttu-id="6cfc7-121">描述對等互連如何連接至對等群組並與之互動。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-121">Describes how a peer connects to and interacts with a peer group.</span></span>                        |
| [<span data-ttu-id="6cfc7-122">管理群組記錄</span><span class="sxs-lookup"><span data-stu-id="6cfc7-122">Managing Group Records</span></span>](managing-group-records.md)                 | <span data-ttu-id="6cfc7-123">描述對等群組記錄，以及如何以成員和系統管理員的身分來管理它們。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-123">Describes peer group records and how to manage them as a member and as an administrator.</span></span> |



 

> [!Note]  
> <span data-ttu-id="6cfc7-124">在具有防火牆的環境中使用群組 API 的應用程式需要例外狀況群組，其中涵蓋應用程式專屬的埠，以及適用于 PNRP 的群組 API 和3540埠 ' 3587-TCP ' 的埠 '-TCP '。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-124">Applications using the Grouping API in an environment with a firewall require exception groups that cover the port specific to the application, as well as port '3587-TCP' for the Grouping API and port '3540-UDP' for PNRP.</span></span> <span data-ttu-id="6cfc7-125">每當應用程式執行時，都應啟用這些例外狀況群組。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-125">These exception groups should be enabled whenever the application is running.</span></span>

 

 

 



