---
description: CBaseDispatch. GetTypeInfoCount 方法-GetTypeInfoCount 方法會抓取物件提供的類型資訊介面數目。
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: 'CBaseDispatch. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099886"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="42a8b-103">CBaseDispatch. GetTypeInfoCount 方法</span><span class="sxs-lookup"><span data-stu-id="42a8b-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="42a8b-104">方法會抓取 `GetTypeInfoCount` 物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="42a8b-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="42a8b-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="42a8b-106">參數</span><span class="sxs-lookup"><span data-stu-id="42a8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a8b-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="42a8b-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="42a8b-108">變數的指標，此變數會接收物件提供的類型資訊介面數目。</span><span class="sxs-lookup"><span data-stu-id="42a8b-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="42a8b-109">當方法傳回時，值為1。</span><span class="sxs-lookup"><span data-stu-id="42a8b-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a8b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="42a8b-110">Return value</span></span>

<span data-ttu-id="42a8b-111">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42a8b-111">Returns one of the following values.</span></span>



| <span data-ttu-id="42a8b-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42a8b-112">Return code</span></span>                                                                               | <span data-ttu-id="42a8b-113">Description</span><span class="sxs-lookup"><span data-stu-id="42a8b-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="42a8b-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42a8b-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="42a8b-115">成功。</span><span class="sxs-lookup"><span data-stu-id="42a8b-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="42a8b-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="42a8b-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="42a8b-117">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="42a8b-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42a8b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="42a8b-118">Requirements</span></span>



| <span data-ttu-id="42a8b-119">需求</span><span class="sxs-lookup"><span data-stu-id="42a8b-119">Requirement</span></span> | <span data-ttu-id="42a8b-120">值</span><span class="sxs-lookup"><span data-stu-id="42a8b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a8b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="42a8b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="42a8b-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="42a8b-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42a8b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="42a8b-123">Library</span></span><br/> | <dl> <span data-ttu-id="42a8b-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="42a8b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a8b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42a8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a8b-126">**CBaseDispatch 類別**</span><span class="sxs-lookup"><span data-stu-id="42a8b-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




