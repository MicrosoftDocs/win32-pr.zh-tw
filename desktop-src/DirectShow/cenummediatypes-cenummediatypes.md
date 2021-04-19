---
description: 函式方法。
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: 'CEnumMediaTypes. CEnumMediaTypes (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995359"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="b8fea-103">CEnumMediaTypes. CEnumMediaTypes 函數</span><span class="sxs-lookup"><span data-stu-id="b8fea-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="b8fea-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="b8fea-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fea-105">語法</span><span class="sxs-lookup"><span data-stu-id="b8fea-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="b8fea-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8fea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8fea-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b8fea-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b8fea-108">要在其上執行列舉的釘選指標。</span><span class="sxs-lookup"><span data-stu-id="b8fea-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="b8fea-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="b8fea-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="b8fea-110">要複製之列舉值的 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b8fea-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8fea-111">備註</span><span class="sxs-lookup"><span data-stu-id="b8fea-111">Remarks</span></span>

<span data-ttu-id="b8fea-112">如果 *pEnumMediaTypes* 是 **Null**，這個方法會將列舉值初始化為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="b8fea-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="b8fea-113">否則，它會複製 *pEnumMediaTypes* 所指定之列舉值的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="b8fea-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8fea-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8fea-114">Requirements</span></span>



| <span data-ttu-id="b8fea-115">需求</span><span class="sxs-lookup"><span data-stu-id="b8fea-115">Requirement</span></span> | <span data-ttu-id="b8fea-116">值</span><span class="sxs-lookup"><span data-stu-id="b8fea-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8fea-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b8fea-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b8fea-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b8fea-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b8fea-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b8fea-119">Library</span></span><br/> | <dl> <span data-ttu-id="b8fea-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b8fea-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8fea-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8fea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8fea-122">**CEnumMediaTypes 類別**</span><span class="sxs-lookup"><span data-stu-id="b8fea-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




