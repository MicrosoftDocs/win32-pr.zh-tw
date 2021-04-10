---
title: midl_pragma 警告屬性
description: 使用 midl \_ pragma warning 選項，在編譯時期暫時覆寫 midl 的警告訊息行為。
ms.assetid: d32a3d3f-5c4d-4f93-a72a-2224ceed0012
keywords:
- midl_pragma 警告屬性 MIDL
topic_type:
- apiref
api_name:
- midl_pragma warning
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b7e1e2c2a1d818216245e45a9129018a3ba2e1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841108"
---
# <a name="midl_pragma-warning-attribute"></a><span data-ttu-id="19f4e-104">midl \_ pragma warning 屬性</span><span class="sxs-lookup"><span data-stu-id="19f4e-104">midl\_pragma warning attribute</span></span>

<span data-ttu-id="19f4e-105">使用 **midl \_ pragma warning** 選項，在編譯時期暫時覆寫 midl 的警告訊息行為。</span><span class="sxs-lookup"><span data-stu-id="19f4e-105">Use the **midl\_pragma warning** option to temporarily override MIDL's warning message behavior at compile time.</span></span>

``` syntax
midl_pragma warning ( warning_option : message_list )
```

## <a name="parameters"></a><span data-ttu-id="19f4e-106">參數</span><span class="sxs-lookup"><span data-stu-id="19f4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f4e-107">*warning \_ 選項*</span><span class="sxs-lookup"><span data-stu-id="19f4e-107">*warning\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="19f4e-108">警告選項可以是下列其中一項： [停用]、[啟用]、[預設]。</span><span class="sxs-lookup"><span data-stu-id="19f4e-108">The warning option can be one of the following: disable, enable, default.</span></span>

</dd> <dt>

<span data-ttu-id="19f4e-109">*郵寄清單 \_*</span><span class="sxs-lookup"><span data-stu-id="19f4e-109">*message\_list*</span></span> 
</dt> <dd>

<span data-ttu-id="19f4e-110">以空格分隔的訊息編號清單。</span><span class="sxs-lookup"><span data-stu-id="19f4e-110">A list of message numbers separated by spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19f4e-111">備註</span><span class="sxs-lookup"><span data-stu-id="19f4e-111">Remarks</span></span>

<span data-ttu-id="19f4e-112">Pragma 可以像 C 編譯器 pragma 一樣使用。</span><span class="sxs-lookup"><span data-stu-id="19f4e-112">The pragma can be used like a C-compiler pragma.</span></span> <span data-ttu-id="19f4e-113">也就是說，它會停用、啟用或返回指定 MIDL 警告的預設行為。</span><span class="sxs-lookup"><span data-stu-id="19f4e-113">That is, it disables, enables, or returns to the default behavior for a given MIDL warning.</span></span>

## <a name="examples"></a><span data-ttu-id="19f4e-114">範例</span><span class="sxs-lookup"><span data-stu-id="19f4e-114">Examples</span></span>

``` syntax
#if (__midl >= 501)
midl_pragma warning( disable: 2007 )   // file already imported midl_pragma warning( disable: 2209 )   // ignored redundant attr
#endif
```

## <a name="see-also"></a><span data-ttu-id="19f4e-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19f4e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f4e-116">**pragma**</span><span class="sxs-lookup"><span data-stu-id="19f4e-116">**pragma**</span></span>](pragma.md)
</dt> </dl>

 

 




