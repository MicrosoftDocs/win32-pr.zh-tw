---
description: 下列清單包含 TAPI MSP 設計目標。
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: 一般設計目標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972451"
---
# <a name="general-design-goals"></a><span data-ttu-id="11d65-103">一般設計目標</span><span class="sxs-lookup"><span data-stu-id="11d65-103">General Design Goals</span></span>

<span data-ttu-id="11d65-104">下列清單包含 TAPI MSP 設計目標。</span><span class="sxs-lookup"><span data-stu-id="11d65-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="11d65-105">基類已保持簡單，只有在絕對必要時才會引進成員和方法。</span><span class="sxs-lookup"><span data-stu-id="11d65-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="11d65-106">簡單的繼承。</span><span class="sxs-lookup"><span data-stu-id="11d65-106">Simple inheritance.</span></span> <span data-ttu-id="11d65-107">類別之間不會有多重繼承，不過介面會使用多個繼承。</span><span class="sxs-lookup"><span data-stu-id="11d65-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="11d65-108">鎖定只會在一個方向進行，以防止鎖死。</span><span class="sxs-lookup"><span data-stu-id="11d65-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="11d65-109">呼叫物件上需要鎖定呼叫的方法，可能會在資料流程上呼叫需要鎖定的方法。</span><span class="sxs-lookup"><span data-stu-id="11d65-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="11d65-110">不過，資料流程上需要鎖定的方法永遠不會呼叫呼叫上需要鎖定的方法。</span><span class="sxs-lookup"><span data-stu-id="11d65-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="11d65-111">Refcounts 可用來保護存取。</span><span class="sxs-lookup"><span data-stu-id="11d65-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="11d65-112">所有張貼到執行緒集區的回呼都有 refcounts。</span><span class="sxs-lookup"><span data-stu-id="11d65-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="11d65-113">Refcount 會在等候取消時取消。</span><span class="sxs-lookup"><span data-stu-id="11d65-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="11d65-114">位址物件在終端機上有 refcounts。</span><span class="sxs-lookup"><span data-stu-id="11d65-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="11d65-115">呼叫物件具有位址和資料流程上的 refcounts。</span><span class="sxs-lookup"><span data-stu-id="11d65-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="11d65-116">資料流程物件具有呼叫和終端機的 refcounts。</span><span class="sxs-lookup"><span data-stu-id="11d65-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="11d65-117">終端機已 refcounts 資料流程。</span><span class="sxs-lookup"><span data-stu-id="11d65-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="11d65-118">呼叫位址和呼叫物件的 shutdown 方法時，迴圈 refcounts 中斷。</span><span class="sxs-lookup"><span data-stu-id="11d65-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



