---
description: QueryVendorInfo 方法會抓取包含廠商資訊的字串。 這個方法會實 IBaseFilter：： QueryVendorInfo 方法。
ms.assetid: 083c0556-d516-4daf-8621-e158ea78b5a3
title: 'CBaseFilter. QueryVendorInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.QueryVendorInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1786477c042bb1d9ecc6340056a771141d0a3c74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994904"
---
# <a name="cbasefilterqueryvendorinfo-method"></a><span data-ttu-id="4e603-104">CBaseFilter. QueryVendorInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4e603-104">CBaseFilter.QueryVendorInfo method</span></span>

<span data-ttu-id="4e603-105">方法會抓取 `QueryVendorInfo` 包含廠商資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="4e603-105">The `QueryVendorInfo` method retrieves a string containing vendor information.</span></span> <span data-ttu-id="4e603-106">這個方法會實 [**IBaseFilter：： QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="4e603-106">This method implements the [**IBaseFilter::QueryVendorInfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryvendorinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e603-107">語法</span><span class="sxs-lookup"><span data-stu-id="4e603-107">Syntax</span></span>


```C++
HRESULT QueryVendorInfo(
   LPWSTR *pVendorInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e603-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e603-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e603-109">*pVendorInfo*</span><span class="sxs-lookup"><span data-stu-id="4e603-109">*pVendorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4e603-110">變數的位址，此變數會接收包含廠商資訊之寬字元字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4e603-110">Address of a variable that receives a pointer to a wide-character string containing the vendor information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e603-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e603-111">Return value</span></span>

<span data-ttu-id="4e603-112">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="4e603-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e603-113">備註</span><span class="sxs-lookup"><span data-stu-id="4e603-113">Remarks</span></span>

<span data-ttu-id="4e603-114">若要提供篩選準則的廠商資訊，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="4e603-114">To provide vendor information for a filter, override this method.</span></span> <span data-ttu-id="4e603-115">如果您執行此方法，請使用 **CoTaskMemAlloc** 函數來配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="4e603-115">If you implement this method, use the **CoTaskMemAlloc** function to allocate memory for the string.</span></span> <span data-ttu-id="4e603-116">呼叫端負責呼叫 **CoTaskMemFree** 函數。</span><span class="sxs-lookup"><span data-stu-id="4e603-116">The caller is responsible for calling the **CoTaskMemFree** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e603-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e603-117">Requirements</span></span>



| <span data-ttu-id="4e603-118">需求</span><span class="sxs-lookup"><span data-stu-id="4e603-118">Requirement</span></span> | <span data-ttu-id="4e603-119">值</span><span class="sxs-lookup"><span data-stu-id="4e603-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e603-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4e603-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4e603-121"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4e603-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e603-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e603-122">Library</span></span><br/> | <dl> <span data-ttu-id="4e603-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4e603-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e603-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e603-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e603-125">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4e603-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




