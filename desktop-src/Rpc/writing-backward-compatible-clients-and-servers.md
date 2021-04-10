---
title: 撰寫回溯相容的用戶端和伺服器
description: 理論上，RPC 的版本控制配置有助於防止修改的伺服器和用戶端之間的 miscommunication，以及其部署的對應專案。
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- 遠端程序呼叫 RPC、最佳作法、回溯相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092245"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="91896-104">撰寫回溯相容的用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="91896-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="91896-105">理論上，RPC 的版本控制配置有助於防止修改的伺服器和用戶端之間的 miscommunication，以及其部署的對應專案。</span><span class="sxs-lookup"><span data-stu-id="91896-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="91896-106">不過在實務上，開發人員經常必須在不修改版本的情況下，對現有介面進行變更，因為先前的用戶端和伺服器必須能夠與新的用戶端和伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="91896-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="91896-107">這是比 COM 更大的標準 RPC 問題;查詢是在 COM 中搜尋支援介面的自然方式，但在 RPC 例外狀況處理中，必須用於對等的涵蓋範圍。</span><span class="sxs-lookup"><span data-stu-id="91896-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="91896-108">本節將討論解決這些情況的最佳 RPC 程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="91896-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="91896-109">本節分為下列主題：</span><span class="sxs-lookup"><span data-stu-id="91896-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="91896-110">RPC 和 COM 的版本控制理論</span><span class="sxs-lookup"><span data-stu-id="91896-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="91896-111">以回溯相容的方式變更介面</span><span class="sxs-lookup"><span data-stu-id="91896-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="91896-112">不相容變更的範例</span><span class="sxs-lookup"><span data-stu-id="91896-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




