---
title: /no_robust 參數
description: /No \_ 健全的參數會指示 MIDL 編譯器明確停用/robust 命令列功能。 /Robust 命令列參數與其相關聯的功能是 MIDL version 6.0.359 和更新版本的預設編譯器設定。
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust switch MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678715"
---
# <a name="no_robust-switch"></a><span data-ttu-id="25de7-105">/no \_ 穩固的交換器</span><span class="sxs-lookup"><span data-stu-id="25de7-105">/no\_robust switch</span></span>

<span data-ttu-id="25de7-106">**/No \_ 健全** 的參數會指示 MIDL 編譯器明確停用 [**/robust**](-robust.md)命令列功能。</span><span class="sxs-lookup"><span data-stu-id="25de7-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="25de7-107">**/Robust** 命令列參數與其相關聯的功能是 MIDL version 6.0.359 和更新版本的預設編譯器設定。</span><span class="sxs-lookup"><span data-stu-id="25de7-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="25de7-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="25de7-108">Switch Options</span></span>

<span data-ttu-id="25de7-109">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="25de7-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="25de7-110">備註</span><span class="sxs-lookup"><span data-stu-id="25de7-110">Remarks</span></span>

<span data-ttu-id="25de7-111">使用 MIDL 版本6.0.359 和更新版本時，MIDL 編譯器預設會設定 [**/robust**](-robust.md) 。</span><span class="sxs-lookup"><span data-stu-id="25de7-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="25de7-112">如果產生的存根需要在 Microsoft Windows NT、Windows 95/98 或 Windows Me 上執行，則必須使用 **/no \_ 健全** 的命令列參數來停用 **/robust** 功能。</span><span class="sxs-lookup"><span data-stu-id="25de7-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="25de7-113">範例</span><span class="sxs-lookup"><span data-stu-id="25de7-113">Examples</span></span>

<span data-ttu-id="25de7-114">**midl/no \_ 健全的檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="25de7-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="25de7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25de7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25de7-116">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="25de7-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="25de7-117">**/robust**</span><span class="sxs-lookup"><span data-stu-id="25de7-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




