---
description: GetCapabilities 方法會抓取資料流程的所有搜尋功能。 這個方法會實 IMediaSeeking：： GetCapabilities 方法。
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: 'CSourceSeeking. GetCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993514"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="67de3-104">CSourceSeeking. GetCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="67de3-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="67de3-105">方法會抓取 `GetCapabilities` 資料流程的所有搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="67de3-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="67de3-106">這個方法會實 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="67de3-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67de3-107">語法</span><span class="sxs-lookup"><span data-stu-id="67de3-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="67de3-108">參數</span><span class="sxs-lookup"><span data-stu-id="67de3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67de3-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="67de3-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="67de3-110">變數的指標，此變數會接收搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 旗標之 AM 的位元組合。</span><span class="sxs-lookup"><span data-stu-id="67de3-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67de3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="67de3-111">Return value</span></span>

<span data-ttu-id="67de3-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="67de3-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="67de3-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="67de3-113">Return code</span></span>                                                                               | <span data-ttu-id="67de3-114">Description</span><span class="sxs-lookup"><span data-stu-id="67de3-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="67de3-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="67de3-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="67de3-116">Success</span><span class="sxs-lookup"><span data-stu-id="67de3-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="67de3-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="67de3-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="67de3-118">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="67de3-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67de3-119">備註</span><span class="sxs-lookup"><span data-stu-id="67de3-119">Remarks</span></span>

<span data-ttu-id="67de3-120">搜尋功能是由 [**CSourceSeeking：： m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) 成員變數所指定。</span><span class="sxs-lookup"><span data-stu-id="67de3-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="67de3-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="67de3-121">Requirements</span></span>



| <span data-ttu-id="67de3-122">需求</span><span class="sxs-lookup"><span data-stu-id="67de3-122">Requirement</span></span> | <span data-ttu-id="67de3-123">值</span><span class="sxs-lookup"><span data-stu-id="67de3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67de3-124">標頭</span><span class="sxs-lookup"><span data-stu-id="67de3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="67de3-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="67de3-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67de3-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="67de3-126">Library</span></span><br/> | <dl> <span data-ttu-id="67de3-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="67de3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67de3-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67de3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67de3-129">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="67de3-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




