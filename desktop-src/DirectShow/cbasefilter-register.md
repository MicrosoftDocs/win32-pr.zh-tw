---
description: Register 方法會將篩選準則新增至登錄。
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: 'CBaseFilter： Register 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993223"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="12e96-103">CBaseFilter 註冊方法</span><span class="sxs-lookup"><span data-stu-id="12e96-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="12e96-104">`Register`方法會將篩選準則新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="12e96-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="12e96-105">這個方法已過時。</span><span class="sxs-lookup"><span data-stu-id="12e96-105">This method is obsolete.</span></span> <span data-ttu-id="12e96-106">您應使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 函式來註冊新的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="12e96-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="12e96-107">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="12e96-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="12e96-108">語法</span><span class="sxs-lookup"><span data-stu-id="12e96-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="12e96-109">參數</span><span class="sxs-lookup"><span data-stu-id="12e96-109">Parameters</span></span>

<span data-ttu-id="12e96-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="12e96-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="12e96-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="12e96-111">Return value</span></span>

<span data-ttu-id="12e96-112">傳回下表所列的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="12e96-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="12e96-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="12e96-113">Return code</span></span>                                                                             | <span data-ttu-id="12e96-114">Description</span><span class="sxs-lookup"><span data-stu-id="12e96-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="12e96-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="12e96-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="12e96-116">成功。</span><span class="sxs-lookup"><span data-stu-id="12e96-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="12e96-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="12e96-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="12e96-118">沒有任何註冊資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="12e96-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="12e96-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e96-119">Requirements</span></span>



| <span data-ttu-id="12e96-120">需求</span><span class="sxs-lookup"><span data-stu-id="12e96-120">Requirement</span></span> | <span data-ttu-id="12e96-121">值</span><span class="sxs-lookup"><span data-stu-id="12e96-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e96-122">標頭</span><span class="sxs-lookup"><span data-stu-id="12e96-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12e96-123"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12e96-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12e96-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="12e96-124">Library</span></span><br/> | <dl> <span data-ttu-id="12e96-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12e96-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e96-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e96-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e96-127">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="12e96-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




