---
description: 如果執行緒正在等候核心模式回呼完成，執行緒的使用者模式端將會在呼叫 ZwCallbackReturn 函數時延遲。
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: 偵測 Kernel-Mode 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936402"
---
# <a name="detecting-kernel-mode-callbacks"></a><span data-ttu-id="a2baa-103">偵測 Kernel-Mode 回呼</span><span class="sxs-lookup"><span data-stu-id="a2baa-103">Detecting Kernel-Mode Callbacks</span></span>

<span data-ttu-id="a2baa-104">大部分的 Windows 作業系統程式碼都是以核心模式執行。</span><span class="sxs-lookup"><span data-stu-id="a2baa-104">Most of the code for the Windows operating system runs in kernel mode.</span></span> <span data-ttu-id="a2baa-105">每當應用程式執行緒從 Windows API 呼叫函式，而該函式接著呼叫必須在核心模式中執行的內部系統函數時，處理器模式就會從使用者模式切換到核心模式。</span><span class="sxs-lookup"><span data-stu-id="a2baa-105">The processor mode switches from user mode to kernel mode whenever an application thread calls a function from the Windows API that in turn calls an internal system function that must execute in kernel mode.</span></span> <span data-ttu-id="a2baa-106">在控制權回到函式之前，處理器模式會回到使用者模式，以便保護系統資料。</span><span class="sxs-lookup"><span data-stu-id="a2baa-106">The processor mode returns to user mode before control returns to the function so that the system data is protected.</span></span>

<span data-ttu-id="a2baa-107">如果執行緒正在等候核心模式回呼完成，執行緒的使用者模式端將會在呼叫 **ZwCallbackReturn** 函數時延遲。</span><span class="sxs-lookup"><span data-stu-id="a2baa-107">If a thread is waiting for a kernel-mode callback to complete, the user-mode side of the thread will delay at a call to the **ZwCallbackReturn** function.</span></span>

 

 



