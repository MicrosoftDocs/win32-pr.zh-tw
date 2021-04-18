---
title: /sal 參數
description: /Sal 參數會指示 MIDL 在產生的存根檔案中產生 SAL 注釋。
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /sal 參數 MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968674"
---
# <a name="sal-switch"></a><span data-ttu-id="e4833-104">/sal 參數</span><span class="sxs-lookup"><span data-stu-id="e4833-104">/sal switch</span></span>

<span data-ttu-id="e4833-105">**/Sal** 參數會指示 MIDL 在產生的存根檔案中產生 sal 注釋。</span><span class="sxs-lookup"><span data-stu-id="e4833-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="e4833-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="e4833-106">Switch Options</span></span>

<span data-ttu-id="e4833-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e4833-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4833-108">備註</span><span class="sxs-lookup"><span data-stu-id="e4833-108">Remarks</span></span>

<span data-ttu-id="e4833-109">MIDL 會將指標和陣列參數標示為反映 IDL 檔案中的參數描述（由 RPC 和 NDR 封送處理引擎強制執行）的注釋。</span><span class="sxs-lookup"><span data-stu-id="e4833-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="e4833-110">除非命令列上也有 [**/sal \_ local**](-sal-local.md) ，否則 MIDL 不會針對以 [**\[ \] 區域**](local.md)屬性標記的介面方法中的參數建立批註。</span><span class="sxs-lookup"><span data-stu-id="e4833-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="e4833-111">若要覆寫 MIDL 產生的注釋，請使用 [ [**\[ 批註 \]**](annotate.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="e4833-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="e4833-112">MIDL 產生的注釋一律會加上 RPC 的前置詞 \_ \_ \_ ，而且需要使用 **rpcsal** 的標頭將批註轉譯成標準 SAL 注釋。</span><span class="sxs-lookup"><span data-stu-id="e4833-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4833-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4833-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4833-114">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="e4833-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e4833-115">**/sal \_ 本機**</span><span class="sxs-lookup"><span data-stu-id="e4833-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="e4833-116">[**\[注釋\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="e4833-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




