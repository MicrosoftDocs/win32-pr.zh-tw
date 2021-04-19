---
title: /sal_local 參數
description: /Sal \_ 本機參數會將 MIDL 導向至另一個標記為 \ local \ 之介面方法參數的 sal 注釋。 /Sal 參數也必須存在。
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /sal_local switch MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106969493"
---
# <a name="sal_local-switch"></a><span data-ttu-id="d083f-105">/sal \_ 本機參數</span><span class="sxs-lookup"><span data-stu-id="d083f-105">/sal\_local switch</span></span>

<span data-ttu-id="d083f-106">**/Sal \_ 本機** 參數會指示 MIDL 針對標記為 [**\[ \] local**](local.md)之介面方法的參數產生 sal 注釋。</span><span class="sxs-lookup"><span data-stu-id="d083f-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="d083f-107">[**/Sal**](-sal.md)參數也必須存在。</span><span class="sxs-lookup"><span data-stu-id="d083f-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="d083f-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="d083f-108">Switch Options</span></span>

<span data-ttu-id="d083f-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d083f-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d083f-110">備註</span><span class="sxs-lookup"><span data-stu-id="d083f-110">Remarks</span></span>

<span data-ttu-id="d083f-111">修改 [**/sal**](-sal.md)參數的行為，也會提供標記有 [**\[ 區域 \]**](local.md)屬性之介面方法參數的附注。</span><span class="sxs-lookup"><span data-stu-id="d083f-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="d083f-112">使用 [ [**\[ 批註 \]**](annotate.md)] 屬性可使用不同的批註字串來覆寫 MIDL 產生的注釋。</span><span class="sxs-lookup"><span data-stu-id="d083f-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="d083f-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d083f-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d083f-114">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="d083f-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="d083f-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="d083f-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="d083f-116">[**\[注釋\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="d083f-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




