---
description: DisplayTypeInfo 方法會在調試過程中顯示媒體類型資訊。
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: 'CBasePin. DisplayTypeInfo 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977777"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="43365-103">CBasePin. DisplayTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="43365-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="43365-104">`DisplayTypeInfo`方法會在調試過程中顯示媒體類型資訊。</span><span class="sxs-lookup"><span data-stu-id="43365-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="43365-105">語法</span><span class="sxs-lookup"><span data-stu-id="43365-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="43365-106">參數</span><span class="sxs-lookup"><span data-stu-id="43365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43365-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="43365-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="43365-108">忽略。</span><span class="sxs-lookup"><span data-stu-id="43365-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="43365-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="43365-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="43365-110">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="43365-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43365-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="43365-111">Return value</span></span>

<span data-ttu-id="43365-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="43365-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43365-113">備註</span><span class="sxs-lookup"><span data-stu-id="43365-113">Remarks</span></span>

<span data-ttu-id="43365-114">在 debug 組建中，這個方法會呼叫 [**DbgLog**](dbglog.md) 函數來顯示指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="43365-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="43365-115">在零售組建中，此方法不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="43365-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="43365-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="43365-116">Requirements</span></span>



| <span data-ttu-id="43365-117">需求</span><span class="sxs-lookup"><span data-stu-id="43365-117">Requirement</span></span> | <span data-ttu-id="43365-118">值</span><span class="sxs-lookup"><span data-stu-id="43365-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43365-119">標頭</span><span class="sxs-lookup"><span data-stu-id="43365-119">Header</span></span><br/>  | <dl> <span data-ttu-id="43365-120"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="43365-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43365-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="43365-121">Library</span></span><br/> | <dl> <span data-ttu-id="43365-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="43365-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43365-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43365-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43365-124">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="43365-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




