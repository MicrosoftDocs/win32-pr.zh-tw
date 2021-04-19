---
description: GetFreeCount 方法會抓取未使用的媒體樣本數目。
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: 'CBaseAllocator. GetFreeCount 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993533"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="bdcb5-103">CBaseAllocator. GetFreeCount 方法</span><span class="sxs-lookup"><span data-stu-id="bdcb5-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="bdcb5-104">`GetFreeCount`方法會抓取未使用的媒體樣本數目。</span><span class="sxs-lookup"><span data-stu-id="bdcb5-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdcb5-105">語法</span><span class="sxs-lookup"><span data-stu-id="bdcb5-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="bdcb5-106">參數</span><span class="sxs-lookup"><span data-stu-id="bdcb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdcb5-107">*plBuffersFree*</span><span class="sxs-lookup"><span data-stu-id="bdcb5-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="bdcb5-108">接收未使用的樣本數目之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="bdcb5-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdcb5-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdcb5-109">Return value</span></span>

<span data-ttu-id="bdcb5-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bdcb5-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdcb5-111">備註</span><span class="sxs-lookup"><span data-stu-id="bdcb5-111">Remarks</span></span>

<span data-ttu-id="bdcb5-112">這個方法會實 [**IMemAllocatorCallbackTemp：： GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) 方法。</span><span class="sxs-lookup"><span data-stu-id="bdcb5-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="bdcb5-113">配置器不會公開 IMemAllocatorCallbackTemp 介面，除非 CBaseAllocator 函式中的 *fEnableReleaseCallback* 旗標設為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="bdcb5-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdcb5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdcb5-114">Requirements</span></span>



| <span data-ttu-id="bdcb5-115">需求</span><span class="sxs-lookup"><span data-stu-id="bdcb5-115">Requirement</span></span> | <span data-ttu-id="bdcb5-116">值</span><span class="sxs-lookup"><span data-stu-id="bdcb5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcb5-117">標頭</span><span class="sxs-lookup"><span data-stu-id="bdcb5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bdcb5-118"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bdcb5-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bdcb5-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="bdcb5-119">Library</span></span><br/> | <dl> <span data-ttu-id="bdcb5-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bdcb5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdcb5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdcb5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcb5-122">**CBaseAllocator 類別**</span><span class="sxs-lookup"><span data-stu-id="bdcb5-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




