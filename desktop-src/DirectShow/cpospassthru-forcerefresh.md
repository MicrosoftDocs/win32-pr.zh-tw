---
description: ForceRefresh 方法已淘汰。
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: 'CPosPassThru. ForceRefresh 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977776"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="ca3ad-103">CPosPassThru. ForceRefresh 方法</span><span class="sxs-lookup"><span data-stu-id="ca3ad-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="ca3ad-104">`ForceRefresh`方法已淘汰。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca3ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="ca3ad-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="ca3ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="ca3ad-106">Parameters</span></span>

<span data-ttu-id="ca3ad-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca3ad-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca3ad-108">Return value</span></span>

<span data-ttu-id="ca3ad-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca3ad-110">備註</span><span class="sxs-lookup"><span data-stu-id="ca3ad-110">Remarks</span></span>

<span data-ttu-id="ca3ad-111">此類別原本是設計來快取連接的釘選 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="ca3ad-112">`ForceRefresh`方法會釋放這些介面。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="ca3ad-113">目前已執行，這個類別不會快取這些介面。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="ca3ad-114">為了提供相容性， `ForceRefresh` 仍會包含方法，但不會執行任何作業，而會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="ca3ad-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca3ad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca3ad-115">Requirements</span></span>



| <span data-ttu-id="ca3ad-116">需求</span><span class="sxs-lookup"><span data-stu-id="ca3ad-116">Requirement</span></span> | <span data-ttu-id="ca3ad-117">值</span><span class="sxs-lookup"><span data-stu-id="ca3ad-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca3ad-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ca3ad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ca3ad-119"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ca3ad-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca3ad-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ca3ad-120">Library</span></span><br/> | <dl> <span data-ttu-id="ca3ad-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ca3ad-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca3ad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca3ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca3ad-123">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="ca3ad-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




