---
description: IsPageDirty 方法會指出屬性頁面在啟動後，或自最近一次呼叫 IPropertyPage：： Apply 之後是否已變更。 這個方法會實 IPropertyPage：： IsPageDirty 方法。
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: 'CBasePropertyPage. IsPageDirty 方法 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990732"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="d12a6-104">CBasePropertyPage. IsPageDirty 方法</span><span class="sxs-lookup"><span data-stu-id="d12a6-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="d12a6-105">`IsPageDirty`方法會指出屬性頁面在啟動後，或自最近一次呼叫 **IPropertyPage：： Apply** 之後是否已變更。</span><span class="sxs-lookup"><span data-stu-id="d12a6-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="d12a6-106">這個方法會實 **IPropertyPage：： IsPageDirty** 方法。</span><span class="sxs-lookup"><span data-stu-id="d12a6-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d12a6-107">語法</span><span class="sxs-lookup"><span data-stu-id="d12a6-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="d12a6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d12a6-108">Parameters</span></span>

<span data-ttu-id="d12a6-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d12a6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d12a6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d12a6-110">Return value</span></span>

<span data-ttu-id="d12a6-111">\_如果 [**CBasePropertyPage：： m \_ bDirty**](cbasepropertypage-m-bdirty.md)為 **TRUE**，則傳回 s OK， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="d12a6-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d12a6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d12a6-112">Requirements</span></span>



| <span data-ttu-id="d12a6-113">需求</span><span class="sxs-lookup"><span data-stu-id="d12a6-113">Requirement</span></span> | <span data-ttu-id="d12a6-114">值</span><span class="sxs-lookup"><span data-stu-id="d12a6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d12a6-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d12a6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d12a6-116"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d12a6-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d12a6-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="d12a6-117">Library</span></span><br/> | <dl> <span data-ttu-id="d12a6-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d12a6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d12a6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d12a6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12a6-120">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="d12a6-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




