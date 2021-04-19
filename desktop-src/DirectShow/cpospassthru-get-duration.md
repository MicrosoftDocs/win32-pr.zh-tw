---
description: 取得 \_ 持續時間方法會抓取資料流程的持續時間。 這個方法會實 IMediaPosition：： get \_ Duration 方法。
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: 'CPosPassThru.get_Duration 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987944"
---
# <a name="cpospassthruget_duration-method"></a><span data-ttu-id="f6686-104">CPosPassThru. 取得 \_ Duration 方法</span><span class="sxs-lookup"><span data-stu-id="f6686-104">CPosPassThru.get\_Duration method</span></span>

<span data-ttu-id="f6686-105">`get_Duration`方法會捕獲資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="f6686-105">The `get_Duration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="f6686-106">這個方法會實 [**IMediaPosition：： get \_ Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) 方法。</span><span class="sxs-lookup"><span data-stu-id="f6686-106">This method implements the [**IMediaPosition::get\_Duration**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6686-107">語法</span><span class="sxs-lookup"><span data-stu-id="f6686-107">Syntax</span></span>


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a><span data-ttu-id="f6686-108">參數</span><span class="sxs-lookup"><span data-stu-id="f6686-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6686-109">*plength*</span><span class="sxs-lookup"><span data-stu-id="f6686-109">*plength*</span></span> 
</dt> <dd>

<span data-ttu-id="f6686-110">接收資料流程長度總計（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="f6686-110">Pointer to a variable that receives the total stream length, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6686-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6686-111">Return value</span></span>

<span data-ttu-id="f6686-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f6686-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6686-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6686-113">Requirements</span></span>



| <span data-ttu-id="f6686-114">需求</span><span class="sxs-lookup"><span data-stu-id="f6686-114">Requirement</span></span> | <span data-ttu-id="f6686-115">值</span><span class="sxs-lookup"><span data-stu-id="f6686-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6686-116">標頭</span><span class="sxs-lookup"><span data-stu-id="f6686-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f6686-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f6686-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6686-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="f6686-118">Library</span></span><br/> | <dl> <span data-ttu-id="f6686-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f6686-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6686-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6686-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6686-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="f6686-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




