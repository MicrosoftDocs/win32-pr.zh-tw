---
description: 啟動方法會建立對話方塊視窗。 這個方法會實 IPropertyPage：： Activate 方法。
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: 'CBasePropertyPage 啟動方法 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989604"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="2791d-104">CBasePropertyPage。 Activate 方法</span><span class="sxs-lookup"><span data-stu-id="2791d-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="2791d-105">`Activate`方法會建立對話方塊視窗。</span><span class="sxs-lookup"><span data-stu-id="2791d-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="2791d-106">這個方法會實 **IPropertyPage：： Activate** 方法。</span><span class="sxs-lookup"><span data-stu-id="2791d-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2791d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2791d-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="2791d-108">參數</span><span class="sxs-lookup"><span data-stu-id="2791d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2791d-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="2791d-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="2791d-110">對話方塊的父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2791d-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2791d-111">*prect*</span><span class="sxs-lookup"><span data-stu-id="2791d-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="2791d-112">**矩形** 結構的指標，該結構包含對話方塊的位置資訊。</span><span class="sxs-lookup"><span data-stu-id="2791d-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="2791d-113">*fModal*</span><span class="sxs-lookup"><span data-stu-id="2791d-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="2791d-114">布林值，指出對話方塊框架是否為強制回應 (**TRUE**) 或非模式 (**FALSE**) 。</span><span class="sxs-lookup"><span data-stu-id="2791d-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2791d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2791d-115">Return value</span></span>

<span data-ttu-id="2791d-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2791d-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2791d-117">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="2791d-117">Possible values include the following.</span></span>



| <span data-ttu-id="2791d-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2791d-118">Return code</span></span>                                                                                   | <span data-ttu-id="2791d-119">Description</span><span class="sxs-lookup"><span data-stu-id="2791d-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2791d-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2791d-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2791d-121">成功。</span><span class="sxs-lookup"><span data-stu-id="2791d-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="2791d-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2791d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2791d-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2791d-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="2791d-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2791d-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2791d-125">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="2791d-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="2791d-126"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="2791d-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="2791d-127">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="2791d-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="2791d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="2791d-128">Requirements</span></span>



| <span data-ttu-id="2791d-129">需求</span><span class="sxs-lookup"><span data-stu-id="2791d-129">Requirement</span></span> | <span data-ttu-id="2791d-130">值</span><span class="sxs-lookup"><span data-stu-id="2791d-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2791d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="2791d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="2791d-132"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2791d-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2791d-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="2791d-133">Library</span></span><br/> | <dl> <span data-ttu-id="2791d-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2791d-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2791d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2791d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2791d-136">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="2791d-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="2791d-137">**CBasePropertyPage：： OnActivate**</span><span class="sxs-lookup"><span data-stu-id="2791d-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




