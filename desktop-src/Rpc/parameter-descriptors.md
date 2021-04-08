---
title: 參數描述項
description: 如先前所述，\ 8211; Oi 和 \ 8211; Oif 樣式參數描述項存在。
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682885"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="f3c6e-103">參數描述項</span><span class="sxs-lookup"><span data-stu-id="f3c6e-103">Parameter Descriptors</span></span>

<span data-ttu-id="f3c6e-104">如先前所述， [**-Oi**](/windows/desktop/Midl/-oi) 和 **– Oif** 樣式參數描述項存在。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="f3c6e-105">– Oi 參數描述項</span><span class="sxs-lookup"><span data-stu-id="f3c6e-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="f3c6e-106">完全解讀的存根需要 RPC 呼叫中每個參數的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="f3c6e-107">程式的參數描述會在程式的描述之後立即執行。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="f3c6e-108">**Simple – Oi**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="f3c6e-109">**參數描述項**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="f3c6e-110">的描述格式 \[  \] 或傳回簡單類型參數的格式為：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="f3c6e-111">–或–</span><span class="sxs-lookup"><span data-stu-id="f3c6e-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="f3c6e-112">其中，簡單 \_ 類型<1> 是指出簡單類型的 FC 權杖。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="f3c6e-113">這些代碼如下所示：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="f3c6e-114">**Other – Oi**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-114">**Other –Oi**</span></span>

<span data-ttu-id="f3c6e-115">**參數描述項**</span><span class="sxs-lookup"><span data-stu-id="f3c6e-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="f3c6e-116">所有其他參數類型之描述的格式為：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="f3c6e-117">其中 \_ 每個描述的參數方向<1> 欄位必須是下表所示的其中一個。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="f3c6e-118">Hex</span><span class="sxs-lookup"><span data-stu-id="f3c6e-118">Hex</span></span> | <span data-ttu-id="f3c6e-119">旗標</span><span class="sxs-lookup"><span data-stu-id="f3c6e-119">Flag</span></span>                          | <span data-ttu-id="f3c6e-120">意義</span><span class="sxs-lookup"><span data-stu-id="f3c6e-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f3c6e-121">4d</span><span class="sxs-lookup"><span data-stu-id="f3c6e-121">4d</span></span>  | <span data-ttu-id="f3c6e-122">\_PARAM 中的 FC \_</span><span class="sxs-lookup"><span data-stu-id="f3c6e-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="f3c6e-123">In 參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="f3c6e-124">50</span><span class="sxs-lookup"><span data-stu-id="f3c6e-124">50</span></span>  | <span data-ttu-id="f3c6e-125">FC \_ IN \_ OUT \_ 參數</span><span class="sxs-lookup"><span data-stu-id="f3c6e-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="f3c6e-126">In/out 參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="f3c6e-127">51</span><span class="sxs-lookup"><span data-stu-id="f3c6e-127">51</span></span>  | <span data-ttu-id="f3c6e-128">FC \_ 輸出 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="f3c6e-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="f3c6e-129">Out 參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="f3c6e-130">52</span><span class="sxs-lookup"><span data-stu-id="f3c6e-130">52</span></span>  | <span data-ttu-id="f3c6e-131">FC \_ 傳回 \_ 參數</span><span class="sxs-lookup"><span data-stu-id="f3c6e-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="f3c6e-132">程式傳回值。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="f3c6e-133">4f</span><span class="sxs-lookup"><span data-stu-id="f3c6e-133">4f</span></span>  | <span data-ttu-id="f3c6e-134">A FC \_ IN \_ PARAM \_ 沒有 \_ 免費 \_ INST</span><span class="sxs-lookup"><span data-stu-id="f3c6e-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="f3c6e-135">Xmit/rep 中的，表示未進行任何釋放的參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="f3c6e-136">堆疊 \_ 大小<1> 是堆疊上參數的大小，以參數在堆疊上佔據的整數數目表示。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="f3c6e-137">64位平臺上不支援 [**– Oi**](/windows/desktop/Midl/-oi) 模式。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="f3c6e-138">Type \_ offset<2> field 是 type format string 資料表中的位移，表示引數的型別描述項。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="f3c6e-139">– Oif 參數描述項</span><span class="sxs-lookup"><span data-stu-id="f3c6e-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="f3c6e-140">參數描述有兩種可能的格式：一個用於基底類型，另一個用於所有其他類型。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="f3c6e-141">基底類型：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="f3c6e-142">其他：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="f3c6e-143">在兩個堆疊 \_ 位移<2> 指出虛擬引數堆疊上的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="f3c6e-144">針對基底類型，引數型別是由對應至類型的格式字元直接提供。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="f3c6e-145">針對其他類型，[類型 \_ 位移]<2> 欄位會在類型格式字串資料表中提供引數的型別描述項所在的位移。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="f3c6e-146">[參數屬性] 欄位的定義如下：</span><span class="sxs-lookup"><span data-stu-id="f3c6e-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="f3c6e-147">只有在參數必須調整大小時，才會設定 **MustSize** 位。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="f3c6e-148">如果伺服器必須呼叫參數的 NdrFree 常式，則會設定 **MustFree** 位 \* 。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="f3c6e-149">**IsSimpleRef** 位是針對屬於其他指標以外之任何其他指標的參考指標而設定的，而且沒有配置屬性的參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="f3c6e-150">針對這類型別，參數描述的型別 \_ offset<> 欄位，除了基底型別的參考指標之外，還提供對參考型別的位移; 參考指標只會略過。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="f3c6e-151">**IsDontCallFreeInst** 位是針對特定的代表設定為 \_ 不應呼叫其免費實例常式的參數。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="f3c6e-152">如果參數為 \[ **out** \] 、 \[ **in** \] 或 \[ **in、out** 指標 \] 或 enum16 指標，且將在伺服器解譯器的堆疊上初始化 **\_**，則 ServerAllocSize 位為非零值，而不是使用 I RpcAllocate 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="f3c6e-153">如果是非零值，則這個值會乘以8以取得參數的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="f3c6e-154">請注意，這麼做表示一律會為指標配置至少8個位元組。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="f3c6e-155">**IsBasetype** 位是針對由 Main [**– Oif**](/windows/desktop/Midl/-oi)解譯器迴圈封送處理的簡單類型所設定。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="f3c6e-156">尤其是，在其上具有範圍屬性的簡單類型，並不會標示為基底類型，以強制使用 FC 範圍權杖來強制執行範圍常式封送處理 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="f3c6e-157">**IsByValue** 位是針對以傳值方式傳送的複合類型而設定，但不會針對簡單類型設定，不論引數是否為指標。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="f3c6e-158">其所設定的複合類型為結構、等位、 [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)， [**表示 \_ 為**](/windows/desktop/Midl/represent-as)、 [**連網 \_ 封送**](/windows/desktop/Midl/wire-marshal) 處理和 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="f3c6e-159">一般來說，在 [**– Oicf**](/windows/desktop/Midl/-oi) 解譯器中，主要解譯器迴圈的優點引進了位，以確保簡單引數 (稱為複合類型引數，) 可正確取值。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="f3c6e-160">先前的解譯器版本中從未使用過此位。</span><span class="sxs-lookup"><span data-stu-id="f3c6e-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 