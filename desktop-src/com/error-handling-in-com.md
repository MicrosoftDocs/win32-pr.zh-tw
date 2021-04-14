---
title: COM (COM) 中的錯誤處理
description: COM 中的錯誤處理
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464169"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="41fb9-103">COM (COM) 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="41fb9-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="41fb9-104">幾乎所有的 COM 函數和介面方法都會傳回類型 **HRESULT** 的值。</span><span class="sxs-lookup"><span data-stu-id="41fb9-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="41fb9-105">*結果控制碼* 的 **HRESULT** (，) 是傳回成功、警告和錯誤值的方法。</span><span class="sxs-lookup"><span data-stu-id="41fb9-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="41fb9-106">**HRESULT** 其實不會處理任何事項;它們只是值中有數個欄位編碼的值。</span><span class="sxs-lookup"><span data-stu-id="41fb9-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="41fb9-107">根據 COM 規格，零的結果表示成功，而非零的結果表示失敗。</span><span class="sxs-lookup"><span data-stu-id="41fb9-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="41fb9-108">在原始程式碼層級，所有錯誤值都包含三個部分，以底線分隔。</span><span class="sxs-lookup"><span data-stu-id="41fb9-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="41fb9-109">第一個部分是識別與錯誤相關聯之設備的前置詞，第二個部分是 E 表示錯誤，而第三個部分是描述實際條件的字串。</span><span class="sxs-lookup"><span data-stu-id="41fb9-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="41fb9-110">例如，當硬碟上沒有剩餘空間時，就會傳回 **Stg. \_ E \_ MEDIUMFULL** 。</span><span class="sxs-lookup"><span data-stu-id="41fb9-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="41fb9-111">**Stg.** 前置詞表示儲存設備， **E** 表示狀態碼代表錯誤，而 **MEDIUMFULL** 則會提供有關錯誤的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="41fb9-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="41fb9-112">您可能想要從介面方法或函式傳回的許多值都是在 Winerror.h 中定義。</span><span class="sxs-lookup"><span data-stu-id="41fb9-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="41fb9-113">如需有關錯誤處理的詳細資訊，請參閱下列各節：</span><span class="sxs-lookup"><span data-stu-id="41fb9-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="41fb9-114">COM 錯誤碼的結構</span><span class="sxs-lookup"><span data-stu-id="41fb9-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="41fb9-115">設備 ITF 中的代碼 \_</span><span class="sxs-lookup"><span data-stu-id="41fb9-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="41fb9-116">使用宏進行錯誤處理</span><span class="sxs-lookup"><span data-stu-id="41fb9-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="41fb9-117">JAVA 和 Visual Basic 中的 COM 錯誤處理</span><span class="sxs-lookup"><span data-stu-id="41fb9-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="41fb9-118">錯誤處理策略</span><span class="sxs-lookup"><span data-stu-id="41fb9-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="41fb9-119">處理未知的錯誤</span><span class="sxs-lookup"><span data-stu-id="41fb9-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="41fb9-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="41fb9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41fb9-121">COM 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="41fb9-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




