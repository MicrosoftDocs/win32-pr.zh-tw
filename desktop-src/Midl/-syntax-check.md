---
title: /syntax_check 參數
description: /Syntax \_ 檢查參數表示編譯器只會檢查語法，並且不會產生輸出檔。
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check switch MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678519"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="f18e6-104">/syntax \_ 檢查參數</span><span class="sxs-lookup"><span data-stu-id="f18e6-104">/syntax\_check switch</span></span>

<span data-ttu-id="f18e6-105">**/Syntax \_ 檢查** 參數表示編譯器只會檢查語法，並且不會產生輸出檔。</span><span class="sxs-lookup"><span data-stu-id="f18e6-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="f18e6-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="f18e6-106">Switch Options</span></span>

<span data-ttu-id="f18e6-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f18e6-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f18e6-108">備註</span><span class="sxs-lookup"><span data-stu-id="f18e6-108">Remarks</span></span>

<span data-ttu-id="f18e6-109">此參數會覆寫所有其他參數，這些參數會指定輸出檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f18e6-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="f18e6-110">您也可以使用 MIDL 編譯器選項 [**/Zs**](-zs.md)來指定語法檢查模式。</span><span class="sxs-lookup"><span data-stu-id="f18e6-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f18e6-111">範例</span><span class="sxs-lookup"><span data-stu-id="f18e6-111">Examples</span></span>

<span data-ttu-id="f18e6-112">**midl/Zs 檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="f18e6-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="f18e6-113">**midl/syntax \_ 檢查檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="f18e6-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="f18e6-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f18e6-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18e6-115">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="f18e6-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f18e6-116">**/Zs**</span><span class="sxs-lookup"><span data-stu-id="f18e6-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




