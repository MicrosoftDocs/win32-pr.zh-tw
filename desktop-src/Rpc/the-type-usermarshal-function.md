---
title: Type_UserMarshal 函式
description: 型 \_ 別 UserMarshal 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: 3cbd78d1-a036-4d0d-bb1d-4c968acfdb36
keywords:
- type_UserMarshal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca4cc8ced4b84e21475960912f8e4ac2054d1c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382785"
---
# <a name="the-type_usermarshal-function"></a><span data-ttu-id="ef78d-104">型別 \_ UserMarshal 函式</span><span class="sxs-lookup"><span data-stu-id="ef78d-104">The type\_UserMarshal Function</span></span>

<span data-ttu-id="ef78d-105">**<type> \_ UserMarshal** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。</span><span class="sxs-lookup"><span data-stu-id="ef78d-105">The **<type>\_UserMarshal** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="ef78d-106">Stub 會呼叫這個函式，以在用戶端或伺服器端上封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="ef78d-106">The stubs call this function to marshal data on the client or server side.</span></span> <span data-ttu-id="ef78d-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="ef78d-107">The function is defined as:</span></span>

``` syntax
unsigned char __RPC_FAR * __RPC_USER  <type>_UserMarshal(
    unsigned long __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * pBuffer,
    <type>  __RPC_FAR *       pMyObj);
```

<span data-ttu-id="ef78d-108">函 <type> 式名稱中的，表示在 **\[ 有線 \_ 封送 \]** 處理或 **\[ 使用者 \_ 封 \] 送** 處理類型定義中指定的 userm 類型。</span><span class="sxs-lookup"><span data-stu-id="ef78d-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span> <span data-ttu-id="ef78d-109">此類型可以是 untransmittable 或甚至是在與 **\[ 使用者 \_ 封送 \]** 處理屬性搭配使用時，也就是 MIDL 編譯器的未知類型。</span><span class="sxs-lookup"><span data-stu-id="ef78d-109">This type may be untransmittable or even—when used with the **\[user\_marshal\]** attribute—a type unknown to the MIDL compiler.</span></span> <span data-ttu-id="ef78d-110">在函式原型中未使用 transmissible 類型) 名稱 (網路類型名稱。</span><span class="sxs-lookup"><span data-stu-id="ef78d-110">The wire type name (the name of transmissible type) is not used in the function prototype.</span></span> <span data-ttu-id="ef78d-111">不過，請注意，網路類型會定義憑證 DCE 所指定之資料的網路版面配置。</span><span class="sxs-lookup"><span data-stu-id="ef78d-111">Note, however, that the wire type defines the wire layout for the data as specified by OSF DCE.</span></span>

<span data-ttu-id="ef78d-112">*PFlags* 參數是不帶正負號的長旗標欄位的指標。</span><span class="sxs-lookup"><span data-stu-id="ef78d-112">The *pFlags* parameter is a pointer to an unsigned long flag field.</span></span> <span data-ttu-id="ef78d-113">旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。</span><span class="sxs-lookup"><span data-stu-id="ef78d-113">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="ef78d-114">下方的單字包含由 COM 通道所定義的封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="ef78d-114">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="ef78d-115">欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。</span><span class="sxs-lookup"><span data-stu-id="ef78d-115">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="ef78d-116">*PBuffer* 參數是目前的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="ef78d-116">The *pBuffer* parameter is the current buffer pointer.</span></span> <span data-ttu-id="ef78d-117">此指標不一定會在輸入時對齊。</span><span class="sxs-lookup"><span data-stu-id="ef78d-117">This pointer may or may not be aligned on entry.</span></span> <span data-ttu-id="ef78d-118">您的 **<type> \_ UserMarshal** 函式應適當地對齊緩衝區指標、封送處理資料，並傳回新的緩衝區位置，也就是封送處理物件之後第一個位元組的位址。</span><span class="sxs-lookup"><span data-stu-id="ef78d-118">Your **<type>\_UserMarshal** function should align the buffer pointer appropriately, marshal the data, and return the new buffer position, which is the address of the first byte after the marshaled object.</span></span> <span data-ttu-id="ef78d-119">請記住，網路類型規格會決定緩衝區中資料的實際版面配置。</span><span class="sxs-lookup"><span data-stu-id="ef78d-119">Keep in mind that the wire type specification determines the actual layout of the data in the buffer.</span></span>

<span data-ttu-id="ef78d-120">*PMyObj* 參數是使用者類型物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ef78d-120">The *pMyObj* parameter is a pointer to a user type object.</span></span>

<span data-ttu-id="ef78d-121">傳回值是新的緩衝區位置，也就是取消封送處理物件之後第一個位元組的位址。</span><span class="sxs-lookup"><span data-stu-id="ef78d-121">The return value is the new buffer position, which is the address of the first byte after the unmarshaled object.</span></span>

<span data-ttu-id="ef78d-122">當您不正確地計算資料的大小，並嘗試封送處理超過預期的資料時，可能會發生緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="ef78d-122">Buffer overflow can occur when you incorrectly calculate the size of the data and attempt to marshal more data than expected.</span></span> <span data-ttu-id="ef78d-123">請小心避免此情況。</span><span class="sxs-lookup"><span data-stu-id="ef78d-123">You should be careful to avoid this situation.</span></span> <span data-ttu-id="ef78d-124">您可以使用 **<type> \_ UserMarshal** 傳回的指標來檢查它。</span><span class="sxs-lookup"><span data-stu-id="ef78d-124">You can check against it by using the pointer that **<type>\_UserMarshal** returns.</span></span> <span data-ttu-id="ef78d-125">否則，您之後可能會有 NDR 引擎引發緩衝區溢位例外狀況的風險。</span><span class="sxs-lookup"><span data-stu-id="ef78d-125">Otherwise, you risk having the NDR engine raise a buffer-overflow exception later.</span></span>

<span data-ttu-id="ef78d-126">必須在本機攔截和處理例外狀況，不能允許例外狀況 propigated 呼叫堆疊。</span><span class="sxs-lookup"><span data-stu-id="ef78d-126">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef78d-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef78d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef78d-128">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="ef78d-128">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="ef78d-129">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="ef78d-129">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="ef78d-130">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="ef78d-130">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 