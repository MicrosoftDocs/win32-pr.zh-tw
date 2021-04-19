---
title: optimize 屬性
description: '\ Optimize \ ACF 屬性是用來微調將資料封送處理的階層層級。'
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- optimize 屬性 MIDL
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968875"
---
# <a name="optimize-attribute"></a><span data-ttu-id="9908e-104">optimize 屬性</span><span class="sxs-lookup"><span data-stu-id="9908e-104">optimize attribute</span></span>

<span data-ttu-id="9908e-105">**\[ Optimize \]** ACF 屬性是用來微調將資料封送處理的階層層級。</span><span class="sxs-lookup"><span data-stu-id="9908e-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="9908e-106">這個關鍵字是取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="9908e-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="9908e-107">目前的 MIDL 編譯應該改用 [**/Oicf**](-oi.md)[**/robust**](-robust.md) 。</span><span class="sxs-lookup"><span data-stu-id="9908e-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="9908e-108">參數</span><span class="sxs-lookup"><span data-stu-id="9908e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9908e-109">*優化-選項*</span><span class="sxs-lookup"><span data-stu-id="9908e-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="9908e-110">指定封送處理資料的方法。</span><span class="sxs-lookup"><span data-stu-id="9908e-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="9908e-111">請使用 "s" 進行混合模式封送處理，或使用 "i" 進行解讀封送處理。</span><span class="sxs-lookup"><span data-stu-id="9908e-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9908e-112">備註</span><span class="sxs-lookup"><span data-stu-id="9908e-112">Remarks</span></span>

<span data-ttu-id="9908e-113">此版本的 RPC 提供兩種方法來封送處理資料：混合模式 ( "s" ) 並 ( "i" ) 進行解讀。</span><span class="sxs-lookup"><span data-stu-id="9908e-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="9908e-114">這些方法會對應至 [**/os**](-os.md) 和 [**/Oi**](-oi.md) 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="9908e-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="9908e-115">解讀的方法會完全離線地封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="9908e-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="9908e-116">雖然這可以大幅減少存根的大小，但效能可能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="9908e-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="9908e-117">如果要考慮效能，混合模式方法可以是最佳的方法。</span><span class="sxs-lookup"><span data-stu-id="9908e-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="9908e-118">混合模式可讓 MIDL 編譯器判斷哪些資料會以內嵌方式進行封送處理，以及透過呼叫離線動態連結程式庫的方式進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="9908e-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="9908e-119">如果有許多程式使用相同的資料類型，就可以重複呼叫單一程式來封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="9908e-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="9908e-120">如此一來，最適合內嵌封送處理的資料會以內嵌方式處理，而其他資料可以更有效率地在離線時進行封送處理。</span><span class="sxs-lookup"><span data-stu-id="9908e-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="9908e-121">請注意， **\[ optimize \]** 屬性可用來做為介面屬性或做為作業屬性。</span><span class="sxs-lookup"><span data-stu-id="9908e-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="9908e-122">如果用來作為介面屬性，它會設定整個介面的預設值，覆寫命令列參數。</span><span class="sxs-lookup"><span data-stu-id="9908e-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="9908e-123">但是，如果使用它做為作業屬性，它只會影響該作業，覆寫命令列參數和介面預設值。</span><span class="sxs-lookup"><span data-stu-id="9908e-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="9908e-124">範例</span><span class="sxs-lookup"><span data-stu-id="9908e-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="9908e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9908e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9908e-126">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="9908e-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="9908e-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="9908e-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="9908e-128">**/Os**</span><span class="sxs-lookup"><span data-stu-id="9908e-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="9908e-129">**/robust**</span><span class="sxs-lookup"><span data-stu-id="9908e-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




