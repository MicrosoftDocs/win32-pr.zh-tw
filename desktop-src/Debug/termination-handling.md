---
description: 終止處理常式可確保每當控制流程離開特定的受防護程式碼主體時，就會執行特定的程式碼區塊。 終止處理常式是由下列元素所組成。
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: 終止處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e926a47a3c0bb4f2cb8a8df350807aee89b49bab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847304"
---
# <a name="termination-handling"></a><span data-ttu-id="115e6-104">終止處理</span><span class="sxs-lookup"><span data-stu-id="115e6-104">Termination Handling</span></span>

<span data-ttu-id="115e6-105">*終止處理常式* 可確保每當控制流程離開特定的受防護程式碼主體時，就會執行特定的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="115e6-105">A *termination handler* ensures that a specific block of code is executed whenever flow of control leaves a particular guarded body of code.</span></span> <span data-ttu-id="115e6-106">終止處理常式是由下列元素所組成。</span><span class="sxs-lookup"><span data-stu-id="115e6-106">A termination handler consists of the following elements.</span></span>

-   <span data-ttu-id="115e6-107">受保護的程式碼主體</span><span class="sxs-lookup"><span data-stu-id="115e6-107">A guarded body of code</span></span>
-   <span data-ttu-id="115e6-108">當控制流程離開受防護主體時要執行的終止程式碼區塊</span><span class="sxs-lookup"><span data-stu-id="115e6-108">A block of termination code to be executed when the flow of control leaves the guarded body</span></span>

<span data-ttu-id="115e6-109">終止處理常式是以特定語言的語法來宣告。</span><span class="sxs-lookup"><span data-stu-id="115e6-109">Termination handlers are declared in language-specific syntax.</span></span> <span data-ttu-id="115e6-110">使用 Microsoft c/c + + 優化編譯器時，它們會使用 **\_ \_ try** 和 **\_ \_ finally** 來執行。</span><span class="sxs-lookup"><span data-stu-id="115e6-110">Using the Microsoft C/C++ Optimizing Compiler, they are implemented using **\_\_try** and **\_\_finally**.</span></span> <span data-ttu-id="115e6-111">如需詳細資訊，請參閱 [處理常式語法](handler-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="115e6-111">For more information, see [Handler Syntax](handler-syntax.md).</span></span>

<span data-ttu-id="115e6-112">受保護的程式碼主體可以是程式碼區塊、一組嵌套區塊，或整個程式或函式。</span><span class="sxs-lookup"><span data-stu-id="115e6-112">The guarded body of code can be a block of code, a set of nested blocks, or an entire procedure or function.</span></span> <span data-ttu-id="115e6-113">每當執行受保護的主體時，就會執行終止程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="115e6-113">Whenever the guarded body is executed, the block of termination code will be executed.</span></span> <span data-ttu-id="115e6-114">唯一的例外是當執行緒在執行受防護主體期間終止時 (例如，如果從受防護主體) 內呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) 或 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。</span><span class="sxs-lookup"><span data-stu-id="115e6-114">The only exception to this is when the thread terminates during execution of the guarded body (for example, if the [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) or [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function is called from within the guarded body).</span></span>

<span data-ttu-id="115e6-115">當控制權的流程離開受保護的主體時，就會執行終止區塊，不論受防護主體是否正常終止或異常。</span><span class="sxs-lookup"><span data-stu-id="115e6-115">The termination block is executed when the flow of control leaves the guarded body, regardless of whether the guarded body terminated normally or abnormally.</span></span> <span data-ttu-id="115e6-116">當區塊中的最後一個語句執行時，會將受保護的主體視為正常終止，並且控制順序進入終止區塊。</span><span class="sxs-lookup"><span data-stu-id="115e6-116">The guarded body is considered to have terminated normally when the last statement in the block is executed and control proceeds sequentially into the termination block.</span></span> <span data-ttu-id="115e6-117">當控制流程因為例外狀況而離開受保護主體，或由於 **return**、 **goto**、 **break** 或 **continue** 等控制語句而離開受保護主體時，就會發生異常終止。</span><span class="sxs-lookup"><span data-stu-id="115e6-117">Abnormal termination occurs when the flow of control leaves the guarded body due to an exception, or due to a control statement such as **return**, **goto**, **break**, or **continue**.</span></span> <span data-ttu-id="115e6-118">您可以從終止區塊內呼叫 [**AbnormalTermination**](abnormaltermination.md) 函式，以判斷受防護主體是否正常終止。</span><span class="sxs-lookup"><span data-stu-id="115e6-118">The [**AbnormalTermination**](abnormaltermination.md) function can be called from within the termination block to determine whether the guarded body terminated normally.</span></span>

 

 
