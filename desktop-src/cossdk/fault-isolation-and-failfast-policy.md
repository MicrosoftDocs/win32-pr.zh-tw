---
description: 錯誤隔離和 Failfast 原則
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: 錯誤隔離和 Failfast 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510519"
---
# <a name="fault-isolation-and-failfast-policy"></a><span data-ttu-id="63c72-103">錯誤隔離和 Failfast 原則</span><span class="sxs-lookup"><span data-stu-id="63c72-103">Fault Isolation and Failfast Policy</span></span>

<span data-ttu-id="63c72-104">COM + 會執行廣泛的內部完整性和一致性檢查。</span><span class="sxs-lookup"><span data-stu-id="63c72-104">COM+ performs extensive internal integrity and consistency checks.</span></span> <span data-ttu-id="63c72-105">如果 COM + 遇到未預期的內部錯誤狀況，則會立即終止進程。</span><span class="sxs-lookup"><span data-stu-id="63c72-105">If COM+ encounters an unexpected internal error condition, it immediately terminates the process.</span></span> <span data-ttu-id="63c72-106">這個稱為 *failfast* 的原則可加速錯誤內含專案，並產生更可靠且健全的系統。</span><span class="sxs-lookup"><span data-stu-id="63c72-106">This policy, called *failfast*, facilitates fault containment and results in more reliable and robust systems.</span></span>

<span data-ttu-id="63c72-107">請考慮 COM + 偵測到其中一個資料結構處於損毀狀態的情況。</span><span class="sxs-lookup"><span data-stu-id="63c72-107">Consider a case in which COM+ detects that one of its data structures is in a corrupted state.</span></span> <span data-ttu-id="63c72-108">此時，原因和損毀的程度都不明，但不幸的是，COM + 無法分辨損毀的分散程度。</span><span class="sxs-lookup"><span data-stu-id="63c72-108">At this point, both the cause and the magnitude of the corruption are unknown and, unfortunately, COM+ cannot tell how far the damage has spread.</span></span> <span data-ttu-id="63c72-109">不過，雖然 COM + 處於不定狀態，但它並不會在隔離的情況下執行。</span><span class="sxs-lookup"><span data-stu-id="63c72-109">However, even though COM+ is in an indeterminate state, it does not run in isolation.</span></span> <span data-ttu-id="63c72-110">就像其他 Dll 一樣，它是裝載在進程環境中，並與主要程式可執行檔和許多其他 Dll 共用單一位址空間。</span><span class="sxs-lookup"><span data-stu-id="63c72-110">Like other DLLs, it is hosted in a process environment and shares a single address space with the main program executable and many other DLLs.</span></span> <span data-ttu-id="63c72-111">因此，COM + 會假設整個程式已損毀，而且程式會立即終止，以防止它將可能損毀的資訊散佈到其他進程，或更糟的是，不允許認可損毀的資料並使其成為持久的。</span><span class="sxs-lookup"><span data-stu-id="63c72-111">Therefore, COM+ assumes that the entire process has been corrupted, and the process is immediately terminated to prevent it from spreading potentially corrupted information to other processes or, worse yet, from allowing corrupted data to be committed and made durable.</span></span>

<span data-ttu-id="63c72-112">COM + 不允許在內容外傳播例外狀況。</span><span class="sxs-lookup"><span data-stu-id="63c72-112">COM+ does not allow exceptions to propagate outside of a context.</span></span> <span data-ttu-id="63c72-113">如果在 COM + 內容中執行時發生例外狀況，而且應用程式在從內容傳回之前未攔截到例外狀況，COM + 會攔截例外狀況並結束進程。</span><span class="sxs-lookup"><span data-stu-id="63c72-113">If an exception occurs while executing within a COM+ context and the application doesn't catch the exception before returning from the context, COM+ catches the exception and terminates the process.</span></span> <span data-ttu-id="63c72-114">在此情況下，使用 failfast 原則是以例外狀況將進程置於不定狀態的假設為基礎。繼續處理並不安全。</span><span class="sxs-lookup"><span data-stu-id="63c72-114">Using the failfast policy in this case is based on the assumption that the exception has put the process into an indeterminate state; it is not safe to continue processing.</span></span>

<span data-ttu-id="63c72-115">如果您是開發人員或系統管理員，您應該檢查事件檢視器的應用程式記錄檔，以取得任何 failfast 動作或嚴重應用程式錯誤的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="63c72-115">As a developer or administrator, you should inspect the Event Viewer application log for details on any failfast action or serious application errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63c72-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="63c72-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63c72-117">找出錯誤的來源</span><span class="sxs-lookup"><span data-stu-id="63c72-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="63c72-118">COM + 如何修改傳回值</span><span class="sxs-lookup"><span data-stu-id="63c72-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="63c72-119">解讀錯誤碼</span><span class="sxs-lookup"><span data-stu-id="63c72-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="63c72-120">在 COM + 中處理錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="63c72-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="63c72-121">疑難排解</span><span class="sxs-lookup"><span data-stu-id="63c72-121">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



