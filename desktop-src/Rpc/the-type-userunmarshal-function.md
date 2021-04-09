---
title: Type_UserUnmarshal 函式
description: 型 \_ 別 UserUnmarshal 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: ee7a0e96-11ec-4d15-9d4b-55cc175fdd55
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332edbc2391aadf297789cc0ae862454786bdd8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104024051"
---
# <a name="the-type_userunmarshal-function"></a><span data-ttu-id="e9ee2-104">型別 \_ UserUnmarshal 函式</span><span class="sxs-lookup"><span data-stu-id="e9ee2-104">The type\_UserUnmarshal Function</span></span>

<span data-ttu-id="e9ee2-105">**<type> \_ UserUnmarshal** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-105">The **<type>\_UserUnmarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="e9ee2-106">Stub 會呼叫這個函式來 unmarshal 用戶端或伺服器端上的資料。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-106">The stubs call this function to unmarshal data on the client or server side.</span></span> <span data-ttu-id="e9ee2-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="e9ee2-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserUnmarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="e9ee2-108">函 <type> 式名稱中的，表示在 **\[ 有線 \_ 封送 \]** 處理或 **\[ 使用者 \_ 封 \] 送** 處理類型定義中指定的 userm 類型。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="e9ee2-109">這種類型在與 **\[ 使用者 \_ 封送 \]** 處理屬性（attribute）搭配使用時，可能是 UNTRANSMITTABLE 或甚至是： MIDL 編譯器的未知。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—unknown to the MIDL compiler.</span></span> <span data-ttu-id="e9ee2-110">在函式原型中未使用 transmissible 類型) 名稱 (網路類型名稱。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="e9ee2-111">不過，請注意，網路類型會定義憑證 DCE 所指定之資料的網路版面配置。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="e9ee2-112">*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-112">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="e9ee2-113">旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="e9ee2-114">下方的單字包含由 COM 通道所定義的封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="e9ee2-115">欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="e9ee2-116">*PBuffer* 參數是目前的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="e9ee2-117">此指標不一定會在輸入時對齊。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="e9ee2-118">您的 **<type> \_ UserUnmarshal** 函式應適當地對齊緩衝區指標，unmarshal 資料，並傳回新的緩衝區位置，也就是取消封送處理物件之後第一個位元組的位址。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-118">Your **<type>\_UserUnmarshal** function should align the buffer pointer appropriately, unmarshal the data, and return the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="e9ee2-119">*PMyObj* 參數是使用者定義型別物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-119">The *pMyObj* parameter is a pointer to a user-defined type object.</span></span>

<span data-ttu-id="e9ee2-120">在異類環境中，NDR 引擎會先執行任何必要的資料轉換，再呼叫 **<type> \_ UserUnmarshal** 函數。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-120">In a heterogeneous environment, the NDR engine performs any data conversion necessary before calling the **<type>\_UserUnmarshal** function.</span></span> <span data-ttu-id="e9ee2-121">請注意，「NDR 引擎」會根據針對此使用者資料類型所提供的網路類型定義來執行此資料轉換。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-121">Note that the NDR engine carries out this data conversion according to the wire-type definition supplied for this user data type.</span></span> <span data-ttu-id="e9ee2-122">旗標表示寄件者的資料標記法。</span><span class="sxs-lookup"><span data-stu-id="e9ee2-122">The flag indicates the data representation of the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9ee2-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="e9ee2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9ee2-124">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="e9ee2-124">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="e9ee2-125">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="e9ee2-125">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="e9ee2-126">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="e9ee2-126">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 