---
description: 例外狀況是在程式執行期間所發生的事件，而且需要在正常控制流程之外執行程式碼。
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: 結構化例外狀況處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847069"
---
# <a name="structured-exception-handling"></a><span data-ttu-id="9f57c-103">結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="9f57c-103">Structured Exception Handling</span></span>

<span data-ttu-id="9f57c-104">*例外* 狀況是在程式執行期間所發生的事件，而且需要在正常控制流程之外執行程式碼。</span><span class="sxs-lookup"><span data-stu-id="9f57c-104">An *exception* is an event that occurs during the execution of a program, and requires the execution of code outside the normal flow of control.</span></span> <span data-ttu-id="9f57c-105">有兩種例外狀況：硬體例外狀況和軟體例外狀況。</span><span class="sxs-lookup"><span data-stu-id="9f57c-105">There are two kinds of exceptions: hardware exceptions and software exceptions.</span></span> <span data-ttu-id="9f57c-106">CPU 會起始 *硬體例外* 狀況。</span><span class="sxs-lookup"><span data-stu-id="9f57c-106">*Hardware exceptions* are initiated by the CPU.</span></span> <span data-ttu-id="9f57c-107">這可能是因為執行特定的指令序列（例如零除或嘗試存取不正確記憶體位址）所導致。</span><span class="sxs-lookup"><span data-stu-id="9f57c-107">They can result from the execution of certain instruction sequences, such as division by zero or an attempt to access an invalid memory address.</span></span> <span data-ttu-id="9f57c-108">*軟體例外* 狀況是由應用程式或作業系統明確起始。</span><span class="sxs-lookup"><span data-stu-id="9f57c-108">*Software exceptions* are initiated explicitly by applications or the operating system.</span></span> <span data-ttu-id="9f57c-109">例如，當指定了不正確參數值時，系統可以偵測到。</span><span class="sxs-lookup"><span data-stu-id="9f57c-109">For example, the system can detect when an invalid parameter value is specified.</span></span>

<span data-ttu-id="9f57c-110">*結構化例外狀況處理* 是一種處理硬體和軟體例外狀況的機制。</span><span class="sxs-lookup"><span data-stu-id="9f57c-110">*Structured exception handling* is a mechanism for handling both hardware and software exceptions.</span></span> <span data-ttu-id="9f57c-111">因此，您的程式碼將會以相同的方式處理硬體和軟體例外狀況。</span><span class="sxs-lookup"><span data-stu-id="9f57c-111">Therefore, your code will handle hardware and software exceptions identically.</span></span> <span data-ttu-id="9f57c-112">結構化例外狀況處理可讓您完全掌控例外狀況的處理、支援偵錯工具，並且可在所有程式設計語言和電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="9f57c-112">Structured exception handling enables you to have complete control over the handling of exceptions, provides support for debuggers, and is usable across all programming languages and machines.</span></span> <span data-ttu-id="9f57c-113">*向量化例外狀況處理* 是結構化例外狀況處理的延伸。</span><span class="sxs-lookup"><span data-stu-id="9f57c-113">*Vectored exception handling* is an extension to structured exception handling.</span></span>

<span data-ttu-id="9f57c-114">系統也支援 *終止處理*，可讓您確保每當執行受保護的程式碼主體時，也會執行指定的終止程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="9f57c-114">The system also supports *termination handling*, which enables you to ensure that whenever a guarded body of code is executed, a specified block of termination code is also executed.</span></span> <span data-ttu-id="9f57c-115">無論控制流程離開受保護主體的方式為何，都會執行終止程式碼。</span><span class="sxs-lookup"><span data-stu-id="9f57c-115">The termination code is executed regardless of how the flow of control leaves the guarded body.</span></span> <span data-ttu-id="9f57c-116">例如，終止處理常式可保證即使在執行受保護的程式碼主體時發生例外狀況或其他錯誤，也會執行清除工作。</span><span class="sxs-lookup"><span data-stu-id="9f57c-116">For example, a termination handler can guarantee that clean-up tasks are performed even if an exception or some other error occurs while the guarded body of code is being executed.</span></span>

-   [<span data-ttu-id="9f57c-117">關於結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="9f57c-117">About Structured Exception Handling</span></span>](about-structured-exception-handling.md)
-   [<span data-ttu-id="9f57c-118">使用結構化例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="9f57c-118">Using Structured Exception Handling</span></span>](using-structured-exception-handling.md)
-   [<span data-ttu-id="9f57c-119">結構化例外狀況處理參考</span><span class="sxs-lookup"><span data-stu-id="9f57c-119">Structured Exception Handling Reference</span></span>](structured-exception-handling-reference.md)

 

 



