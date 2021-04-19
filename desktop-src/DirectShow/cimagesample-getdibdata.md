---
description: GetDIBData 方法會抓取此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: 'CImageSample. GetDIBData 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977422"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="eb48d-103">CImageSample. GetDIBData 方法</span><span class="sxs-lookup"><span data-stu-id="eb48d-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="eb48d-104">`GetDIBData`方法會抓取此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="eb48d-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb48d-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb48d-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="eb48d-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb48d-106">Parameters</span></span>

<span data-ttu-id="eb48d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="eb48d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb48d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb48d-108">Return value</span></span>

<span data-ttu-id="eb48d-109">傳回 [**DIBDATA**](dibdata.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="eb48d-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb48d-110">備註</span><span class="sxs-lookup"><span data-stu-id="eb48d-110">Remarks</span></span>

<span data-ttu-id="eb48d-111">呼叫這個方法之前，呼叫端必須初始化 **DIBDATA** 結構。檢查 **CImageSample：： m \_ bInit** 的值。</span><span class="sxs-lookup"><span data-stu-id="eb48d-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="eb48d-112">若要初始化結構，請呼叫 [**CImageSample：： SetDIBData**](cimagesample-setdibdata.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb48d-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb48d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb48d-113">Requirements</span></span>



| <span data-ttu-id="eb48d-114">需求</span><span class="sxs-lookup"><span data-stu-id="eb48d-114">Requirement</span></span> | <span data-ttu-id="eb48d-115">值</span><span class="sxs-lookup"><span data-stu-id="eb48d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb48d-116">標頭</span><span class="sxs-lookup"><span data-stu-id="eb48d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eb48d-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eb48d-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb48d-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb48d-118">Library</span></span><br/> | <dl> <span data-ttu-id="eb48d-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eb48d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb48d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb48d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb48d-121">**CImageSample 類別**</span><span class="sxs-lookup"><span data-stu-id="eb48d-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




