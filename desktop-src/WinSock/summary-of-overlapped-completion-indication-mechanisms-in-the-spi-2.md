---
description: Windows 通訊端中重迭的完成指示機制的摘要， (Winsock) SPI。
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: SPI 中重迭完成指示機制的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113000"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="97a49-103">SPI 中重迭完成指示機制的摘要</span><span class="sxs-lookup"><span data-stu-id="97a49-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="97a49-104">下表摘要說明重迭通訊端的完成語義，顯示各種 *lpOverlapped*、 **hEvent** 和 *lpCompletionRoutine* 的組合。</span><span class="sxs-lookup"><span data-stu-id="97a49-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="97a49-105">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="97a49-105">*lpOverlapped*</span></span> | <span data-ttu-id="97a49-106">**hEvent**</span><span class="sxs-lookup"><span data-stu-id="97a49-106">**hEvent**</span></span>     | <span data-ttu-id="97a49-107">*lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="97a49-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="97a49-108">完成指示</span><span class="sxs-lookup"><span data-stu-id="97a49-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a49-109">NULL</span><span class="sxs-lookup"><span data-stu-id="97a49-109">NULL</span></span>           | <span data-ttu-id="97a49-110">不適用</span><span class="sxs-lookup"><span data-stu-id="97a49-110">Not applicable</span></span> | <span data-ttu-id="97a49-111">忽略</span><span class="sxs-lookup"><span data-stu-id="97a49-111">Ignored</span></span>               | <span data-ttu-id="97a49-112">作業會以同步方式完成，也就是說，它的行為會如同 nonoverlapped 通訊端一樣。</span><span class="sxs-lookup"><span data-stu-id="97a49-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="97a49-113">非 Null</span><span class="sxs-lookup"><span data-stu-id="97a49-113">not NULL</span></span>       | <span data-ttu-id="97a49-114">NULL</span><span class="sxs-lookup"><span data-stu-id="97a49-114">NULL</span></span>           | <span data-ttu-id="97a49-115">NULL</span><span class="sxs-lookup"><span data-stu-id="97a49-115">NULL</span></span>                  | <span data-ttu-id="97a49-116">作業已完成重迭，但沒有 Windows 通訊端2支援的完成機制。</span><span class="sxs-lookup"><span data-stu-id="97a49-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="97a49-117">完成埠機制 (如果在此情況下可以使用支援的) ，否則就不會有完成通知。</span><span class="sxs-lookup"><span data-stu-id="97a49-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="97a49-118">非 Null</span><span class="sxs-lookup"><span data-stu-id="97a49-118">not NULL</span></span>       | <span data-ttu-id="97a49-119">非 Null</span><span class="sxs-lookup"><span data-stu-id="97a49-119">not NULL</span></span>       | <span data-ttu-id="97a49-120">NULL</span><span class="sxs-lookup"><span data-stu-id="97a49-120">NULL</span></span>                  | <span data-ttu-id="97a49-121">作業完成重迭，由訊號事件物件發出通知。</span><span class="sxs-lookup"><span data-stu-id="97a49-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="97a49-122">非 Null</span><span class="sxs-lookup"><span data-stu-id="97a49-122">not NULL</span></span>       | <span data-ttu-id="97a49-123">忽略</span><span class="sxs-lookup"><span data-stu-id="97a49-123">Ignored</span></span>        | <span data-ttu-id="97a49-124">非 Null</span><span class="sxs-lookup"><span data-stu-id="97a49-124">not NULL</span></span>              | <span data-ttu-id="97a49-125">作業完成重迭，藉由排程完成常式來通知。</span><span class="sxs-lookup"><span data-stu-id="97a49-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



