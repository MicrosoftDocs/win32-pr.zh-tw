---
description: Assert 和中斷點宏
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Assert 和中斷點宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109733"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="99071-103">Assert 和中斷點宏</span><span class="sxs-lookup"><span data-stu-id="99071-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="99071-104">[DirectShow 基類](directshow-base-classes.md)提供數個執行判斷提示或導致中斷點的宏。</span><span class="sxs-lookup"><span data-stu-id="99071-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="99071-105">巨集</span><span class="sxs-lookup"><span data-stu-id="99071-105">Macro</span></span>                                        | <span data-ttu-id="99071-106">Description</span><span class="sxs-lookup"><span data-stu-id="99071-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99071-107">**斷言**</span><span class="sxs-lookup"><span data-stu-id="99071-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="99071-108">評估運算式，並在運算式為 **FALSE** 時顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="99071-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="99071-109">**DbgAssertAligned**</span><span class="sxs-lookup"><span data-stu-id="99071-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="99071-110">測試指標是否對齊指定的界限。</span><span class="sxs-lookup"><span data-stu-id="99071-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="99071-111">**DbgBreak**</span><span class="sxs-lookup"><span data-stu-id="99071-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="99071-112">使用指定的字串、來源檔案的名稱和行號，顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="99071-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="99071-113">**EXECUTE \_ ASSERT**</span><span class="sxs-lookup"><span data-stu-id="99071-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="99071-114">評估 debug 和 retail 組建中的運算式。</span><span class="sxs-lookup"><span data-stu-id="99071-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="99071-115">在 [偵錯工具] 組建中，如果運算式為 **FALSE**，則會顯示診斷訊息。</span><span class="sxs-lookup"><span data-stu-id="99071-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="99071-116">**KASSERT**</span><span class="sxs-lookup"><span data-stu-id="99071-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="99071-117">評估運算式，並在運算式為 **FALSE** 時引發中斷點例外狀況。</span><span class="sxs-lookup"><span data-stu-id="99071-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="99071-118">**KDbgBreak**</span><span class="sxs-lookup"><span data-stu-id="99071-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="99071-119">導致中斷點例外狀況，並記錄指定的字串。</span><span class="sxs-lookup"><span data-stu-id="99071-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="99071-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="99071-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99071-121">偵錯工具</span><span class="sxs-lookup"><span data-stu-id="99071-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



