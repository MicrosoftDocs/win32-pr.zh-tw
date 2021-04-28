---
description: CSourceSeeking. GetRate 方法-GetRate 方法會捕獲播放速率。 這個方法會實 IMediaSeeking：： GetRate 方法。
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: 'CSourceSeeking. GetRate 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085226"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="2e7ce-104">CSourceSeeking. GetRate 方法</span><span class="sxs-lookup"><span data-stu-id="2e7ce-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="2e7ce-105">`GetRate`方法會捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="2e7ce-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="2e7ce-106">這個方法會實 [**IMediaSeeking：： GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="2e7ce-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e7ce-107">語法</span><span class="sxs-lookup"><span data-stu-id="2e7ce-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="2e7ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e7ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e7ce-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="2e7ce-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="2e7ce-110">接收播放速率之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="2e7ce-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e7ce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e7ce-111">Return value</span></span>

<span data-ttu-id="2e7ce-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2e7ce-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="2e7ce-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2e7ce-113">Return code</span></span>                                                                               | <span data-ttu-id="2e7ce-114">Description</span><span class="sxs-lookup"><span data-stu-id="2e7ce-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="2e7ce-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2e7ce-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2e7ce-116">Success</span><span class="sxs-lookup"><span data-stu-id="2e7ce-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="2e7ce-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2e7ce-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2e7ce-118">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="2e7ce-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2e7ce-119">備註</span><span class="sxs-lookup"><span data-stu-id="2e7ce-119">Remarks</span></span>

<span data-ttu-id="2e7ce-120">播放速率是由 [**CSourceSeeking：： m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) 成員變數所指定。</span><span class="sxs-lookup"><span data-stu-id="2e7ce-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e7ce-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2e7ce-121">Requirements</span></span>



| <span data-ttu-id="2e7ce-122">需求</span><span class="sxs-lookup"><span data-stu-id="2e7ce-122">Requirement</span></span> | <span data-ttu-id="2e7ce-123">值</span><span class="sxs-lookup"><span data-stu-id="2e7ce-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e7ce-124">標頭</span><span class="sxs-lookup"><span data-stu-id="2e7ce-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2e7ce-125"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2e7ce-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e7ce-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="2e7ce-126">Library</span></span><br/> | <dl> <span data-ttu-id="2e7ce-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2e7ce-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e7ce-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2e7ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e7ce-129">**CSourceSeeking 類別**</span><span class="sxs-lookup"><span data-stu-id="2e7ce-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




