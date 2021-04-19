---
description: 停用方法會終結對話方塊視窗。 這個方法會實 IPropertyPage：:D eactivate 方法。
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: CBasePropertyPage) 停用方法 (Cprop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985572"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="b1a43-104">CBasePropertyPage. Deactivate 方法</span><span class="sxs-lookup"><span data-stu-id="b1a43-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="b1a43-105">方法會終結 `Deactivate` 對話方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="b1a43-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="b1a43-106">這個方法會實 **IPropertyPage：:D eactivate** 方法。</span><span class="sxs-lookup"><span data-stu-id="b1a43-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a43-107">語法</span><span class="sxs-lookup"><span data-stu-id="b1a43-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="b1a43-108">參數</span><span class="sxs-lookup"><span data-stu-id="b1a43-108">Parameters</span></span>

<span data-ttu-id="b1a43-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b1a43-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1a43-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1a43-110">Return value</span></span>

<span data-ttu-id="b1a43-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b1a43-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b1a43-112">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="b1a43-112">Possible values include the following.</span></span>



| <span data-ttu-id="b1a43-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b1a43-113">Return code</span></span>                                                                                  | <span data-ttu-id="b1a43-114">Description</span><span class="sxs-lookup"><span data-stu-id="b1a43-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="b1a43-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a43-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b1a43-116">成功。</span><span class="sxs-lookup"><span data-stu-id="b1a43-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="b1a43-117"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="b1a43-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="b1a43-118">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="b1a43-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b1a43-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a43-119">Requirements</span></span>



| <span data-ttu-id="b1a43-120">需求</span><span class="sxs-lookup"><span data-stu-id="b1a43-120">Requirement</span></span> | <span data-ttu-id="b1a43-121">值</span><span class="sxs-lookup"><span data-stu-id="b1a43-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a43-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b1a43-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b1a43-123"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b1a43-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b1a43-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1a43-124">Library</span></span><br/> | <dl> <span data-ttu-id="b1a43-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b1a43-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a43-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1a43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a43-127">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="b1a43-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="b1a43-128">**CBasePropertyPage::OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="b1a43-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




