---
description: 撰寫元件最有問題的部分是處理可能的錯誤。
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: 在 COM + 中處理錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111677"
---
# <a name="handling-errors-in-com"></a><span data-ttu-id="c1999-103">在 COM + 中處理錯誤</span><span class="sxs-lookup"><span data-stu-id="c1999-103">Handling Errors in COM+</span></span>

<span data-ttu-id="c1999-104">撰寫元件最有問題的部分是處理可能的錯誤。</span><span class="sxs-lookup"><span data-stu-id="c1999-104">The most problematic part of writing components is dealing with possible errors.</span></span> <span data-ttu-id="c1999-105">在最佳情況下，嘗試判斷發生錯誤的原因，以及應採取的動作可能會很困難。</span><span class="sxs-lookup"><span data-stu-id="c1999-105">Trying to determine what can go wrong and what to do about it can be challenging under the best conditions.</span></span> <span data-ttu-id="c1999-106">您的元件可能會檢查和處理的常見錯誤是失敗的網路連線、安全性錯誤，以及與無法連線之物件相關聯的失敗。</span><span class="sxs-lookup"><span data-stu-id="c1999-106">Common errors that your component might check for and handle are failed network connections, security errors, and failures associated with unreachable objects.</span></span>

<span data-ttu-id="c1999-107">此外，您可以開發自己的錯誤碼來報告介面特定的錯誤，例如違反商務規則時。</span><span class="sxs-lookup"><span data-stu-id="c1999-107">Additionally, you can develop your own error codes to report interface-specific errors such as when a business rule has been violated.</span></span>

<span data-ttu-id="c1999-108">為了保持 COM + 程式設計模型，物件可以 (，而且通常會) 呼叫其他物件上的介面方法來執行工作。</span><span class="sxs-lookup"><span data-stu-id="c1999-108">In keeping with the COM+ programming model, an object can (and often does) call interface methods on other objects to perform work.</span></span> <span data-ttu-id="c1999-109">因為程式設計人員可以用不同的程式設計語言撰寫元件，所以 COM + 要求所有錯誤處理機制都必須是語言中立的，例如： Hresult 和 [**ErrorInfo**](errorinfo.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="c1999-109">Because programmers can write components in different programming languages, COM+ requires that all error-handling mechanisms be language-neutral, for example: HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span>

<span data-ttu-id="c1999-110">本節包含下表所述的主題，這些主題會討論在 COM + 應用程式中處理錯誤的技巧、COM + 中影響失敗行為的功能，以及診斷 COM + 錯誤的建議。</span><span class="sxs-lookup"><span data-stu-id="c1999-110">This section includes topics, described in the following table, that discuss techniques for handling errors in COM+ applications, features in COM+ that affect failure behavior, and suggestions for diagnosing COM+ errors.</span></span>



| <span data-ttu-id="c1999-111">主題</span><span class="sxs-lookup"><span data-stu-id="c1999-111">Topic</span></span>                                                                                           | <span data-ttu-id="c1999-112">描述</span><span class="sxs-lookup"><span data-stu-id="c1999-112">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1999-113">在 COM + 中處理錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="c1999-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)<br/> | <span data-ttu-id="c1999-114">列出並描述在 COM + 中處理錯誤的基本指導方針，包括使用 Hresult 和 [**ErrorInfo**](errorinfo.md) 集合的時機。</span><span class="sxs-lookup"><span data-stu-id="c1999-114">Lists and describes basic guidelines for handling errors in COM+, including when to use HRESULTs and [**ErrorInfo**](errorinfo.md) collections.</span></span><br/> |
| [<span data-ttu-id="c1999-115">COM + 如何修改傳回值</span><span class="sxs-lookup"><span data-stu-id="c1999-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)<br/>               | <span data-ttu-id="c1999-116">識別 COM + 將標準 HRESULT 轉換回呼叫端之前，會將標準 HRESULT 轉換成 COM + 錯誤碼的單一條件。</span><span class="sxs-lookup"><span data-stu-id="c1999-116">Identifies the single condition in which COM+ converts a standard HRESULT to a COM+ error code before passing it back to the caller.</span></span><br/>             |
| [<span data-ttu-id="c1999-117">錯誤隔離和 Failfast 原則</span><span class="sxs-lookup"><span data-stu-id="c1999-117">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)<br/>       | <span data-ttu-id="c1999-118">顯示錯誤隔離和 failfast 原則如何影響 COM + 行為。</span><span class="sxs-lookup"><span data-stu-id="c1999-118">Shows how fault isolation and the failfast policy affect COM+ behavior.</span></span><br/>                                                                          |
| [<span data-ttu-id="c1999-119">找出錯誤的來源</span><span class="sxs-lookup"><span data-stu-id="c1999-119">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)<br/>                 | <span data-ttu-id="c1999-120">說明如何診斷來源，以及取得應用程式錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="c1999-120">Describes how you can diagnose the source and obtain a description of application errors.</span></span> <br/>                                                       |
| [<span data-ttu-id="c1999-121">解讀錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c1999-121">Interpreting Error Codes</span></span>](interpreting-error-codes.md)<br/>                             | <span data-ttu-id="c1999-122">識別 Microsoft Visual C++、JAVA 語言和 Microsoft Visual Basic 的主流錯誤處理機制。</span><span class="sxs-lookup"><span data-stu-id="c1999-122">Identifies the predominant error-handling mechanism for Microsoft Visual C++, the Java language, and Microsoft Visual Basic.</span></span> <br/>                    |
| [<span data-ttu-id="c1999-123">疑難排解</span><span class="sxs-lookup"><span data-stu-id="c1999-123">Troubleshooting</span></span>](troubleshooting.md)<br/>                                               | <span data-ttu-id="c1999-124">提供診斷錯誤的其他協助。</span><span class="sxs-lookup"><span data-stu-id="c1999-124">Provides additional assistance in diagnosing errors.</span></span><br/>                                                                                             |
| [<span data-ttu-id="c1999-125">聯絡支援</span><span class="sxs-lookup"><span data-stu-id="c1999-125">Contacting Support</span></span>](contacting-support.md)<br/>                                         | <span data-ttu-id="c1999-126">識別在聯繫支援人員時應提供的重要問題解決資訊。</span><span class="sxs-lookup"><span data-stu-id="c1999-126">Identifies important problem-solving information you should provide when contacting support.</span></span><br/>                                                     |



 

<span data-ttu-id="c1999-127">如需處理與各種 COM + 服務相關聯之錯誤的詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="c1999-127">For detailed information on handling errors associated with various COM+ services, see the following sections:</span></span>

-   [<span data-ttu-id="c1999-128">藉由通知根物件來加速交易</span><span class="sxs-lookup"><span data-stu-id="c1999-128">Speeding Transactions by Notifying the Root Object</span></span>](speeding-transactions-by-notifying-the-root-object.md)
-   <span data-ttu-id="c1999-129">[處理](handling-errors-in-queued-components.md) 佇列元件的錯誤 () </span><span class="sxs-lookup"><span data-stu-id="c1999-129">[Handling Errors](handling-errors-in-queued-components.md) (for queued components)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1999-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1999-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1999-131">偵錯工具 COM + 應用程式</span><span class="sxs-lookup"><span data-stu-id="c1999-131">Debugging COM+ Applications</span></span>](debugging-com--applications.md)
</dt> </dl>

 

 




