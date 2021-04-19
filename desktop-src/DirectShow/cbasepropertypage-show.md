---
description: Show 方法會顯示或隱藏對話方塊。 這個方法會實 IPropertyPage：： Show 方法。
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: 'CBasePropertyPage： Show 方法 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990298"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="71a41-104">CBasePropertyPage 方法</span><span class="sxs-lookup"><span data-stu-id="71a41-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="71a41-105">`Show`方法會顯示或隱藏對話方塊。</span><span class="sxs-lookup"><span data-stu-id="71a41-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="71a41-106">這個方法會實 [IPropertyPage：： Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) 方法。</span><span class="sxs-lookup"><span data-stu-id="71a41-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a41-107">語法</span><span class="sxs-lookup"><span data-stu-id="71a41-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="71a41-108">參數</span><span class="sxs-lookup"><span data-stu-id="71a41-108">Parameters</span></span>

<span data-ttu-id="71a41-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="71a41-109">*nCmdShow*</span></span>

<span data-ttu-id="71a41-110">類型： **[UINT](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a41-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a41-111">指定是否要顯示或隱藏視窗的值。</span><span class="sxs-lookup"><span data-stu-id="71a41-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="71a41-112">如需詳細資訊，請參閱 [IPropertyPage：： Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) 方法。</span><span class="sxs-lookup"><span data-stu-id="71a41-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="71a41-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="71a41-113">Return value</span></span>

<span data-ttu-id="71a41-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="71a41-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71a41-115">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="71a41-115">Possible values include the following.</span></span>

| <span data-ttu-id="71a41-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="71a41-116">Return code</span></span>                                                                                  | <span data-ttu-id="71a41-117">Description</span><span class="sxs-lookup"><span data-stu-id="71a41-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="71a41-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="71a41-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="71a41-119">成功。</span><span class="sxs-lookup"><span data-stu-id="71a41-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="71a41-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="71a41-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="71a41-121">無效引數。</span><span class="sxs-lookup"><span data-stu-id="71a41-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="71a41-122"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="71a41-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="71a41-123">發生非預期的失敗。</span><span class="sxs-lookup"><span data-stu-id="71a41-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="71a41-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="71a41-124">Requirements</span></span>

| <span data-ttu-id="71a41-125">需求</span><span class="sxs-lookup"><span data-stu-id="71a41-125">Requirement</span></span> | <span data-ttu-id="71a41-126">值</span><span class="sxs-lookup"><span data-stu-id="71a41-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a41-127">標頭</span><span class="sxs-lookup"><span data-stu-id="71a41-127">Header</span></span>  | <dl> <span data-ttu-id="71a41-128"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="71a41-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="71a41-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="71a41-129">Library</span></span> | <dl> <span data-ttu-id="71a41-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="71a41-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="71a41-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71a41-131">See also</span></span>

[<span data-ttu-id="71a41-132">CBasePropertyPage 類別</span><span class="sxs-lookup"><span data-stu-id="71a41-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
