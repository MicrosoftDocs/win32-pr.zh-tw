---
title: 'DeducingBlobSetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 setter 回呼。
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- DeducingBlobSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d3bbfcc0a48d722bd98456821d7f7df5e8780a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978417"
---
# <a name="deducingblobsetter"></a><span data-ttu-id="b1965-104">DeducingBlobSetter</span><span class="sxs-lookup"><span data-stu-id="b1965-104">DeducingBlobSetter</span></span>

<span data-ttu-id="b1965-105">會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 setter 回呼。</span><span class="sxs-lookup"><span data-stu-id="b1965-105">Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="b1965-106">DeducingBlobSetter 不應該直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="b1965-106">DeducingBlobSetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="b1965-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1965-107">Requirements</span></span>



| <span data-ttu-id="b1965-108">需求</span><span class="sxs-lookup"><span data-stu-id="b1965-108">Requirement</span></span> | <span data-ttu-id="b1965-109">值</span><span class="sxs-lookup"><span data-stu-id="b1965-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1965-110">標頭</span><span class="sxs-lookup"><span data-stu-id="b1965-110">Header</span></span><br/> | <dl> <span data-ttu-id="b1965-111"><dt>D2d1effecthelpers。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1965-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1965-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1965-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1965-113">**Direct2D：:D educingBlobGetter**</span><span class="sxs-lookup"><span data-stu-id="b1965-113">**Direct2D::DeducingBlobGetter**</span></span>](deducingblobgetter.md)
</dt> </dl>

 

 





