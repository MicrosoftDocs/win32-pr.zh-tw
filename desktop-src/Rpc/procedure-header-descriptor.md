---
title: 程式標頭描述元
description: 在 NDR 引擎的存留期內，標頭已延伸數次。 根據編譯器的模式，目前的編譯器仍會產生不同的標頭。 不過，較新的標頭是較舊的標頭的超集合。
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463537"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="02824-105">程式標頭描述元</span><span class="sxs-lookup"><span data-stu-id="02824-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="02824-106">在 NDR 引擎的存留期內，標頭已延伸數次。</span><span class="sxs-lookup"><span data-stu-id="02824-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="02824-107">根據編譯器的模式，目前的編譯器仍會產生不同的標頭。</span><span class="sxs-lookup"><span data-stu-id="02824-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="02824-108">不過，較新的標頭是較舊的標頭的超集合。</span><span class="sxs-lookup"><span data-stu-id="02824-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="02824-109">舊的– Oi 標頭</span><span class="sxs-lookup"><span data-stu-id="02824-109">The Old –Oi Header</span></span>

<span data-ttu-id="02824-110">標頭的格式如下：</span><span class="sxs-lookup"><span data-stu-id="02824-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="02824-111">其中 \_<1> 的控制碼類型可以是下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="02824-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="02824-112">Hex</span><span class="sxs-lookup"><span data-stu-id="02824-112">Hex</span></span> | <span data-ttu-id="02824-113">Handle</span><span class="sxs-lookup"><span data-stu-id="02824-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="02824-114">31</span><span class="sxs-lookup"><span data-stu-id="02824-114">31</span></span>  | <span data-ttu-id="02824-115">FC \_ BIND \_ 泛型</span><span class="sxs-lookup"><span data-stu-id="02824-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="02824-116">32</span><span class="sxs-lookup"><span data-stu-id="02824-116">32</span></span>  | <span data-ttu-id="02824-117">FC 系結 \_ \_ 基本</span><span class="sxs-lookup"><span data-stu-id="02824-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="02824-118">33</span><span class="sxs-lookup"><span data-stu-id="02824-118">33</span></span>  | <span data-ttu-id="02824-119">FC \_ 自動 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="02824-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="02824-120">34</span><span class="sxs-lookup"><span data-stu-id="02824-120">34</span></span>  | <span data-ttu-id="02824-121">FC \_ 回呼 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="02824-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="02824-122">0</span><span class="sxs-lookup"><span data-stu-id="02824-122">0</span></span>   | <span data-ttu-id="02824-123"> (明確的控制碼) </span><span class="sxs-lookup"><span data-stu-id="02824-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="02824-124">如果控制碼 \_ 類型<1> 欄位為非零值，則程式會使用指定種類的隱含控制碼。</span><span class="sxs-lookup"><span data-stu-id="02824-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="02824-125">如需詳細資訊，請參閱「 [控制碼](handles.md) 」主題。</span><span class="sxs-lookup"><span data-stu-id="02824-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="02824-126">如果控制碼 \_ 類型<1> 欄位為零，則用於系結的控制碼就是該程式的其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="02824-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="02824-127">明確控制碼可以是基本、泛型和內容;最後一個具有下列 FC 權杖。</span><span class="sxs-lookup"><span data-stu-id="02824-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="02824-128">Hex</span><span class="sxs-lookup"><span data-stu-id="02824-128">Hex</span></span> | <span data-ttu-id="02824-129">Handle</span><span class="sxs-lookup"><span data-stu-id="02824-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="02824-130">30</span><span class="sxs-lookup"><span data-stu-id="02824-130">30</span></span>  | <span data-ttu-id="02824-131">FC 系結 \_ \_ 內容</span><span class="sxs-lookup"><span data-stu-id="02824-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="02824-132">依照慣例，DCOM 介面的控制碼類型為 FC \_ 自動 \_ 處理。</span><span class="sxs-lookup"><span data-stu-id="02824-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="02824-133">Oi \_ 旗標<1> 欄位是下列旗標的8位遮罩。</span><span class="sxs-lookup"><span data-stu-id="02824-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="02824-134">Hex</span><span class="sxs-lookup"><span data-stu-id="02824-134">Hex</span></span> | <span data-ttu-id="02824-135">旗標</span><span class="sxs-lookup"><span data-stu-id="02824-135">Flag</span></span>                         | <span data-ttu-id="02824-136">意義</span><span class="sxs-lookup"><span data-stu-id="02824-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="02824-137">01</span><span class="sxs-lookup"><span data-stu-id="02824-137">01</span></span>  | <span data-ttu-id="02824-138">已 \_ 使用的 Oi 完整 \_ PTR \_</span><span class="sxs-lookup"><span data-stu-id="02824-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="02824-139">使用完整的指標封裝。</span><span class="sxs-lookup"><span data-stu-id="02824-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="02824-140">02</span><span class="sxs-lookup"><span data-stu-id="02824-140">02</span></span>  | <span data-ttu-id="02824-141">使用的 Oi \_ RPCSS 配置 \_ \_</span><span class="sxs-lookup"><span data-stu-id="02824-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="02824-142">使用「RpcSs 記憶體」套件。</span><span class="sxs-lookup"><span data-stu-id="02824-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="02824-143">04</span><span class="sxs-lookup"><span data-stu-id="02824-143">04</span></span>  | <span data-ttu-id="02824-144">Oi \_ 物件 \_ 進程</span><span class="sxs-lookup"><span data-stu-id="02824-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="02824-145">物件介面中的程式。</span><span class="sxs-lookup"><span data-stu-id="02824-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="02824-146">08</span><span class="sxs-lookup"><span data-stu-id="02824-146">08</span></span>  | <span data-ttu-id="02824-147">Oi \_ 有 \_ RPCFLAGS</span><span class="sxs-lookup"><span data-stu-id="02824-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="02824-148">此程式有非零的 Rpc 旗標。</span><span class="sxs-lookup"><span data-stu-id="02824-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="02824-149">10</span><span class="sxs-lookup"><span data-stu-id="02824-149">10</span></span>  | <span data-ttu-id="02824-150">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="02824-150">Oi\_\*</span></span>                       | <span data-ttu-id="02824-151">多載。</span><span class="sxs-lookup"><span data-stu-id="02824-151">Overloaded.</span></span>                              |
| <span data-ttu-id="02824-152">20</span><span class="sxs-lookup"><span data-stu-id="02824-152">20</span></span>  | <span data-ttu-id="02824-153">Oi\_\*</span><span class="sxs-lookup"><span data-stu-id="02824-153">Oi\_\*</span></span>                       | <span data-ttu-id="02824-154">多載。</span><span class="sxs-lookup"><span data-stu-id="02824-154">Overloaded.</span></span>                              |
| <span data-ttu-id="02824-155">40</span><span class="sxs-lookup"><span data-stu-id="02824-155">40</span></span>  | <span data-ttu-id="02824-156">Oi \_ 使用 \_ 新的 \_ INIT \_ 常式</span><span class="sxs-lookup"><span data-stu-id="02824-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="02824-157">使用 Windows NT 3.5 Beta2 + init 常式。</span><span class="sxs-lookup"><span data-stu-id="02824-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="02824-158">80</span><span class="sxs-lookup"><span data-stu-id="02824-158">80</span></span>  |                              | <span data-ttu-id="02824-159">未使用的。</span><span class="sxs-lookup"><span data-stu-id="02824-159">Unused.</span></span>                                  |



 

<span data-ttu-id="02824-160">以下是多載的旗標。</span><span class="sxs-lookup"><span data-stu-id="02824-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="02824-161">Hex</span><span class="sxs-lookup"><span data-stu-id="02824-161">Hex</span></span> | <span data-ttu-id="02824-162">旗標</span><span class="sxs-lookup"><span data-stu-id="02824-162">Flag</span></span>                                    | <span data-ttu-id="02824-163">意義</span><span class="sxs-lookup"><span data-stu-id="02824-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="02824-164">10</span><span class="sxs-lookup"><span data-stu-id="02824-164">10</span></span>  | <span data-ttu-id="02824-165">\_使用編碼 \_</span><span class="sxs-lookup"><span data-stu-id="02824-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="02824-166">只能在 pickling 中使用。</span><span class="sxs-lookup"><span data-stu-id="02824-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="02824-167">20</span><span class="sxs-lookup"><span data-stu-id="02824-167">20</span></span>  | <span data-ttu-id="02824-168">\_使用解碼 \_</span><span class="sxs-lookup"><span data-stu-id="02824-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="02824-169">只能在 pickling 中使用。</span><span class="sxs-lookup"><span data-stu-id="02824-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="02824-170">10</span><span class="sxs-lookup"><span data-stu-id="02824-170">10</span></span>  | <span data-ttu-id="02824-171">Oi \_ 忽略 \_ 物件 \_ 例外狀況 \_ 處理</span><span class="sxs-lookup"><span data-stu-id="02824-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="02824-172">不再使用 (舊的 OLE) 。</span><span class="sxs-lookup"><span data-stu-id="02824-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="02824-173">20</span><span class="sxs-lookup"><span data-stu-id="02824-173">20</span></span>  | <span data-ttu-id="02824-174">Oi \_ 有 \_ 通訊 \_ 或 \_ 錯誤</span><span class="sxs-lookup"><span data-stu-id="02824-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="02824-175">僅限原始 RPC、 \[ 通訊 \_ 、錯誤 \_ 狀態 \] 。</span><span class="sxs-lookup"><span data-stu-id="02824-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="02824-176">20</span><span class="sxs-lookup"><span data-stu-id="02824-176">20</span></span>  | <span data-ttu-id="02824-177">Oi \_ OBJ \_ 使用 \_ V2 \_ 解譯器</span><span class="sxs-lookup"><span data-stu-id="02824-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="02824-178">在僅限 DCOM 中，請使用 [**– Oif**](/windows/desktop/Midl/-oi) 解譯器。</span><span class="sxs-lookup"><span data-stu-id="02824-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="02824-179">Rpc \_ 旗標<4> 欄位說明如何設定 [**rpc \_ 訊息**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)結構的 **RpcFlags** 欄位。</span><span class="sxs-lookup"><span data-stu-id="02824-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="02824-180">只有當 Oi \_ 旗標<1> 欄位有 oi 已 \_ 設定 RPCFLAGS 時，才會出現此欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="02824-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="02824-181">如果這個欄位不存在，則遠端程式的 RPC 旗標為零。</span><span class="sxs-lookup"><span data-stu-id="02824-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="02824-182">針對效能，非同步解譯器一律會有 \_<4> 欄位的 rpc 旗標。</span><span class="sxs-lookup"><span data-stu-id="02824-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="02824-183">[Proc \_ num<2>] 欄位提供程式的程式編號。</span><span class="sxs-lookup"><span data-stu-id="02824-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="02824-184">堆疊 \_ 大小<2> 提供堆疊上所有參數的總大小，包括此指標和/或傳回值。</span><span class="sxs-lookup"><span data-stu-id="02824-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="02824-185">\_ \_ 本檔稍後會說明<> 欄位的明確控制碼描述。</span><span class="sxs-lookup"><span data-stu-id="02824-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="02824-186">如果程式使用隱含控制碼，就不會出現這個欄位。</span><span class="sxs-lookup"><span data-stu-id="02824-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 