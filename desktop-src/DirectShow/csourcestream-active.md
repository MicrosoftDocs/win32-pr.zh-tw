---
description: 使用中的方法會通知釘選篩選現在為使用中狀態。 這個方法會覆寫 CBasePin：： Active 方法。 如果連接的是連接的，這個方法會啟動串流執行緒。
ms.assetid: ea32b602-2583-4de6-96ec-6ea875c49d14
title: 'CSourceStream 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a161c82621f29b916e03fbc2e59ec762871940b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983069"
---
# <a name="csourcestreamactive-method"></a><span data-ttu-id="3b49e-105">CSourceStream 方法</span><span class="sxs-lookup"><span data-stu-id="3b49e-105">CSourceStream.Active method</span></span>

<span data-ttu-id="3b49e-106">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="3b49e-106">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="3b49e-107">這個方法會覆寫 [**CBasePin：： Active**](cbasepin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3b49e-107">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="3b49e-108">如果連接的是連接的，這個方法會啟動串流執行緒。</span><span class="sxs-lookup"><span data-stu-id="3b49e-108">If the pin is connected, this method starts the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b49e-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b49e-109">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="3b49e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b49e-110">Parameters</span></span>

<span data-ttu-id="3b49e-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3b49e-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3b49e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b49e-112">Return value</span></span>

<span data-ttu-id="3b49e-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3b49e-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3b49e-114">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="3b49e-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3b49e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3b49e-115">Return code</span></span>                                                                             | <span data-ttu-id="3b49e-116">Description</span><span class="sxs-lookup"><span data-stu-id="3b49e-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="3b49e-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3b49e-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3b49e-118">Pin 已在使用中。</span><span class="sxs-lookup"><span data-stu-id="3b49e-118">The pin is already active.</span></span><br/>  |
| <dl> <span data-ttu-id="3b49e-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3b49e-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3b49e-120">成功。</span><span class="sxs-lookup"><span data-stu-id="3b49e-120">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="3b49e-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3b49e-121"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="3b49e-122">無法啟動執行緒。</span><span class="sxs-lookup"><span data-stu-id="3b49e-122">Could not start the thread.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b49e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b49e-123">Requirements</span></span>



| <span data-ttu-id="3b49e-124">需求</span><span class="sxs-lookup"><span data-stu-id="3b49e-124">Requirement</span></span> | <span data-ttu-id="3b49e-125">值</span><span class="sxs-lookup"><span data-stu-id="3b49e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b49e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="3b49e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="3b49e-127"><dt>來源 .h (包含) 的資料流程 </dt></span><span class="sxs-lookup"><span data-stu-id="3b49e-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3b49e-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b49e-128">Library</span></span><br/> | <dl> <span data-ttu-id="3b49e-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3b49e-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b49e-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b49e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b49e-131">**CSourceStream 類別**</span><span class="sxs-lookup"><span data-stu-id="3b49e-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




