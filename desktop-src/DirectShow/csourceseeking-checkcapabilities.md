---
description: CheckCapabilities 方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 IMediaSeeking：： CheckCapabilities 方法。
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: 'CSourceSeeking. CheckCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994209"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="d2438-104">CSourceSeeking. CheckCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="d2438-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="d2438-105">`CheckCapabilities`方法會查詢資料流程是否已指定搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="d2438-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="d2438-106">這個方法會實 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="d2438-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2438-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2438-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="d2438-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2438-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2438-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="d2438-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="d2438-110">一或多個搜尋中搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 屬性的位元組合指標。</span><span class="sxs-lookup"><span data-stu-id="d2438-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2438-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2438-111">Return value</span></span>

<span data-ttu-id="d2438-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d2438-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d2438-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d2438-113">Return code</span></span>                                                                               | <span data-ttu-id="d2438-114">Description</span><span class="sxs-lookup"><span data-stu-id="d2438-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2438-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d2438-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="d2438-116">並非 *pCapabilities* 中的所有功能都存在。</span><span class="sxs-lookup"><span data-stu-id="d2438-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="d2438-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d2438-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d2438-118">*PCapabilities* 中的所有功能都存在。</span><span class="sxs-lookup"><span data-stu-id="d2438-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="d2438-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="d2438-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d2438-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="d2438-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="d2438-121">備註</span><span class="sxs-lookup"><span data-stu-id="d2438-121">Remarks</span></span>

<span data-ttu-id="d2438-122">如同實，這個方法會根據 [**CSourceSeeking：： m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md)成員變數來檢查 *\* pCapabilities* 的值。</span><span class="sxs-lookup"><span data-stu-id="d2438-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="d2438-123">但是，它不會將 *\* pCapabilities* 設定為等於 **m \_ dwSeekingCaps**，如 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)方法所述。</span><span class="sxs-lookup"><span data-stu-id="d2438-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="d2438-124">此外，如果沒有任何指定的功能可供使用，則該方法不會傳回 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="d2438-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="d2438-125">更完整的實施方式如下：</span><span class="sxs-lookup"><span data-stu-id="d2438-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d2438-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2438-126">Requirements</span></span>



| <span data-ttu-id="d2438-127">需求</span><span class="sxs-lookup"><span data-stu-id="d2438-127">Requirement</span></span> | <span data-ttu-id="d2438-128">值</span><span class="sxs-lookup"><span data-stu-id="d2438-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2438-129">標頭</span><span class="sxs-lookup"><span data-stu-id="d2438-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d2438-130"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d2438-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2438-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="d2438-131">Library</span></span><br/> | <dl> <span data-ttu-id="d2438-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d2438-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2438-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2438-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2438-134">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="d2438-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




