---
title: User_marshal 和 wire_marshal 的封送處理規則
description: 封送處理內嵌指標類型的憑證-DCE 規格需要您在實 \_ UserSize、型別 \_ UserMarshal 和型別 UserUnMarshal 函式時觀察下列限制 \_ 。
ms.assetid: 077cdd1a-9630-459e-8749-ab0c70b16ecb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4d201f05787ac0b122766ba7fb662532320c43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682747"
---
# <a name="marshaling-rules-for-user_marshal-and-wire_marshal"></a><span data-ttu-id="9dbdf-103">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="9dbdf-103">Marshaling Rules for user\_marshal and wire\_marshal</span></span>

<span data-ttu-id="9dbdf-104">封送處理內嵌指標類型的憑證-DCE 規格需要您在實 <type> \_ UserSize、 <type> \_ UserMarshal 和 <type> \_ UserUnMarshal 函式時觀察到下列限制。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-104">The OSF-DCE specification for marshaling embedded pointer types requires that you observe the following restrictions when implementing the <type>\_UserSize, <type>\_UserMarshal, and <type>\_UserUnMarshal functions.</span></span> <span data-ttu-id="9dbdf-105"> (此處提供的規則和範例適用于封送處理。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-105">(The rules and examples given here are for marshaling.</span></span> <span data-ttu-id="9dbdf-106">不過，您的大小調整和封送送出常式必須遵循相同的限制) ：</span><span class="sxs-lookup"><span data-stu-id="9dbdf-106">However, your sizing and unmarshaling routines must follow the same restrictions):</span></span>

-   <span data-ttu-id="9dbdf-107">如果連線類型是沒有指標的一般類型，則對應 userm 類型的封送處理常式應該只會根據網路類型的配置封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-107">If the wire-type is a flat type with no pointers, your marshaling routine for the corresponding userm-type should simply marshal the data according to the layout of the wire-type.</span></span> <span data-ttu-id="9dbdf-108">例如：</span><span class="sxs-lookup"><span data-stu-id="9dbdf-108">For example:</span></span>

    ``` syntax
    typedef [wire_marshal (long)] void * HANDLE_HANDLE;
    ```

    <span data-ttu-id="9dbdf-109">請注意，網路類型 **long** 是一種平面類型。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-109">Note that the wire type, **long**, is a flat type.</span></span> <span data-ttu-id="9dbdf-110">只要將控制碼控制碼物件傳遞給控制碼，UserMarshal 函式就 \_ \_ 會封送處理 \_ 。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-110">Your HANDLE\_HANDLE\_UserMarshal function marshals a **long** whenever a HANDLE\_HANDLE object is passed to it.</span></span>

-   <span data-ttu-id="9dbdf-111">如果連線類型是另一種類型的指標，則對應 userm 型別的封送處理常式應該會根據有線型別所指向之類型的版面配置來封送處理資料。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-111">If the wire-type is a pointer to another type, your marshaling routine for the corresponding userm-type should marshal the data according to the layout for the type that the wire-type points to.</span></span> <span data-ttu-id="9dbdf-112">NDR 引擎負責處理指標。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-112">The NDR engine takes care of the pointer.</span></span> <span data-ttu-id="9dbdf-113">例如：</span><span class="sxs-lookup"><span data-stu-id="9dbdf-113">For example:</span></span>

    ``` syntax
    typedef struct HDATA
    {
        long size;
        [size_is(size)] long * pData;
    } HDATA;

    typedef HDATA * WIRE_TYPE;
    typedef [wire_marshal(WIRE_TYPE)] void * HANDLE_DATA;
    ```

    <span data-ttu-id="9dbdf-114">請注意，網路類型 [ **電傳 \_ 類型]** 是指標類型。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-114">Note that the wire type, **WIRE\_TYPE**, is a pointer type.</span></span> <span data-ttu-id="9dbdf-115">您的控制碼資料 UserMarshal 函式會 \_ \_ 使用 HDATA 配置（而非 HDATA 配置）來封送處理與控制碼相關的資料 \* 。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-115">Your HANDLE\_DATA\_UserMarshal function marshals the data related to the handle, using the HDATA layout, rather than the HDATA \* layout.</span></span>

-   <span data-ttu-id="9dbdf-116">有線類型必須是一般資料類型或指標類型。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-116">A wire-type must be either a flat data type or a pointer type.</span></span> <span data-ttu-id="9dbdf-117">如果您的 transmissible 類型必須是其他 (具有指標的結構，例如) ，請使用您想要的型別指標作為網路類型。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-117">If your transmissible type must be something else (a structure with pointers, for example), use a pointer to your desired type as the wire-type.</span></span>

<span data-ttu-id="9dbdf-118">這些限制的影響是以 \[ [**網路 \_ 封送**](/windows/desktop/Midl/wire-marshal)處理 \] 或 \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理屬性定義的類型 \] 可以自由地內嵌在其他類型中。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-118">The effect of these restrictions is that the types defined with the \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\] or \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\] attributes can be freely embedded in other types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dbdf-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="9dbdf-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dbdf-120">**網路 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-120">**wire\_marshal**</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="9dbdf-121">**使用者 \_ 封送處理**</span><span class="sxs-lookup"><span data-stu-id="9dbdf-121">**user\_marshal**</span></span>](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[<span data-ttu-id="9dbdf-122">型別 \_ UserSize 函式</span><span class="sxs-lookup"><span data-stu-id="9dbdf-122">The type\_UserSize Function</span></span>](the-type-usersize-function.md)
</dt> <dt>

[<span data-ttu-id="9dbdf-123">型別 \_ UserMarshal 函式</span><span class="sxs-lookup"><span data-stu-id="9dbdf-123">The type\_UserMarshal Function</span></span>](the-type-usermarshal-function.md)
</dt> <dt>

[<span data-ttu-id="9dbdf-124">Thetype \_ UserUnMarshalFunction</span><span class="sxs-lookup"><span data-stu-id="9dbdf-124">Thetype\_UserUnMarshalFunction</span></span>](the-type-userunmarshal-function.md)
</dt> <dt>

[<span data-ttu-id="9dbdf-125">Thetype \_ UserFreeFunction</span><span class="sxs-lookup"><span data-stu-id="9dbdf-125">Thetype\_UserFreeFunction</span></span>](the-type-userfree-function.md)
</dt> </dl>

 

 