---
description: Get \_ StopTime 方法會捕獲播放將停止的時間，相對於資料流程的持續時間。 這個方法會實 IMediaPosition：： get \_ StopTime 方法。
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: 'CPosPassThru.get_StopTime 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987097"
---
# <a name="cpospassthruget_stoptime-method"></a><span data-ttu-id="06e0c-104">CPosPassThru. 取得 \_ StopTime 方法</span><span class="sxs-lookup"><span data-stu-id="06e0c-104">CPosPassThru.get\_StopTime method</span></span>

<span data-ttu-id="06e0c-105">`get_StopTime`方法會抓取播放將停止的時間，相對於資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="06e0c-105">The `get_StopTime` method retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> <span data-ttu-id="06e0c-106">這個方法會實 [**IMediaPosition：： get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) 方法。</span><span class="sxs-lookup"><span data-stu-id="06e0c-106">This method implements the [**IMediaPosition::get\_StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06e0c-107">語法</span><span class="sxs-lookup"><span data-stu-id="06e0c-107">Syntax</span></span>


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="06e0c-108">參數</span><span class="sxs-lookup"><span data-stu-id="06e0c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06e0c-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="06e0c-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="06e0c-110">接收停止時間之變數的指標（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="06e0c-110">Pointer to a variable that receives the stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06e0c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="06e0c-111">Return value</span></span>

<span data-ttu-id="06e0c-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="06e0c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="06e0c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="06e0c-113">Requirements</span></span>



| <span data-ttu-id="06e0c-114">需求</span><span class="sxs-lookup"><span data-stu-id="06e0c-114">Requirement</span></span> | <span data-ttu-id="06e0c-115">值</span><span class="sxs-lookup"><span data-stu-id="06e0c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06e0c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="06e0c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="06e0c-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="06e0c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06e0c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="06e0c-118">Library</span></span><br/> | <dl> <span data-ttu-id="06e0c-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="06e0c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06e0c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06e0c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06e0c-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="06e0c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




