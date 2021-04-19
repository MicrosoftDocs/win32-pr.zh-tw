---
description: QueryFilterInfo 方法會捕獲篩選的相關資訊。 這個方法會實 IBaseFilter：： QueryFilterInfo 方法。
ms.assetid: 0c25aa9e-933c-4c45-a1cc-ffc9253dd561
title: 'CBaseFilter. QueryFilterInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryFilterInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a706663c1fb39e0e2e84b4097ec620f9e608843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979602"
---
# <a name="cbasefilterqueryfilterinfo-method"></a><span data-ttu-id="c2057-104">CBaseFilter. QueryFilterInfo 方法</span><span class="sxs-lookup"><span data-stu-id="c2057-104">CBaseFilter.QueryFilterInfo method</span></span>

<span data-ttu-id="c2057-105">方法會抓取 `QueryFilterInfo` 篩選的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c2057-105">The `QueryFilterInfo` method retrieves information about the filter.</span></span> <span data-ttu-id="c2057-106">這個方法會實 [**IBaseFilter：： QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="c2057-106">This method implements the [**IBaseFilter::QueryFilterInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2057-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2057-107">Syntax</span></span>


```C++
HRESULT QueryFilterInfo(
   FILTER_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c2057-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2057-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2057-109">*pInfo*</span><span class="sxs-lookup"><span data-stu-id="c2057-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c2057-110">[**篩選 \_ 資訊**](/windows/win32/api/strmif/ns-strmif-filter_info)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c2057-110">Pointer to a [**FILTER\_INFO**](/windows/win32/api/strmif/ns-strmif-filter_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2057-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2057-111">Return value</span></span>

<span data-ttu-id="c2057-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="c2057-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2057-113">備註</span><span class="sxs-lookup"><span data-stu-id="c2057-113">Remarks</span></span>

<span data-ttu-id="c2057-114">這個方法會將篩選的名稱從 [**CBaseFilter：： m \_ pName**](cbasefilter-m-pname.md) 成員變數複製到篩選資訊結構的 **achName** 成員中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c2057-114">This method copies the filter's name from the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable into the **achName** member of the FILTER\_INFO structure.</span></span> <span data-ttu-id="c2057-115">如果 **m \_ PName** 為 **Null**，則方法會將 **achName** 設定為 L ' \\ 0 '。</span><span class="sxs-lookup"><span data-stu-id="c2057-115">If **m\_pName** is **NULL**, the method sets **achName** to L'\\0'.</span></span>

<span data-ttu-id="c2057-116">方法會將篩選資訊結構的 **pGraph** 成員設定 \_ 為等於 [**CBaseFilter：： m \_ pGraph**](cbasefilter-m-pgraph.md) 成員變數，並遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="c2057-116">The method sets the **pGraph** member of the FILTER\_INFO structure equal to the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable, and increments the reference count.</span></span> <span data-ttu-id="c2057-117">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="c2057-117">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2057-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2057-118">Requirements</span></span>



| <span data-ttu-id="c2057-119">需求</span><span class="sxs-lookup"><span data-stu-id="c2057-119">Requirement</span></span> | <span data-ttu-id="c2057-120">值</span><span class="sxs-lookup"><span data-stu-id="c2057-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2057-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c2057-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c2057-122"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c2057-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c2057-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2057-123">Library</span></span><br/> | <dl> <span data-ttu-id="c2057-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c2057-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2057-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2057-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2057-126">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c2057-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




