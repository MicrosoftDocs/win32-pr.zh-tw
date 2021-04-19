---
description: Stop 方法會停止物件。 這個方法會實 IMediaFilter：： Stop 方法。
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: 'CBaseMediaFilter. Stop 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993473"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="6edfd-104">CBaseMediaFilter. Stop 方法</span><span class="sxs-lookup"><span data-stu-id="6edfd-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="6edfd-105">`Stop`方法會停止物件。</span><span class="sxs-lookup"><span data-stu-id="6edfd-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="6edfd-106">這個方法會實 [**IMediaFilter：： Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) 方法。</span><span class="sxs-lookup"><span data-stu-id="6edfd-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edfd-107">語法</span><span class="sxs-lookup"><span data-stu-id="6edfd-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="6edfd-108">參數</span><span class="sxs-lookup"><span data-stu-id="6edfd-108">Parameters</span></span>

<span data-ttu-id="6edfd-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6edfd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6edfd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6edfd-110">Return value</span></span>

<span data-ttu-id="6edfd-111">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6edfd-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edfd-112">備註</span><span class="sxs-lookup"><span data-stu-id="6edfd-112">Remarks</span></span>

<span data-ttu-id="6edfd-113">在基類中，這個方法會將 [**CBaseMediaFilter：： m \_ state**](cbasemediafilter-m-state.md) 成員變數設定為 State \_ 已停止，但不執行任何其他動作。</span><span class="sxs-lookup"><span data-stu-id="6edfd-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edfd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6edfd-114">Requirements</span></span>



| <span data-ttu-id="6edfd-115">需求</span><span class="sxs-lookup"><span data-stu-id="6edfd-115">Requirement</span></span> | <span data-ttu-id="6edfd-116">值</span><span class="sxs-lookup"><span data-stu-id="6edfd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edfd-117">標頭</span><span class="sxs-lookup"><span data-stu-id="6edfd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6edfd-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6edfd-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6edfd-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="6edfd-119">Library</span></span><br/> | <dl> <span data-ttu-id="6edfd-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6edfd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6edfd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6edfd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6edfd-122">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="6edfd-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




