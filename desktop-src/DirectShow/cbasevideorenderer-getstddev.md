---
description: GetStdDev 方法會根據每個畫面格的統計資料，來估計每個框架的到期時間和實際轉譯的標準差（以毫秒為單位）。
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: 'CBaseVideoRenderer. GetStdDev 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978649"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="851cc-103">CBaseVideoRenderer. GetStdDev 方法</span><span class="sxs-lookup"><span data-stu-id="851cc-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="851cc-104">方法會根據每個畫面格的 `GetStdDev` 統計資料，來估計每個框架的到期時間和實際轉譯的標準差（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="851cc-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="851cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="851cc-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="851cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="851cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="851cc-107">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="851cc-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="851cc-108">整數值，其中包含影片轉譯器收到的影片樣本數。</span><span class="sxs-lookup"><span data-stu-id="851cc-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="851cc-109">*piResult*</span><span class="sxs-lookup"><span data-stu-id="851cc-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="851cc-110">整數值的指標，該整數值會包含標準差。</span><span class="sxs-lookup"><span data-stu-id="851cc-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="851cc-111">*llSumSq*</span><span class="sxs-lookup"><span data-stu-id="851cc-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="851cc-112">值，表示所有轉譯的影片樣本的標準差（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="851cc-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="851cc-113">值越低，呈現的一致性就越一致。</span><span class="sxs-lookup"><span data-stu-id="851cc-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="851cc-114">*iTot*</span><span class="sxs-lookup"><span data-stu-id="851cc-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="851cc-115">值，表示所有轉譯的影片樣本的戳記時間和轉譯時間之間的平均值（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="851cc-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="851cc-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="851cc-116">Return value</span></span>

<span data-ttu-id="851cc-117">傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR。</span><span class="sxs-lookup"><span data-stu-id="851cc-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="851cc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="851cc-118">Requirements</span></span>



| <span data-ttu-id="851cc-119">需求</span><span class="sxs-lookup"><span data-stu-id="851cc-119">Requirement</span></span> | <span data-ttu-id="851cc-120">值</span><span class="sxs-lookup"><span data-stu-id="851cc-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="851cc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="851cc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="851cc-122"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="851cc-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="851cc-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="851cc-123">Library</span></span><br/> | <dl> <span data-ttu-id="851cc-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="851cc-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="851cc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="851cc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="851cc-126">**CBaseVideoRenderer 類別**</span><span class="sxs-lookup"><span data-stu-id="851cc-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




