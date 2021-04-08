---
title: /robust 參數
description: /Robust 參數會告知 MIDL 編譯器產生額外的錯誤檢查資訊，而 NDR 引擎會使用此資訊在執行時間執行完整性檢查。
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robust 參數 MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841123"
---
# <a name="robust-switch"></a><span data-ttu-id="3bb51-104">/robust 參數</span><span class="sxs-lookup"><span data-stu-id="3bb51-104">/robust switch</span></span>

<span data-ttu-id="3bb51-105">**/Robust** 參數會告知 MIDL 編譯器產生額外的錯誤檢查資訊，而 NDR 引擎會使用此資訊在執行時間執行完整性檢查。</span><span class="sxs-lookup"><span data-stu-id="3bb51-105">The **/robust** switch tells the MIDL compiler to generate additional error-checking information, which the NDR engine uses to perform integrity checks at run time.</span></span>

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a><span data-ttu-id="3bb51-106">切換選項</span><span class="sxs-lookup"><span data-stu-id="3bb51-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="3bb51-107">*/Oicf*</span><span class="sxs-lookup"><span data-stu-id="3bb51-107">*/Oicf*</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="3bb51-108">*/Oif*</span><span class="sxs-lookup"><span data-stu-id="3bb51-108">*/Oif*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb51-109">這些參數在其功能上都相同。</span><span class="sxs-lookup"><span data-stu-id="3bb51-109">These switches are identical in their functionality.</span></span> <span data-ttu-id="3bb51-110">他們會指定封送處理的無程式碼 proxy 方法，並使用快速格式字串來改善效能。</span><span class="sxs-lookup"><span data-stu-id="3bb51-110">They specify the codeless proxy method of marshaling and use fast format strings for improved performance.</span></span> <span data-ttu-id="3bb51-111">請參閱/ [**Oi**](-oi.md)。</span><span class="sxs-lookup"><span data-stu-id="3bb51-111">See / [**Oi**](-oi.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bb51-112">備註</span><span class="sxs-lookup"><span data-stu-id="3bb51-112">Remarks</span></span>

<span data-ttu-id="3bb51-113">使用 **/robust** 參數會產生額外的資訊，以允許 (NDR) 引擎的網路資料表示，在動態陣列、等位和 DCOM 應用程式的 [**輸出**](out-idl.md) 介面指標中，對相互關聯的引數執行執行階段錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="3bb51-113">Using the **/robust** switch generates additional information that allows the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in [**out**](out-idl.md) interface pointers in DCOM applications.</span></span> <span data-ttu-id="3bb51-114">**/Robust** 參數僅適用于 windows 2000 和更新版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="3bb51-114">The **/robust** switch is only available under WindowsÂ 2000 and later versions of Windows.</span></span>

<span data-ttu-id="3bb51-115">相互關聯的引數是使用任何屬性的引數，這些屬性可在執行時間決定資料物件的大小： [**大小 \_ 為**](size-is.md)、 [**長度 \_ 為**](length-is.md)、 [**第一個 \_ 為**](first-is.md)、 [**最後一個 \_**](last-is.md)、 [**最大 \_**](max-is.md)值、 [**參數 \_ 為**](switch-is.md)，而且 [**iid \_ 為**](iid-is.md)。</span><span class="sxs-lookup"><span data-stu-id="3bb51-115">A correlated argument is an argument that uses any of the attributes that allow the size of a data object to be determined at run time: [**size\_is**](size-is.md), [**length\_is**](length-is.md), [**first\_is**](first-is.md), [**last\_is**](last-is.md), [**max\_is**](max-is.md), [**switch\_is**](switch-is.md), and [**iid\_is**](iid-is.md).</span></span> <span data-ttu-id="3bb51-116">根據網路標記法的憑證-DCE 規格，此相互關聯的引數會出現在兩個不同的位置。</span><span class="sxs-lookup"><span data-stu-id="3bb51-116">In accordance with the OSF-DCE specification for the wire representation, this correlated argument appears in two different places.</span></span> <span data-ttu-id="3bb51-117">例如，請考慮使用 **大小 \_ 為** 屬性的一般用法：</span><span class="sxs-lookup"><span data-stu-id="3bb51-117">For example, consider a typical usage of the **size\_is** attribute:</span></span>

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

<span data-ttu-id="3bb51-118">在此範例中，用戶端會傳遞 long，以指定橫條圖類型區塊的大小 \_ (以) 的橫條類型元素數目為單位 \_ ，並以指標指向橫條圖類型的實際區塊 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3bb51-118">In this example, the client passes a long that specifies the size of a block of BAR\_TYPEs (in terms of number of BAR\_TYPES elements), and a pointer to the actual block of BAR\_TYPEs.</span></span> <span data-ttu-id="3bb51-119">Size 引數與 pBarType 引數相互關聯。</span><span class="sxs-lookup"><span data-stu-id="3bb51-119">The Size argument correlates with the pBarType argument.</span></span> <span data-ttu-id="3bb51-120">根據憑證-DCE 規格，Size 引數會在網路上以兩次表示（先做為本身，然後使用 \_ 代表 pBarType 引數的橫條類型元素陣列）。</span><span class="sxs-lookup"><span data-stu-id="3bb51-120">In accordance with the OSF-DCE specification, the Size argument is represented twice on the wire—first as itself and then with the array of BAR\_TYPE elements that represent the pBarType argument.</span></span> <span data-ttu-id="3bb51-121">每個引數會根據其本身的線路表示來獨立進行封送。</span><span class="sxs-lookup"><span data-stu-id="3bb51-121">Each argument is unmarshaled independently, according to its own wire representation.</span></span> <span data-ttu-id="3bb51-122">一般來說，大小引數及其複製（用來代表另一個引數的一部分）具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="3bb51-122">Normally, the Size argument and its copy, which is used to represent part of the other argument, have the same values.</span></span> <span data-ttu-id="3bb51-123">但是，如果大小引數損毀 (例如，當橫條類型的區塊大於配置) 的區塊時， \_ 伺服器應用程式可能會停止回應，因為它會使用 Size 引數的值來測量傳入的資料。</span><span class="sxs-lookup"><span data-stu-id="3bb51-123">However, if the Size argument becomes corrupted (for example, when the block of BAR\_TYPES is larger than what was allocated), the server application may stop responding, because it uses the value of the Size argument to measure incoming data.</span></span>

<span data-ttu-id="3bb51-124">需要 **/robust** 參數才能使用 [**range**](range.md) 屬性來執行有效的範圍檢查。</span><span class="sxs-lookup"><span data-stu-id="3bb51-124">The **/robust** switch is required to implement valid range checking with the [**range**](range.md) attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="3bb51-125">範例</span><span class="sxs-lookup"><span data-stu-id="3bb51-125">Examples</span></span>

<span data-ttu-id="3bb51-126">**midl/robust/Oicf filename .idl**</span><span class="sxs-lookup"><span data-stu-id="3bb51-126">**midl /robust /Oicf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="3bb51-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bb51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb51-128">一般 MIDL 命令列語法</span><span class="sxs-lookup"><span data-stu-id="3bb51-128">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="3bb51-129">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="3bb51-129">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="3bb51-130">**範圍**</span><span class="sxs-lookup"><span data-stu-id="3bb51-130">**range**</span></span>](range.md)
</dt> </dl>

 

 




