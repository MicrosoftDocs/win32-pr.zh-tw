---
title: /mktyplib203 參數
description: /Mktyplib203 參數會強制 MIDL 編譯器剖析輸入檔。
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203 參數 MIDL
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841435"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="19ad7-104">/mktyplib203 參數</span><span class="sxs-lookup"><span data-stu-id="19ad7-104">/mktyplib203 switch</span></span>

<span data-ttu-id="19ad7-105">**/Mktyplib203** 參數會強制 MIDL 編譯器剖析輸入檔。</span><span class="sxs-lookup"><span data-stu-id="19ad7-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="19ad7-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="19ad7-106">Switch Options</span></span>

<span data-ttu-id="19ad7-107">此參數沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="19ad7-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="19ad7-108">備註</span><span class="sxs-lookup"><span data-stu-id="19ad7-108">Remarks</span></span>

<span data-ttu-id="19ad7-109">為了使用 **/mktyplib203** 參數，輸入檔必須完全遵循 ODL 語法，這表示您不能將任何語句放在程式庫區塊之外。</span><span class="sxs-lookup"><span data-stu-id="19ad7-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="19ad7-110">範例</span><span class="sxs-lookup"><span data-stu-id="19ad7-110">Examples</span></span>

<span data-ttu-id="19ad7-111">**midl/mktyplib203 myoldodl. odl**</span><span class="sxs-lookup"><span data-stu-id="19ad7-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="19ad7-112">**midl/mktyplib203 oldhabit .idl**</span><span class="sxs-lookup"><span data-stu-id="19ad7-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="19ad7-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19ad7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19ad7-114">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="19ad7-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="19ad7-115">使用 MIDL 產生類型程式庫</span><span class="sxs-lookup"><span data-stu-id="19ad7-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




