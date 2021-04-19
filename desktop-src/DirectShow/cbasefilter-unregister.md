---
description: 取消註冊方法會將篩選從登錄中移除。
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: 'CBaseFilter：取消註冊方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992877"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="d640f-103">CBaseFilter，取消註冊方法</span><span class="sxs-lookup"><span data-stu-id="d640f-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="d640f-104">`Unregister`方法會從登錄中移除篩選。</span><span class="sxs-lookup"><span data-stu-id="d640f-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="d640f-105">這個方法已過時。</span><span class="sxs-lookup"><span data-stu-id="d640f-105">This method is obsolete.</span></span> <span data-ttu-id="d640f-106">新的篩選器應該使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 函式來取消註冊。</span><span class="sxs-lookup"><span data-stu-id="d640f-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="d640f-107">如需詳細資訊，請參閱 [如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="d640f-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d640f-108">語法</span><span class="sxs-lookup"><span data-stu-id="d640f-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="d640f-109">參數</span><span class="sxs-lookup"><span data-stu-id="d640f-109">Parameters</span></span>

<span data-ttu-id="d640f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d640f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d640f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d640f-111">Return value</span></span>

<span data-ttu-id="d640f-112">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d640f-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d640f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d640f-113">Requirements</span></span>



| <span data-ttu-id="d640f-114">需求</span><span class="sxs-lookup"><span data-stu-id="d640f-114">Requirement</span></span> | <span data-ttu-id="d640f-115">值</span><span class="sxs-lookup"><span data-stu-id="d640f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d640f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d640f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d640f-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d640f-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d640f-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d640f-118">Library</span></span><br/> | <dl> <span data-ttu-id="d640f-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d640f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d640f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d640f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d640f-121">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="d640f-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




