---
description: CEnumMediaTypes。 CEnumMediaTypes 函式-函數方法。
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095676"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="0b517-103">CEnumMediaTypes. CEnumMediaTypes 函數</span><span class="sxs-lookup"><span data-stu-id="0b517-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="0b517-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="0b517-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b517-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b517-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="0b517-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b517-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="0b517-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="0b517-108">要在其上執行列舉的釘選指標。</span><span class="sxs-lookup"><span data-stu-id="0b517-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="0b517-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="0b517-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="0b517-110">要複製之列舉值的 [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) 介面指標，或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0b517-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b517-111">備註</span><span class="sxs-lookup"><span data-stu-id="0b517-111">Remarks</span></span>

<span data-ttu-id="0b517-112">如果 *pEnumMediaTypes* 是 **Null**，這個方法會將列舉值初始化為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="0b517-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="0b517-113">否則，它會複製 *pEnumMediaTypes* 所指定之列舉值的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="0b517-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b517-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b517-114">Requirements</span></span>



| <span data-ttu-id="0b517-115">需求</span><span class="sxs-lookup"><span data-stu-id="0b517-115">Requirement</span></span> | <span data-ttu-id="0b517-116">值</span><span class="sxs-lookup"><span data-stu-id="0b517-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b517-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0b517-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0b517-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0b517-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0b517-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b517-119">Library</span></span><br/> | <dl> <span data-ttu-id="0b517-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0b517-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b517-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b517-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b517-122">**CEnumMediaTypes 類別**</span><span class="sxs-lookup"><span data-stu-id="0b517-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




