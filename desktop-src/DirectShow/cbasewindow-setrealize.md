---
description: SetRealize 方法會指定視窗是否會發現調色板。
ms.assetid: ab4a6069-c11f-4126-93bf-6de5277970a1
title: 'CBaseWindow. SetRealize 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetRealize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 587e54cdbbbf57ddb4cf52e2d5dfb916acaee22d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991243"
---
# <a name="cbasewindowsetrealize-method"></a><span data-ttu-id="728b1-103">CBaseWindow. SetRealize 方法</span><span class="sxs-lookup"><span data-stu-id="728b1-103">CBaseWindow.SetRealize method</span></span>

<span data-ttu-id="728b1-104">`SetRealize`方法會指定視窗是否會發現調色板。</span><span class="sxs-lookup"><span data-stu-id="728b1-104">The `SetRealize` method specifies whether the window realizes palettes.</span></span>

## <a name="syntax"></a><span data-ttu-id="728b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="728b1-105">Syntax</span></span>


```C++
void SetRealize(
   BOOL bRealize
);
```



## <a name="parameters"></a><span data-ttu-id="728b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="728b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="728b1-107">*bRealize*</span><span class="sxs-lookup"><span data-stu-id="728b1-107">*bRealize*</span></span> 
</dt> <dd>

<span data-ttu-id="728b1-108">指定是否要實現調色板的布林值。</span><span class="sxs-lookup"><span data-stu-id="728b1-108">Boolean value that specifies whether to realize palettes.</span></span> <span data-ttu-id="728b1-109">若 **為 TRUE**， [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 方法會發現調色板。</span><span class="sxs-lookup"><span data-stu-id="728b1-109">If **TRUE**, the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method realizes palettes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="728b1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="728b1-110">Return value</span></span>

<span data-ttu-id="728b1-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="728b1-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="728b1-112">備註</span><span class="sxs-lookup"><span data-stu-id="728b1-112">Remarks</span></span>

<span data-ttu-id="728b1-113">根據預設， **SetPalette** 方法會發現指定的調色板。</span><span class="sxs-lookup"><span data-stu-id="728b1-113">By default, the **SetPalette** method realizes the specified palette.</span></span> <span data-ttu-id="728b1-114">呼叫這個方法來變更預設行為，以選取但不能實現調色板。</span><span class="sxs-lookup"><span data-stu-id="728b1-114">Call this method to change the default behavior, so that palettes are selected but not realized.</span></span> <span data-ttu-id="728b1-115">這個方法會設定 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="728b1-115">This method sets the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="728b1-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="728b1-116">Requirements</span></span>



| <span data-ttu-id="728b1-117">需求</span><span class="sxs-lookup"><span data-stu-id="728b1-117">Requirement</span></span> | <span data-ttu-id="728b1-118">值</span><span class="sxs-lookup"><span data-stu-id="728b1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="728b1-119">標頭</span><span class="sxs-lookup"><span data-stu-id="728b1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="728b1-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="728b1-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="728b1-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="728b1-121">Library</span></span><br/> | <dl> <span data-ttu-id="728b1-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="728b1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="728b1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="728b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="728b1-124">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="728b1-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




