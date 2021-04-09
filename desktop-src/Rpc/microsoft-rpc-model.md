---
title: RPC 模型
description: C 和 c + + 程式設計語言 (RPC) 的遠端程序呼叫，其設計目的是為了協助滿足開發人員在 Windows 作業系統下一代軟體的需求。
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- 遠端程序呼叫 RPC （說明） RPC 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682886"
---
# <a name="the-rpc-model"></a><span data-ttu-id="349d3-104">RPC 模型</span><span class="sxs-lookup"><span data-stu-id="349d3-104">The RPC Model</span></span>

<span data-ttu-id="349d3-105">C 和 c + + 程式設計語言 (RPC) 的遠端程序呼叫，其設計目的是為了協助滿足開發人員在 Windows 作業系統下一代軟體的需求。</span><span class="sxs-lookup"><span data-stu-id="349d3-105">Remote Procedure Call (RPC) for the C and C++ programming languages is designed to help meet the needs of developers working on the next generation of software for Windows operating systems.</span></span>

<span data-ttu-id="349d3-106">RPC 是一種功能強大、穩固、有效率且安全的處理序間通訊 (IPC) 機制，可讓您在不同的進程中進行資料交換和叫用功能。</span><span class="sxs-lookup"><span data-stu-id="349d3-106">RPC is a powerful, robust, efficient, and secure interprocess communication (IPC) mechanism that enables data exchange and invocation of functionality residing in a different process.</span></span> <span data-ttu-id="349d3-107">不同的進程可以位於相同電腦、區域網路或網際網路上。</span><span class="sxs-lookup"><span data-stu-id="349d3-107">That different process can be on the same machine, on the local area network, or across the Internet.</span></span> <span data-ttu-id="349d3-108">本節說明 RPC 程式設計模型，以及可使用 RPC 來執行之分散式系統的模型。</span><span class="sxs-lookup"><span data-stu-id="349d3-108">This section explains the RPC programming model and the model for distributed systems that can be implemented using RPC.</span></span>

<span data-ttu-id="349d3-109">RPC 完全支援64位 Windows。</span><span class="sxs-lookup"><span data-stu-id="349d3-109">RPC fully supports 64-bit Windows.</span></span> <span data-ttu-id="349d3-110">有三種類型的進程：原生32位程式、原生64位處理常式，以及在64位系統上以32位程式模擬器執行的32位處理常式 (通常稱為 WOW64 進程) 。</span><span class="sxs-lookup"><span data-stu-id="349d3-110">There are three types of processes: native 32-bit processes, native 64-bit processes, and 32-bit processes running under the 32-bit process emulator on a 64-bit system (often referred to as WOW64 processes).</span></span> <span data-ttu-id="349d3-111">如需 WOW64 的詳細資訊，請參閱執行 [32 位應用程式](/windows/desktop/WinProg64/running-32-bit-applications)。</span><span class="sxs-lookup"><span data-stu-id="349d3-111">For more information about WOW64, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span> <span data-ttu-id="349d3-112">使用 RPC，開發人員可以在不同類型的進程之間透明地通訊;RPC 會自動管理幕後的進程差異。</span><span class="sxs-lookup"><span data-stu-id="349d3-112">Using RPC, developers can transparently communicate between different types of process; RPC automatically manages process differences behind the scenes.</span></span>

<span data-ttu-id="349d3-113">RPC 最初開發為憑證 RPC 的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="349d3-113">RPC was initially developed as an extension to OSF RPC.</span></span> <span data-ttu-id="349d3-114">除了部分的 advanced 功能之外，RPC 也可與其他廠商的憑證 RPC 實現互通。</span><span class="sxs-lookup"><span data-stu-id="349d3-114">With the exception of some of its advanced features, RPC is interoperable with other vendors' implementations of OSF RPC.</span></span>

<span data-ttu-id="349d3-115">本節也提供 RPC 元件及其操作的總覽。</span><span class="sxs-lookup"><span data-stu-id="349d3-115">This section also provides an overview of RPC components and their operation.</span></span> <span data-ttu-id="349d3-116">下列主題將提供此資訊：</span><span class="sxs-lookup"><span data-stu-id="349d3-116">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="349d3-117">程式設計模型</span><span class="sxs-lookup"><span data-stu-id="349d3-117">The Programming Model</span></span>](the-programming-model.md)
-   [<span data-ttu-id="349d3-118">分散式系統的模型</span><span class="sxs-lookup"><span data-stu-id="349d3-118">The Model for Distributed Systems</span></span>](the-model-for-distributed-systems.md)
-   [<span data-ttu-id="349d3-119">RPC 的運作方式</span><span class="sxs-lookup"><span data-stu-id="349d3-119">How RPC Works</span></span>](how-rpc-works.md)
-   [<span data-ttu-id="349d3-120">Microsoft RPC 元件</span><span class="sxs-lookup"><span data-stu-id="349d3-120">Microsoft RPC Components</span></span>](microsoft-rpc-components.md)

 

 