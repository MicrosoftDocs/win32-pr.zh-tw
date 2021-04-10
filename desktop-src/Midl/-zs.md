---
title: /Zs 參數
description: /Zs 參數表示編譯器只會檢查語法，且不會產生輸出檔。
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /Zs 參數 MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678308"
---
# <a name="zs-switch"></a><span data-ttu-id="c0fee-104">/Zs 參數</span><span class="sxs-lookup"><span data-stu-id="c0fee-104">/Zs switch</span></span>

<span data-ttu-id="c0fee-105">**/Zs** 參數表示編譯器只會檢查語法，且不會產生輸出檔。</span><span class="sxs-lookup"><span data-stu-id="c0fee-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="c0fee-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="c0fee-106">Switch Options</span></span>

<span data-ttu-id="c0fee-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0fee-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0fee-108">備註</span><span class="sxs-lookup"><span data-stu-id="c0fee-108">Remarks</span></span>

<span data-ttu-id="c0fee-109">此參數會覆寫所有其他參數，這些參數會指定輸出檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c0fee-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="c0fee-110">您也可以使用 MIDL 編譯器參數 [**/syntax \_ 檢查**](-syntax-check.md)來指定語法檢查模式。</span><span class="sxs-lookup"><span data-stu-id="c0fee-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c0fee-111">範例</span><span class="sxs-lookup"><span data-stu-id="c0fee-111">Examples</span></span>

<span data-ttu-id="c0fee-112">**midl/Zs 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c0fee-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="c0fee-113">**midl/syntax \_ 檢查檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="c0fee-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c0fee-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0fee-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0fee-115">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="c0fee-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c0fee-116">**/syntax \_ 檢查**</span><span class="sxs-lookup"><span data-stu-id="c0fee-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




