---
description: DECLARE \_ IUNKNOWN 宏會為新介面宣告基底介面的三種方法。
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: 'DECLARE_IUNKNOWN (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984353"
---
# <a name="declare_iunknown"></a><span data-ttu-id="24714-103">宣告 \_ IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="24714-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="24714-104">**DECLARE \_ IUNKNOWN** 宏會為新介面宣告基底介面的三種方法。</span><span class="sxs-lookup"><span data-stu-id="24714-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="24714-105">**語法**</span><span class="sxs-lookup"><span data-stu-id="24714-105">**Syntax**</span></span>

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a><span data-ttu-id="24714-106">備註</span><span class="sxs-lookup"><span data-stu-id="24714-106">Remarks</span></span>

<span data-ttu-id="24714-107">當您建立新的介面時，它必須衍生自 **IUnknown**，其中有三個方法： **QueryInterface**、 **AddRef** 和 **Release**。</span><span class="sxs-lookup"><span data-stu-id="24714-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="24714-108">這個宏會針對新介面宣告這些方法，藉此簡化宣告程式。</span><span class="sxs-lookup"><span data-stu-id="24714-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="24714-109">這個宏只適用于直接或間接衍生自 [**CUnknown**](cunknown.md) 類別的類別。</span><span class="sxs-lookup"><span data-stu-id="24714-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="24714-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="24714-110">Requirements</span></span>



| <span data-ttu-id="24714-111">需求</span><span class="sxs-lookup"><span data-stu-id="24714-111">Requirement</span></span> | <span data-ttu-id="24714-112">值</span><span class="sxs-lookup"><span data-stu-id="24714-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24714-113">標頭</span><span class="sxs-lookup"><span data-stu-id="24714-113">Header</span></span><br/>  | <dl> <span data-ttu-id="24714-114"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="24714-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24714-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="24714-115">Library</span></span><br/> | <dl> <span data-ttu-id="24714-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="24714-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24714-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="24714-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24714-118">**COM Helper 函數**</span><span class="sxs-lookup"><span data-stu-id="24714-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="24714-119">**CUnknown：： GetOwner**</span><span class="sxs-lookup"><span data-stu-id="24714-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="24714-120">如何執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="24714-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




