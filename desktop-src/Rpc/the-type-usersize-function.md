---
title: Type_UserSize 函式
description: 型 \_ 別 UserSize 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29e5936763f9fe7b3513d66ddca7db9c35dbfe7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683037"
---
# <a name="the-type_usersize-function"></a><span data-ttu-id="74117-104">型別 \_ UserSize 函式</span><span class="sxs-lookup"><span data-stu-id="74117-104">The type\_UserSize Function</span></span>

<span data-ttu-id="74117-105">**<type> \_ UserSize** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。</span><span class="sxs-lookup"><span data-stu-id="74117-105">The **<type>\_UserSize** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="74117-106">在用戶端或伺服器端將資料封送處理之前，存根會呼叫這個函式來調整使用者資料物件的 RPC 資料緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="74117-106">The stubs call this function to size the RPC data buffer for the user data object before the data is marshaled on the client or server side.</span></span> <span data-ttu-id="74117-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="74117-107">The function is defined as:</span></span>

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

<span data-ttu-id="74117-108">函 <type> 式名稱中的表示 userm 類型，如 **\[ 有線 \_ 封 \] 送** 處理或 **\[ 使用者 \_ 封送 \]** 處理類型定義中所指定。</span><span class="sxs-lookup"><span data-stu-id="74117-108">The <type> in the function name means the userm-type, as specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="74117-109">這種類型在與 **\[ 使用者 \_ 封送 \]** 處理屬性（attribute）搭配使用時，可能是 UNTRANSMITTABLE 或甚至是： MIDL 編譯器的未知。</span><span class="sxs-lookup"><span data-stu-id="74117-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute— unknown to the MIDL compiler.</span></span> <span data-ttu-id="74117-110">網路類型名稱 (在網路) 傳輸的類型名稱，不會用在函式原型中。</span><span class="sxs-lookup"><span data-stu-id="74117-110">The wire type name (the name of the type transmitted across the network) is not used in the function prototype.</span></span> <span data-ttu-id="74117-111">不過，請注意，網路類型會定義憑證 DCE 所指定之資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="74117-111">Note, however, that the wire type defines the layout for the data as specified by OSF DCE.</span></span> <span data-ttu-id="74117-112">所有資料都必須轉換成 (NDR) 格式的網路資料標記法。</span><span class="sxs-lookup"><span data-stu-id="74117-112">All data must be converted to network data representation (NDR) format.</span></span>

<span data-ttu-id="74117-113">*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。</span><span class="sxs-lookup"><span data-stu-id="74117-113">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="74117-114">旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 格式旗標。</span><span class="sxs-lookup"><span data-stu-id="74117-114">The upper word of the flag contains NDR format flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="74117-115">下方的單字包含由 COM 通道所定義的封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="74117-115">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="74117-116">下表會顯示欄位內旗標的確切版面配置。</span><span class="sxs-lookup"><span data-stu-id="74117-116">The exact layout of the flags within the field is shown in the following table.</span></span>



| <span data-ttu-id="74117-117">Bits</span><span class="sxs-lookup"><span data-stu-id="74117-117">Bits</span></span>  | <span data-ttu-id="74117-118">旗標</span><span class="sxs-lookup"><span data-stu-id="74117-118">Flag</span></span>                                  | <span data-ttu-id="74117-119">值</span><span class="sxs-lookup"><span data-stu-id="74117-119">Value</span></span>                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="74117-120">31-24</span><span class="sxs-lookup"><span data-stu-id="74117-120">31-24</span></span> | <span data-ttu-id="74117-121">浮點數標記法</span><span class="sxs-lookup"><span data-stu-id="74117-121">Floating-point representation</span></span>         | <span data-ttu-id="74117-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span><span class="sxs-lookup"><span data-stu-id="74117-122">0 = IEEE 1 = VAX 2 = Cray 3 = IBM</span></span>                                                         |
| <span data-ttu-id="74117-123">23-20</span><span class="sxs-lookup"><span data-stu-id="74117-123">23-20</span></span> | <span data-ttu-id="74117-124">整數和浮點位元組順序</span><span class="sxs-lookup"><span data-stu-id="74117-124">Integer and floating-point byte order</span></span> | <span data-ttu-id="74117-125">0 = 位元組由大到小的 1 = 位元組由小到大</span><span class="sxs-lookup"><span data-stu-id="74117-125">0 = Big-endian 1 = Little-endian</span></span>                                                          |
| <span data-ttu-id="74117-126">19-16</span><span class="sxs-lookup"><span data-stu-id="74117-126">19-16</span></span> | <span data-ttu-id="74117-127">字元標記法</span><span class="sxs-lookup"><span data-stu-id="74117-127">Character representation</span></span>              | <span data-ttu-id="74117-128">0 = ASCII 1 = EBCDIC</span><span class="sxs-lookup"><span data-stu-id="74117-128">0 = ASCII 1 = EBCDIC</span></span>                                                                      |
| <span data-ttu-id="74117-129">15-0</span><span class="sxs-lookup"><span data-stu-id="74117-129">15-0</span></span>  | <span data-ttu-id="74117-130">封送處理內容旗標</span><span class="sxs-lookup"><span data-stu-id="74117-130">Marshaling context flag</span></span>               | <span data-ttu-id="74117-131">0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC</span><span class="sxs-lookup"><span data-stu-id="74117-131">0 = MSHCTX\_LOCAL 1 = MSHCTX\_NOSHAREDMEM 2 = MSHCTX\_DIFFERENTMACHINE 3 = MSHCTX\_INPROC</span></span> |



 

<span data-ttu-id="74117-132">封送處理內容旗標可讓您根據 RPC 呼叫的內容改變常式的行為。</span><span class="sxs-lookup"><span data-stu-id="74117-132">The marshaling context flag makes it possible to alter the behavior of your routine depending on the context for the RPC call.</span></span> <span data-ttu-id="74117-133">比方說，如果您有一個控制碼 (**長**) 至資料區塊，您可以傳送同進程呼叫的控制碼，但您會將呼叫的實際資料傳送給不同的電腦。</span><span class="sxs-lookup"><span data-stu-id="74117-133">For example, if you have a handle (**long**) to a block of data, you could send the handle for an in-process call, but you would send the actual data for a call to a different machine.</span></span> <span data-ttu-id="74117-134">封送處理內容旗標及其值會定義在平臺軟體發展工具組 (SDK) 的 Wtypes.h .h 和 Wtypes.h .idl 檔案中。</span><span class="sxs-lookup"><span data-stu-id="74117-134">The marshaling context flag and its values are defined in the Wtypes.h and Wtypes.idl files in the Platform Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="74117-135">正確定義網路類型時，您不需要使用 NDR 格式旗標，因為 NDR 引擎會執行必要的轉換。</span><span class="sxs-lookup"><span data-stu-id="74117-135">When the wire type is properly defined, you do not have to use the NDR format flags, as the NDR engine performs the necessary conversions.</span></span>

 

<span data-ttu-id="74117-136">*StartingSize* 參數是目前的緩衝區位移。</span><span class="sxs-lookup"><span data-stu-id="74117-136">The *StartingSize* a parameter is the current buffer offset.</span></span> <span data-ttu-id="74117-137">起始大小表示使用者物件的緩衝區位移，且可能會正確對齊。</span><span class="sxs-lookup"><span data-stu-id="74117-137">The starting size indicates the buffer offset for the user object, and it may or may not be aligned properly.</span></span> <span data-ttu-id="74117-138">您的常式應考慮需要什麼填補。</span><span class="sxs-lookup"><span data-stu-id="74117-138">Your routine should account for whatever padding is necessary.</span></span>

<span data-ttu-id="74117-139">*PMyObj* 參數是使用者類型物件的指標。</span><span class="sxs-lookup"><span data-stu-id="74117-139">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="74117-140">傳回值是新的位移或緩衝區位置。</span><span class="sxs-lookup"><span data-stu-id="74117-140">The return value is the new offset or buffer position.</span></span> <span data-ttu-id="74117-141">函數應該會傳回累計大小，也就是開始大小加上可能的填補加上資料大小。</span><span class="sxs-lookup"><span data-stu-id="74117-141">The function should return the cumulative size, which is the starting size plus possible padding plus the data size.</span></span>

<span data-ttu-id="74117-142">**<type> \_ UserSize** 函數可以傳回所需大小的高估值。</span><span class="sxs-lookup"><span data-stu-id="74117-142">The **<type>\_UserSize** function can return an overestimate of the size needed.</span></span> <span data-ttu-id="74117-143">傳送緩衝區的實際大小是由資料大小所定義，而不是由緩衝區配置大小所定義。</span><span class="sxs-lookup"><span data-stu-id="74117-143">The actual size of the sent buffer is defined by the data size, not by the buffer allocation size.</span></span>

<span data-ttu-id="74117-144">如果可以在編譯時期計算網路大小，則不會呼叫 **<type> \_ UserSize** 函數。</span><span class="sxs-lookup"><span data-stu-id="74117-144">The **<type>\_UserSize** function is not called if the wire size can be computed at compile time.</span></span> <span data-ttu-id="74117-145">請注意，對於大部分的等位，即使沒有指標，也只能在執行時間決定網路標記法的實際大小。</span><span class="sxs-lookup"><span data-stu-id="74117-145">Note that for most unions, even if there are no pointers, the actual size of the wire representation can be determined only at run time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74117-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="74117-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74117-147">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="74117-147">Marshaling rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="74117-148">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="74117-148">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="74117-149">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="74117-149">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 