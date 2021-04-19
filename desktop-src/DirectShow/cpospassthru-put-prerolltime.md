---
description: Put \_ PrerollTime 方法會設定要在開始位置之前排入佇列的資料量。 這個方法會實 IMediaPosition：:p 的 \_ PrerollTime 方法。
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: 'CPosPassThru.put_PrerollTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993412"
---
# <a name="cpospassthruput_prerolltime-method"></a><span data-ttu-id="b3e43-104">CPosPassThru. put \_ PrerollTime 方法</span><span class="sxs-lookup"><span data-stu-id="b3e43-104">CPosPassThru.put\_PrerollTime method</span></span>

<span data-ttu-id="b3e43-105">`put_PrerollTime`方法會設定要在開始位置之前排入佇列的資料量。</span><span class="sxs-lookup"><span data-stu-id="b3e43-105">The `put_PrerollTime` method sets the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="b3e43-106">這個方法會實 [**IMediaPosition：:p 的 \_ PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) 方法。</span><span class="sxs-lookup"><span data-stu-id="b3e43-106">This method implements the [**IMediaPosition::put\_PrerollTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e43-107">語法</span><span class="sxs-lookup"><span data-stu-id="b3e43-107">Syntax</span></span>


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="b3e43-108">參數</span><span class="sxs-lookup"><span data-stu-id="b3e43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e43-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="b3e43-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e43-110">預先計算的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b3e43-110">Preroll time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e43-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3e43-111">Return value</span></span>

<span data-ttu-id="b3e43-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b3e43-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3e43-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3e43-113">Requirements</span></span>



| <span data-ttu-id="b3e43-114">需求</span><span class="sxs-lookup"><span data-stu-id="b3e43-114">Requirement</span></span> | <span data-ttu-id="b3e43-115">值</span><span class="sxs-lookup"><span data-stu-id="b3e43-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e43-116">標頭</span><span class="sxs-lookup"><span data-stu-id="b3e43-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b3e43-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b3e43-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b3e43-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="b3e43-118">Library</span></span><br/> | <dl> <span data-ttu-id="b3e43-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b3e43-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3e43-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3e43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e43-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="b3e43-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




