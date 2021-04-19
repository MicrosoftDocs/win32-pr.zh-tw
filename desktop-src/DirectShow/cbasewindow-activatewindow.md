---
description: ActivateWindow 方法會根據衍生類別的需求來調整視窗的大小。
ms.assetid: 39e23080-e4ae-46d5-bb3f-306c92bbfe14
title: 'CBaseWindow. ActivateWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.ActivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f747f108bb6c7e42e90a0ff8503ec59a83c59699
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000461"
---
# <a name="cbasewindowactivatewindow-method"></a><span data-ttu-id="c3ef7-103">CBaseWindow. ActivateWindow 方法</span><span class="sxs-lookup"><span data-stu-id="c3ef7-103">CBaseWindow.ActivateWindow method</span></span>

<span data-ttu-id="c3ef7-104">`ActivateWindow`方法會根據衍生類別的需求來調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-104">The `ActivateWindow` method sizes the window according to the requirements of the derived class.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ef7-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3ef7-105">Syntax</span></span>


```C++
virtual HRESULT ActivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="c3ef7-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3ef7-106">Parameters</span></span>

<span data-ttu-id="c3ef7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3ef7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3ef7-108">Return value</span></span>

<span data-ttu-id="c3ef7-109">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c3ef7-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c3ef7-110">Return code</span></span>                                                                             | <span data-ttu-id="c3ef7-111">Description</span><span class="sxs-lookup"><span data-stu-id="c3ef7-111">Description</span></span>                              |
|-----------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="c3ef7-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ef7-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c3ef7-113">視窗已經啟用。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-113">Window was already activated.</span></span><br/> |
| <dl> <span data-ttu-id="c3ef7-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ef7-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c3ef7-115">成功。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-115">Success.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="c3ef7-116">備註</span><span class="sxs-lookup"><span data-stu-id="c3ef7-116">Remarks</span></span>

<span data-ttu-id="c3ef7-117">這個方法會呼叫 [**CBaseWindow：： GetDefaultRect**](cbasewindow-getdefaultrect.md) 方法來判斷視窗大小。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-117">This methods calls the [**CBaseWindow::GetDefaultRect**](cbasewindow-getdefaultrect.md) method to determine the window size.</span></span> <span data-ttu-id="c3ef7-118">衍生類別應該覆寫 **GetDefaultRect** ，以傳回將顯示之影像的大小。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-118">The derived class should override **GetDefaultRect** to return the size of the images that will be displayed.</span></span>

<span data-ttu-id="c3ef7-119">如果視窗已在使用中，則呼叫 `ActivateWindow` 會將視窗移至 Z 順序的頂端，但不會調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-119">If the window is already active, calling `ActivateWindow` moves the window to the top of the Z order, but does not resize the window.</span></span> <span data-ttu-id="c3ef7-120">如果視窗有父代，也是如此。</span><span class="sxs-lookup"><span data-stu-id="c3ef7-120">The same is true if the window has a parent.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ef7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3ef7-121">Requirements</span></span>



| <span data-ttu-id="c3ef7-122">需求</span><span class="sxs-lookup"><span data-stu-id="c3ef7-122">Requirement</span></span> | <span data-ttu-id="c3ef7-123">值</span><span class="sxs-lookup"><span data-stu-id="c3ef7-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ef7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c3ef7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c3ef7-125"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c3ef7-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3ef7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3ef7-126">Library</span></span><br/> | <dl> <span data-ttu-id="c3ef7-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c3ef7-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ef7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3ef7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ef7-129">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="c3ef7-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




