---
title: 處理
description: 程式位址控制碼的格式字串描述中最多有兩個部分。
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316066"
---
# <a name="handles"></a><span data-ttu-id="32a18-103">處理</span><span class="sxs-lookup"><span data-stu-id="32a18-103">Handles</span></span>

<span data-ttu-id="32a18-104">程式位址控制碼的格式字串描述中最多有兩個部分。</span><span class="sxs-lookup"><span data-stu-id="32a18-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="32a18-105">第一個部分是程式 \_ 描述<1> 欄位的控制碼類型，用來指示隱含控制碼。</span><span class="sxs-lookup"><span data-stu-id="32a18-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="32a18-106">這部分永遠存在。</span><span class="sxs-lookup"><span data-stu-id="32a18-106">This part is always present.</span></span> <span data-ttu-id="32a18-107">第二個部分是程式中任何明確控制碼的參數描述。</span><span class="sxs-lookup"><span data-stu-id="32a18-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="32a18-108">下列各節將說明這兩個部分，並討論系結控制碼問題的存根描述元結構的其他 MIDL 編譯器支援。</span><span class="sxs-lookup"><span data-stu-id="32a18-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="32a18-109">隱含控制碼</span><span class="sxs-lookup"><span data-stu-id="32a18-109">Implicit Handles</span></span>

<span data-ttu-id="32a18-110">如果程式使用系結的隱含控制碼，程式 \_ 描述的<1> 欄位的控制碼類型，會包含三個有效非零值其中之一。</span><span class="sxs-lookup"><span data-stu-id="32a18-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="32a18-111">在 \_ 存根描述元結構的隱含控制碼資訊欄位中，可以找到隱含控制碼的 MIDL 編譯器支援 \_ ：</span><span class="sxs-lookup"><span data-stu-id="32a18-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="32a18-112">如果程式使用 auto 控制碼， **pAutoHandle** 成員就會包含已定義的存根（自動控制碼變數）位址。</span><span class="sxs-lookup"><span data-stu-id="32a18-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="32a18-113">如果程式使用隱含基本控制碼， **pPrimitiveHandle** 成員就會包含已定義的存根（基本控制碼）變數位址。</span><span class="sxs-lookup"><span data-stu-id="32a18-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="32a18-114">最後，如果程式使用隱含的泛型控制碼， **pGenericBindingInfo** 成員會將指標的位址保留在對應的泛型系結 **\_ \_ 資訊** 結構中。</span><span class="sxs-lookup"><span data-stu-id="32a18-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="32a18-115">資料結構 **MIDL \_ 存根 \_ DESC** 包含泛型系 **\_ \_ 結** 組結構集合的指標。</span><span class="sxs-lookup"><span data-stu-id="32a18-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="32a18-116">此集合之零位置的專案會保留給系結和 **解除** 系結 **常式，對應** 至 **pGenericBindingInfo** 在 **隱含 \_ 控制碼 \_ 資訊** 中參考的泛型系結控制碼。</span><span class="sxs-lookup"><span data-stu-id="32a18-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="32a18-117">隱含系結控制碼的型別會以格式字串表示。</span><span class="sxs-lookup"><span data-stu-id="32a18-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="32a18-118">明確控制碼</span><span class="sxs-lookup"><span data-stu-id="32a18-118">Explicit Handles</span></span>

<span data-ttu-id="32a18-119">有三個可能的明確控制碼類型：內容、泛型和基本。</span><span class="sxs-lookup"><span data-stu-id="32a18-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="32a18-120">如果是明確控制碼 (或 \[  \] 僅限輸出的內容控制碼（以) 的相同方式處理），系結處理資訊就會顯示為程式的其中一個參數。</span><span class="sxs-lookup"><span data-stu-id="32a18-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="32a18-121">三個可能的描述如下所示。</span><span class="sxs-lookup"><span data-stu-id="32a18-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="32a18-122">Primitive</span><span class="sxs-lookup"><span data-stu-id="32a18-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="32a18-123">旗標<1> 指出控制碼是否以指標傳遞。</span><span class="sxs-lookup"><span data-stu-id="32a18-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="32a18-124">Offset<2> 提供從堆疊開頭到基本控制碼的位移。</span><span class="sxs-lookup"><span data-stu-id="32a18-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="32a18-125">類型格式字串中的基本控制碼描述會縮減為單一 FC \_ 略過。</span><span class="sxs-lookup"><span data-stu-id="32a18-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="32a18-126">泛型</span><span class="sxs-lookup"><span data-stu-id="32a18-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="32a18-127">旗標 \_ 和 \_ 大小<1> 具有上方旗標半值和較低大小的半值。</span><span class="sxs-lookup"><span data-stu-id="32a18-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="32a18-128">旗標會指出控制碼是否以指標傳遞。</span><span class="sxs-lookup"><span data-stu-id="32a18-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="32a18-129">[大小] 欄位提供使用者定義的大小–一般控制碼類型。</span><span class="sxs-lookup"><span data-stu-id="32a18-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="32a18-130">在32位系統上，此大小限制為1、2或4個位元組，而64位系統上的1、2、4或8個位元組則為1、2、4或8個位元組。</span><span class="sxs-lookup"><span data-stu-id="32a18-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="32a18-131">Offset<2> 欄位提供從指標堆疊開頭到指定大小資料的位移。</span><span class="sxs-lookup"><span data-stu-id="32a18-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="32a18-132">系 \_ 結常式 \_ 組 \_ 索引<1> 欄位會將存根描述項的 aGenericBindingRoutinePairs 欄位中的索引提供給泛型控制碼的系結和 **解除** 系結常式函式指標。</span><span class="sxs-lookup"><span data-stu-id="32a18-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="32a18-133">類型格式的泛型控制碼描述僅為相關資料類型的描述。</span><span class="sxs-lookup"><span data-stu-id="32a18-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="32a18-134">Context</span><span class="sxs-lookup"><span data-stu-id="32a18-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="32a18-135">旗標<1> 指出控制碼的傳遞方式，以及其型別。</span><span class="sxs-lookup"><span data-stu-id="32a18-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="32a18-136">下表顯示有效的旗標。</span><span class="sxs-lookup"><span data-stu-id="32a18-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="32a18-137">Hex</span><span class="sxs-lookup"><span data-stu-id="32a18-137">Hex</span></span> | <span data-ttu-id="32a18-138">旗標</span><span class="sxs-lookup"><span data-stu-id="32a18-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="32a18-139">80</span><span class="sxs-lookup"><span data-stu-id="32a18-139">80</span></span>  | <span data-ttu-id="32a18-140">控制碼 \_ 參數 \_ 為 \_ VIA \_ PTR</span><span class="sxs-lookup"><span data-stu-id="32a18-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="32a18-141">40</span><span class="sxs-lookup"><span data-stu-id="32a18-141">40</span></span>  | <span data-ttu-id="32a18-142">句 \_ 柄 \_ 參數 \_ 位於</span><span class="sxs-lookup"><span data-stu-id="32a18-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="32a18-143">20</span><span class="sxs-lookup"><span data-stu-id="32a18-143">20</span></span>  | <span data-ttu-id="32a18-144">控制碼 \_ 參數 \_ 已 \_ 退出</span><span class="sxs-lookup"><span data-stu-id="32a18-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="32a18-145">21</span><span class="sxs-lookup"><span data-stu-id="32a18-145">21</span></span>  | <span data-ttu-id="32a18-146">控制碼 \_ 參數 \_ 為 \_ RETURN</span><span class="sxs-lookup"><span data-stu-id="32a18-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="32a18-147">08</span><span class="sxs-lookup"><span data-stu-id="32a18-147">08</span></span>  | <span data-ttu-id="32a18-148">NDR \_ STRICT \_ 內容 \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="32a18-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="32a18-149">04</span><span class="sxs-lookup"><span data-stu-id="32a18-149">04</span></span>  | <span data-ttu-id="32a18-150">NDR \_ 內容 \_ 控制碼 \_ 沒有 \_ 序列化</span><span class="sxs-lookup"><span data-stu-id="32a18-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="32a18-151">02</span><span class="sxs-lookup"><span data-stu-id="32a18-151">02</span></span>  | <span data-ttu-id="32a18-152">NDR \_ 內容 \_ 控制碼 \_ 序列化</span><span class="sxs-lookup"><span data-stu-id="32a18-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="32a18-153">01</span><span class="sxs-lookup"><span data-stu-id="32a18-153">01</span></span>  | <span data-ttu-id="32a18-154">NDR \_ 內容 \_ 控制碼 \_ 不 \_ 可以是 \_ Null</span><span class="sxs-lookup"><span data-stu-id="32a18-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="32a18-155">前四個旗標一直都存在，最後四個旗標已新增到 Windows 2000 中。</span><span class="sxs-lookup"><span data-stu-id="32a18-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="32a18-156">Offset<2> 欄位提供從堆疊開頭到內容控制碼的位移。</span><span class="sxs-lookup"><span data-stu-id="32a18-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="32a18-157">內容取消 \_ \_ 常式 \_ 索引<1> 為此內容控制碼所用的取消常式提供存根描述元之 **apfnNdrRundownRoutines** 欄位的索引。</span><span class="sxs-lookup"><span data-stu-id="32a18-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="32a18-158">編譯器一律會產生索引。</span><span class="sxs-lookup"><span data-stu-id="32a18-158">The compiler always generates an index.</span></span> <span data-ttu-id="32a18-159">針對沒有取消常式的常式，這是包含 null 之資料表位置的索引。</span><span class="sxs-lookup"><span data-stu-id="32a18-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="32a18-160">針對內建的存根 **-Oi2**，param \_ num<1> 提供序數計數，從零開始，以指定在指定程式中的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="32a18-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="32a18-161">在舊版的解譯器中，param \_ num<1> 在其程式中提供內容控制碼的參數編號，從零開始。</span><span class="sxs-lookup"><span data-stu-id="32a18-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="32a18-162">在 [描述] 中，類型格式字串中的內容控制碼描述不會有<2> 的位移。</span><span class="sxs-lookup"><span data-stu-id="32a18-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="32a18-163">New – Oif 標頭</span><span class="sxs-lookup"><span data-stu-id="32a18-163">The New –Oif Header</span></span>

<span data-ttu-id="32a18-164">如先前所述，– [**Oif**](/windows/desktop/Midl/-oi) 標頭會在 **– Oi** 標頭上展開。</span><span class="sxs-lookup"><span data-stu-id="32a18-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="32a18-165">為了方便起見，所有欄位如下所示：</span><span class="sxs-lookup"><span data-stu-id="32a18-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="32a18-166"> (舊的標頭) </span><span class="sxs-lookup"><span data-stu-id="32a18-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="32a18-167"> ([**– Oif**](/windows/desktop/Midl/-oi) 延伸模組) </span><span class="sxs-lookup"><span data-stu-id="32a18-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="32a18-168">常數 \_ 用戶端 \_ 緩衝區 \_ 大小<2> 提供編譯器預先計算的封送處理緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="32a18-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="32a18-169">這可能只是部分大小，因為 ClientMustSize 旗標會觸發調整大小。</span><span class="sxs-lookup"><span data-stu-id="32a18-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="32a18-170">常數 \_ 伺服器 \_ 緩衝區 \_ 大小<2> 提供編譯器所預先計算的封送處理緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="32a18-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="32a18-171">這可能只是部分大小，因為 ServerMustSize 旗標會觸發調整大小。</span><span class="sxs-lookup"><span data-stu-id="32a18-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="32a18-172">解譯器 \_ OPT \_ 旗標是在 Ndrtypes 中定義：</span><span class="sxs-lookup"><span data-stu-id="32a18-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="32a18-173">如果伺服器需要執行緩衝區調整大小傳遞，就會設定 ServerMustSize 位。</span><span class="sxs-lookup"><span data-stu-id="32a18-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="32a18-174">如果用戶端需要執行緩衝區調整大小傳遞，就會設定 ClientMustSize 位。</span><span class="sxs-lookup"><span data-stu-id="32a18-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="32a18-175">如果程式有傳回值，則會設定 HasReturn 位。</span><span class="sxs-lookup"><span data-stu-id="32a18-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="32a18-176">如果管道封裝需要用來支援管道引數，則會設定 HasPipes 位。</span><span class="sxs-lookup"><span data-stu-id="32a18-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="32a18-177">如果程式是非同步 DCOM 程式，則會設定 HasAsyncUuid 位。</span><span class="sxs-lookup"><span data-stu-id="32a18-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="32a18-178">HasExtensions 位表示使用 Windows 2000 和更新版本的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="32a18-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="32a18-179">HasAsyncHandle 位表示非同步 RPC 程式。</span><span class="sxs-lookup"><span data-stu-id="32a18-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="32a18-180">HasAsyncHandle 位一開始是用於不同的非同步支援 DCOM 實，因此無法用於 DCOM 中目前的樣式非同步支援。</span><span class="sxs-lookup"><span data-stu-id="32a18-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="32a18-181">HasAsyncUuid 位目前表示這一點。</span><span class="sxs-lookup"><span data-stu-id="32a18-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 