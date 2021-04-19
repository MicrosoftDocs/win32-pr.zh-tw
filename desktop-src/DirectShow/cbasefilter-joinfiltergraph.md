---
description: JoinFilterGraph 方法會通知篩選其已加入或離開篩選圖形。 這個方法會實 IBaseFilter：： JoinFilterGraph 方法。
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: 'CBaseFilter. JoinFilterGraph 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993607"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="e0694-104">CBaseFilter. JoinFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="e0694-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="e0694-105">`JoinFilterGraph`方法會通知篩選其已加入或離開篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="e0694-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="e0694-106">這個方法會實 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法。</span><span class="sxs-lookup"><span data-stu-id="e0694-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0694-107">語法</span><span class="sxs-lookup"><span data-stu-id="e0694-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="e0694-108">參數</span><span class="sxs-lookup"><span data-stu-id="e0694-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0694-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="e0694-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="e0694-110">篩選圖形管理員 [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) 介面的指標，如果篩選離開圖形，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e0694-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="e0694-111">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0694-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0694-112">包含篩選名稱的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="e0694-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0694-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0694-113">Return value</span></span>

<span data-ttu-id="e0694-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e0694-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0694-115">備註</span><span class="sxs-lookup"><span data-stu-id="e0694-115">Remarks</span></span>

<span data-ttu-id="e0694-116">這個方法會設定等於 *pGraph* 參數的 [**CBaseFilter：： m \_ pGraph**](cbasefilter-m-pgraph.md)成員變數。</span><span class="sxs-lookup"><span data-stu-id="e0694-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="e0694-117">它也會查詢 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面指標，並將它儲存在 [**CBaseFilter：： m \_ pSink**](cbasefilter-m-psink.md) 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="e0694-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="e0694-118">但是，篩選不會在其中一個介面上保留參考計數。</span><span class="sxs-lookup"><span data-stu-id="e0694-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="e0694-119">這麼做會建立迴圈參考計數，因為篩選圖形管理員會保留篩選的參考計數。</span><span class="sxs-lookup"><span data-stu-id="e0694-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="e0694-120">方法會將 *pName* 指定的字串複製到 [**CBaseFilter：： m \_ pName**](cbasefilter-m-pname.md) 成員變數中。</span><span class="sxs-lookup"><span data-stu-id="e0694-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0694-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0694-121">Requirements</span></span>



| <span data-ttu-id="e0694-122">需求</span><span class="sxs-lookup"><span data-stu-id="e0694-122">Requirement</span></span> | <span data-ttu-id="e0694-123">值</span><span class="sxs-lookup"><span data-stu-id="e0694-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0694-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e0694-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e0694-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e0694-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e0694-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e0694-126">Library</span></span><br/> | <dl> <span data-ttu-id="e0694-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e0694-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0694-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0694-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0694-129">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e0694-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




