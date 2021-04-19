---
title: 'DeducingBlobGetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 getter 回呼。
ms.assetid: 1B8800CB-2AD0-4684-99D7-986F6C53A6F1
keywords:
- DeducingBlobGetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobGetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ca5cc37a9fbd79807e258a87a199be7319ce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997719"
---
# <a name="deducingblobgetter"></a><span data-ttu-id="29840-104">DeducingBlobGetter</span><span class="sxs-lookup"><span data-stu-id="29840-104">DeducingBlobGetter</span></span>

<span data-ttu-id="29840-105">會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 getter 回呼。</span><span class="sxs-lookup"><span data-stu-id="29840-105">Deduces the class and arguments and then calls a member-function property getter callback for a blob-type property.</span></span>

> [!Note]  
> <span data-ttu-id="29840-106">DeducingBlobGetter 不應該直接呼叫。</span><span class="sxs-lookup"><span data-stu-id="29840-106">DeducingBlobGetter should not be called directly.</span></span>

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobGetter(  
    _In_ HRESULT (C::*callback)(BYTE *, UINT32, UINT32*) const,  
    _In_ const I *effect,  
    _Out_writes_opt_(dataSize) BYTE *data,  
    UINT32 dataSize,  
    _Out_opt_ UINT32 *actualSize  
    ) 
```

## <a name="requirements"></a><span data-ttu-id="29840-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="29840-107">Requirements</span></span>



| <span data-ttu-id="29840-108">需求</span><span class="sxs-lookup"><span data-stu-id="29840-108">Requirement</span></span> | <span data-ttu-id="29840-109">值</span><span class="sxs-lookup"><span data-stu-id="29840-109">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29840-110">標頭</span><span class="sxs-lookup"><span data-stu-id="29840-110">Header</span></span><br/> | <dl> <span data-ttu-id="29840-111"><dt>D2d1effecthelpers。h</dt></span><span class="sxs-lookup"><span data-stu-id="29840-111"><dt>D2d1effecthelpers.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29840-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29840-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29840-113">**Direct2D：:D educingBlobSetter**</span><span class="sxs-lookup"><span data-stu-id="29840-113">**Direct2D::DeducingBlobSetter**</span></span>](deducingblobsetter.md)
</dt> </dl>

 

 





