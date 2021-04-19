---
description: 取得 \_ 速率方法會抓取播放速率。 這個方法會實 IMediaPosition：： get \_ 速率方法。
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: 'CPosPassThru.get_Rate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998808"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="285cf-104">CPosPassThru. 取得 \_ 率方法</span><span class="sxs-lookup"><span data-stu-id="285cf-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="285cf-105">`get_Rate`方法會捕獲播放速率。</span><span class="sxs-lookup"><span data-stu-id="285cf-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="285cf-106">這個方法會實 [**IMediaPosition：： get \_ 速率**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) 方法。</span><span class="sxs-lookup"><span data-stu-id="285cf-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="285cf-107">語法</span><span class="sxs-lookup"><span data-stu-id="285cf-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="285cf-108">參數</span><span class="sxs-lookup"><span data-stu-id="285cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285cf-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="285cf-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="285cf-110">接收播放速率之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="285cf-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285cf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="285cf-111">Return value</span></span>

<span data-ttu-id="285cf-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="285cf-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="285cf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="285cf-113">Requirements</span></span>



| <span data-ttu-id="285cf-114">需求</span><span class="sxs-lookup"><span data-stu-id="285cf-114">Requirement</span></span> | <span data-ttu-id="285cf-115">值</span><span class="sxs-lookup"><span data-stu-id="285cf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="285cf-116">標頭</span><span class="sxs-lookup"><span data-stu-id="285cf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="285cf-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="285cf-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="285cf-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="285cf-118">Library</span></span><br/> | <dl> <span data-ttu-id="285cf-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="285cf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285cf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="285cf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285cf-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="285cf-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




