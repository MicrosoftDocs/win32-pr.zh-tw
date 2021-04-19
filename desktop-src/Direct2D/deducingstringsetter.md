---
title: 'DeducingStringSetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 setter 回呼。
ms.assetid: D3075B7B-D253-4F85-9FD2-3487C4207122
keywords:
- DeducingStringSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingStringSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7860978fd271b2ff395caae068cd651d3057020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982642"
---
# <a name="deducingstringsetter"></a><span data-ttu-id="3fc94-104">DeducingStringSetter</span><span class="sxs-lookup"><span data-stu-id="3fc94-104">DeducingStringSetter</span></span>

<span data-ttu-id="3fc94-105">會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 setter 回呼。</span><span class="sxs-lookup"><span data-stu-id="3fc94-105">Deduces the class and arguments and then calls a member-function property setter callback for a string-type property.</span></span>

> [!Note]  
> <span data-ttu-id="3fc94-106">DeducingStringSetter 不應該直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="3fc94-106">DeducingStringSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingStringSetter(  
    _In_ HRESULT (C::*callback)(PCWSTR string),
    _In_ I *effect,
    _In_reads_(dataSize) const BYTE *data,
    UINT32 dataSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="3fc94-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fc94-107">Requirements</span></span>



| <span data-ttu-id="3fc94-108">需求</span><span class="sxs-lookup"><span data-stu-id="3fc94-108">Requirement</span></span> | <span data-ttu-id="3fc94-109">值</span><span class="sxs-lookup"><span data-stu-id="3fc94-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc94-110">標頭</span><span class="sxs-lookup"><span data-stu-id="3fc94-110">Header</span></span><br/> | <dl> <span data-ttu-id="3fc94-111"><dt>D2d1effecthelpers。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc94-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc94-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fc94-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc94-113">**Direct2D：:D educingStringGetter**</span><span class="sxs-lookup"><span data-stu-id="3fc94-113">**Direct2D::DeducingStringGetter**</span></span>](deducingstringgetter.md)
</dt> </dl>

 

 





