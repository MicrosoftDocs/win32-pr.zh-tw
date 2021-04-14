---
title: 非同步 i/o 和非同步 RPC
description: 非同步 i/o 是一個有效率的方法，可讓單一線程同時管理多個 i/o 要求。
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932e85283eb67ff6675a646e791bbce5fe15d65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382621"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a><span data-ttu-id="3ba0c-103">非同步 i/o 和非同步 RPC</span><span class="sxs-lookup"><span data-stu-id="3ba0c-103">Asynchronous I/O and Asynchronous RPC</span></span>

<span data-ttu-id="3ba0c-104">非同步 i/o 是一個有效率的方法，可讓單一線程同時管理多個 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-104">Asynchronous I/O is an efficient means for a single thread to manage multiple I/O requests simultaneously.</span></span> <span data-ttu-id="3ba0c-105">伺服器上的非同步 RPC 完成 RPC 要求的類似用途。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-105">Asynchronous RPC on the server accomplishes a similar purpose for RPC requests.</span></span> <span data-ttu-id="3ba0c-106">在 Windows Vista 之前的 Windows 版本中，不建議使用非同步 RPC 從伺服器程式張貼非同步 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-106">In versions of Windows prior to Windows Vista, posting asynchronous I/O requests from server procedures using asynchronous RPC is discouraged.</span></span> <span data-ttu-id="3ba0c-107">不過，在 Windows Vista 和更新版本的 Windows 中，非同步 RPC 也支援與 i/o 完成埠相關聯的非同步 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-107">However, in Windows Vista and later versions of Windows, asynchronous I/O requests that are associated with an I/O completion port are supported by asynchronous RPC.</span></span>

<span data-ttu-id="3ba0c-108">在 Windows Vista 之前，非同步遠端程序呼叫可能會在非同步 i/o 要求完成之前完成。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-108">Prior to Windows Vista, an asynchronous remote procedure call may complete before the asynchronous I/O request completes.</span></span> <span data-ttu-id="3ba0c-109">當非同步呼叫完成時，如果 RPC 執行時間決定它有足夠的執行緒可用來服務預期的工作負載，則其執行緒可能會終止。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-109">When the asynchronous call completes, its thread may terminate if the RPC runtime decides it has enough threads available to service the expected workload.</span></span> <span data-ttu-id="3ba0c-110">系統會將所有 i/o 要求系結至起始這些要求的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-110">The system binds all I/O requests to the thread that initiates them.</span></span> <span data-ttu-id="3ba0c-111">如果執行緒終止，則會中止該執行緒上暫止的所有 i/o 要求。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-111">If the thread terminates, any I/O requests pending on that thread are aborted.</span></span> <span data-ttu-id="3ba0c-112">暫止 i/o 要求無法移至另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-112">Pending I/O requests cannot be moved to another thread.</span></span>

<span data-ttu-id="3ba0c-113">因此，以 Windows Vista 之前的 Windows 版本為目標的應用程式設計工具可以在伺服器程式中使用同步 i/o，也可以將所有牽涉到非同步 i/o 的要求轉送到應用程式所管理之執行緒集區上執行的程式。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-113">Therefore, application designers targeting versions of Windows prior to Windows Vista can either use synchronous I/O in server procedures, or they can forward all requests that involve asynchronous I/O to procedures executing on a thread pool that the application manages.</span></span> <span data-ttu-id="3ba0c-114">Windows API 提供執行緒集區管理的功能。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-114">The Windows API provides functions for thread-pool management.</span></span> <span data-ttu-id="3ba0c-115">請參閱 [進程和執行緒函數](/windows/desktop/ProcThread/process-and-thread-functions)。</span><span class="sxs-lookup"><span data-stu-id="3ba0c-115">See [Process and Thread Functions](/windows/desktop/ProcThread/process-and-thread-functions).</span></span>

 

 