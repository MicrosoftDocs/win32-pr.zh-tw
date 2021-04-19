---
description: CheckStreaming 方法會判斷 pin 是否可以接受範例。
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: 'CTransformInputPin. CheckStreaming 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989631"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="5e17d-103">CTransformInputPin. CheckStreaming 方法</span><span class="sxs-lookup"><span data-stu-id="5e17d-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="5e17d-104">`CheckStreaming`方法會判斷 pin 是否可以接受範例。</span><span class="sxs-lookup"><span data-stu-id="5e17d-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e17d-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e17d-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="5e17d-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e17d-106">Parameters</span></span>

<span data-ttu-id="5e17d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5e17d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e17d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e17d-108">Return value</span></span>

<span data-ttu-id="5e17d-109">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5e17d-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="5e17d-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5e17d-110">Return code</span></span>                                                                                           | <span data-ttu-id="5e17d-111">Description</span><span class="sxs-lookup"><span data-stu-id="5e17d-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="5e17d-112"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5e17d-113">成功。</span><span class="sxs-lookup"><span data-stu-id="5e17d-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="5e17d-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="5e17d-115">Pin 目前正在排清。</span><span class="sxs-lookup"><span data-stu-id="5e17d-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="5e17d-116"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5e17d-117">輸出針腳未連接。</span><span class="sxs-lookup"><span data-stu-id="5e17d-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5e17d-118"><dt>**VFW \_ E \_ 運行時 \_ 錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="5e17d-119">發生執行階段錯誤。</span><span class="sxs-lookup"><span data-stu-id="5e17d-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="5e17d-120"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="5e17d-121">已停止 pin。</span><span class="sxs-lookup"><span data-stu-id="5e17d-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="5e17d-122">備註</span><span class="sxs-lookup"><span data-stu-id="5e17d-122">Remarks</span></span>

<span data-ttu-id="5e17d-123">這個方法會覆寫 [**CBaseInputPin：： CheckStreaming**](cbaseinputpin-checkstreaming.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5e17d-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e17d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e17d-124">Requirements</span></span>



| <span data-ttu-id="5e17d-125">需求</span><span class="sxs-lookup"><span data-stu-id="5e17d-125">Requirement</span></span> | <span data-ttu-id="5e17d-126">值</span><span class="sxs-lookup"><span data-stu-id="5e17d-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e17d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5e17d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5e17d-128"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5e17d-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e17d-129">Library</span></span><br/> | <dl> <span data-ttu-id="5e17d-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5e17d-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




