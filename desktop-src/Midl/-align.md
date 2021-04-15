---
title: /align 參數
description: /Align 參數的功能與 MIDL/Zp 選項相同，而且 MIDL 編譯器只會針對回溯相容性與 Mktyplib.exe 進行辨識。
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align 參數 MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507613"
---
# <a name="align-switch"></a><span data-ttu-id="6e1d7-104">/align 參數</span><span class="sxs-lookup"><span data-stu-id="6e1d7-104">/align switch</span></span>

<span data-ttu-id="6e1d7-105">**/Align** 參數的功能與 midl [**/Zp**](-zp.md)選項相同，而且 midl 編譯器只會針對回溯相容性與 mktyplib.exe 進行辨識。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="6e1d7-106">Mktyplib.exe 工具已淘汰。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="6e1d7-107">請改用 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="6e1d7-108">切換選項</span><span class="sxs-lookup"><span data-stu-id="6e1d7-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6e1d7-109">*對準*</span><span class="sxs-lookup"><span data-stu-id="6e1d7-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="6e1d7-110">指定程式庫中類型的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="6e1d7-111">*對齊* 值可以是1、2、4或8。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="6e1d7-112">值1表示自然對齊; *n* 表示位元組 *n* 的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="6e1d7-113">當您未指定 **/align** 參數時，預設值為8。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e1d7-114">備註</span><span class="sxs-lookup"><span data-stu-id="6e1d7-114">Remarks</span></span>

<span data-ttu-id="6e1d7-115">如果您要產生新的 makefile，請使用 [**/Zp**](-zp.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="6e1d7-116">對齊值會對應到 Microsoft C/c + + 編譯器所使用的 [**/Zp**](-zp.md) 選項值。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="6e1d7-117">當您叫用 MIDL 編譯器時，請務必指定相同的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="6e1d7-118">如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="6e1d7-119">如需使用非標準封裝層級的潛在危險討論，請參閱 [**/Zp**](-zp.md) 說明主題。</span><span class="sxs-lookup"><span data-stu-id="6e1d7-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="6e1d7-120">範例</span><span class="sxs-lookup"><span data-stu-id="6e1d7-120">Examples</span></span>

<span data-ttu-id="6e1d7-121">**midl/align：4檔案名 .idl**</span><span class="sxs-lookup"><span data-stu-id="6e1d7-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6e1d7-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e1d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1d7-123">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="6e1d7-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6e1d7-124">**/Zp**</span><span class="sxs-lookup"><span data-stu-id="6e1d7-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




