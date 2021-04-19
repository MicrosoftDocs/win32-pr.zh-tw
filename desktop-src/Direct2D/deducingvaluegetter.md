---
title: 'DeducingValueGetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對實數值型別屬性呼叫成員函式屬性 getter 回呼。
ms.assetid: E2E5CCC3-B112-4D3C-8840-121A55C4F1A2
keywords:
- DeducingValueGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingValueGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd6eac823457882513f97557939db884efcf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995649"
---
# <a name="deducingvaluegetter"></a><span data-ttu-id="b4c52-104">DeducingValueGetter</span><span class="sxs-lookup"><span data-stu-id="b4c52-104">DeducingValueGetter</span></span>

<span data-ttu-id="b4c52-105">會推算類別和引數，然後針對實數值型別屬性呼叫成員函式屬性 getter 回呼。</span><span class="sxs-lookup"><span data-stu-id="b4c52-105">Deduces the class and arguments and then calls a member-function property getter callback for a value-type property.</span></span>

> [!Note]  
> <span data-ttu-id="b4c52-106">DeducingValueGetter 不應該直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="b4c52-106">DeducingValueGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename P, typename I>
HRESULT DeducingValueGetter(
    _In_ P (C::*callback)() const,
    _In_ const I *effect,
    _Out_writes_opt_(dataSize) BYTE *data,
    UINT32 dataSize,
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="b4c52-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4c52-107">Requirements</span></span>



| <span data-ttu-id="b4c52-108">需求</span><span class="sxs-lookup"><span data-stu-id="b4c52-108">Requirement</span></span> | <span data-ttu-id="b4c52-109">值</span><span class="sxs-lookup"><span data-stu-id="b4c52-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c52-110">標頭</span><span class="sxs-lookup"><span data-stu-id="b4c52-110">Header</span></span><br/> | <dl> <span data-ttu-id="b4c52-111"><dt>D2d1effecthelpers。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c52-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c52-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4c52-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c52-113">**Direct2D：:D educingValueSetter**</span><span class="sxs-lookup"><span data-stu-id="b4c52-113">**Direct2D::DeducingValueSetter**</span></span>](deducingvaluesetter.md)
</dt> </dl>

 

 





