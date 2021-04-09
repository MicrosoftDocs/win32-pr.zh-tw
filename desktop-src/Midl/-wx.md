---
title: /WX 參數
description: /WX 參數指示 MIDL 編譯器在指定警告層級上，將所有錯誤處理為錯誤。
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX 參數 MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841387"
---
# <a name="wx-switch"></a><span data-ttu-id="c2c12-104">/WX 參數</span><span class="sxs-lookup"><span data-stu-id="c2c12-104">/WX switch</span></span>

<span data-ttu-id="c2c12-105">**/Wx** 參數指示 MIDL 編譯器在指定警告層級上，將所有錯誤處理為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2c12-105">The **/WX** switch instructs the MIDL compiler to handle all errors at the given warning level as errors.</span></span>

``` syntax
midl /WX
```

## <a name="switch-options"></a><span data-ttu-id="c2c12-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="c2c12-106">Switch Options</span></span>

<span data-ttu-id="c2c12-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c2c12-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c12-108">備註</span><span class="sxs-lookup"><span data-stu-id="c2c12-108">Remarks</span></span>

<span data-ttu-id="c2c12-109">如果指定了 **/wx** 參數，且未指定 [**/w**](-w.md)*n* 參數，則預設層級1的所有警告都會視為錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2c12-109">If the **/WX** switch is specified and the [**/W**](-w.md)*n* switch is not specified, all warnings at the default level, level 1, are treated as errors.</span></span>

<span data-ttu-id="c2c12-110">[**/W**](-w.md)*n* 參數會指示編譯器顯示層級 *n* 的所有警告，而 **/wx** 則會指示編譯器將所有警告視為錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="c2c12-110">The [**/W**](-w.md)*n* switch directs the compiler to display all warnings at level *n* and **/WX** directs the compiler to handle all warnings as errors.</span></span> <span data-ttu-id="c2c12-111">這兩個參數的組合會指示編譯器將層級 *n* 的所有警告視為錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="c2c12-111">The combination of these two switches directs the compiler to handle all warnings at level *n* as errors.</span></span>

<span data-ttu-id="c2c12-112">錯誤與警告不同。</span><span class="sxs-lookup"><span data-stu-id="c2c12-112">Errors are different from warnings.</span></span> <span data-ttu-id="c2c12-113">錯誤會導致 MIDL 編譯器終止 IDL 檔案的處理。</span><span class="sxs-lookup"><span data-stu-id="c2c12-113">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="c2c12-114">警告會導致 MIDL 編譯器發出參考用訊息，並繼續處理 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="c2c12-114">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="c2c12-115">警告-層級零 (0) 指示 MIDL 編譯器隱藏警告資訊。</span><span class="sxs-lookup"><span data-stu-id="c2c12-115">Warning-level zero (0) directs the MIDL compiler to suppress warning information.</span></span> <span data-ttu-id="c2c12-116">結合 **/W0** 和 **/wx** 參數時，MIDL 編譯器會隱藏所有警告資訊。</span><span class="sxs-lookup"><span data-stu-id="c2c12-116">When the **/W0** and **/WX** switches are combined, the MIDL compiler suppresses all warning information.</span></span> <span data-ttu-id="c2c12-117">在此情況下， **/wx** 參數沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="c2c12-117">In this case, the **/WX** switch has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="c2c12-118">範例</span><span class="sxs-lookup"><span data-stu-id="c2c12-118">Examples</span></span>

<span data-ttu-id="c2c12-119">**midl/WX 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c2c12-119">**midl /WX filename.idl**</span></span>

<span data-ttu-id="c2c12-120">**midl/W3/WX 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c2c12-120">**midl /W3 /WX filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c2c12-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2c12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2c12-122">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="c2c12-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c2c12-123">**/W**</span><span class="sxs-lookup"><span data-stu-id="c2c12-123">**/W**</span></span>](-w.md)
</dt> </dl>

 

 




