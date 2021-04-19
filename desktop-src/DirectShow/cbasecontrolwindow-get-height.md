---
description: Get \_ Height 方法會抓取目前的視窗高度。
ms.assetid: 841c7d5d-f633-41fb-9cde-6126cd1cab9b
title: 'CBaseControlWindow.get_Height 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Height
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bed7beaac064ce9d97b9c93264eab8d56b27c9df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989778"
---
# <a name="cbasecontrolwindowget_height-method"></a><span data-ttu-id="42f59-103">CBaseControlWindow. 取得 \_ 高度方法</span><span class="sxs-lookup"><span data-stu-id="42f59-103">CBaseControlWindow.get\_Height method</span></span>

<span data-ttu-id="42f59-104">方法會抓取 `get_Height` 目前的視窗高度。</span><span class="sxs-lookup"><span data-stu-id="42f59-104">The `get_Height` method retrieves the current window height.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f59-105">語法</span><span class="sxs-lookup"><span data-stu-id="42f59-105">Syntax</span></span>


```C++
HRESULT get_Height(
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="42f59-106">參數</span><span class="sxs-lookup"><span data-stu-id="42f59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f59-107">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="42f59-107">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="42f59-108">目前視窗高度的指標（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="42f59-108">Pointer to the current window height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f59-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="42f59-109">Return value</span></span>

<span data-ttu-id="42f59-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="42f59-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="42f59-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="42f59-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="42f59-112">備註</span><span class="sxs-lookup"><span data-stu-id="42f59-112">Remarks</span></span>

<span data-ttu-id="42f59-113">視窗具有桌面上的位置。</span><span class="sxs-lookup"><span data-stu-id="42f59-113">The window has a position on the desktop.</span></span> <span data-ttu-id="42f59-114">這是以圖元為單位來表示， (左、上、右和下) 。</span><span class="sxs-lookup"><span data-stu-id="42f59-114">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="42f59-115">OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。</span><span class="sxs-lookup"><span data-stu-id="42f59-115">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="42f59-116">所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。</span><span class="sxs-lookup"><span data-stu-id="42f59-116">All coordinates are expressed in pixels, and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="42f59-117">設定左方或上座標會分別將視窗向左或上移動;這些座標不會影響視窗的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="42f59-117">Setting the left or top coordinates moves the window left or up, respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="42f59-118">同樣地，設定寬度和高度並不會影響左邊和上座標。</span><span class="sxs-lookup"><span data-stu-id="42f59-118">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f59-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="42f59-119">Requirements</span></span>



| <span data-ttu-id="42f59-120">需求</span><span class="sxs-lookup"><span data-stu-id="42f59-120">Requirement</span></span> | <span data-ttu-id="42f59-121">值</span><span class="sxs-lookup"><span data-stu-id="42f59-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f59-122">標頭</span><span class="sxs-lookup"><span data-stu-id="42f59-122">Header</span></span><br/>  | <dl> <span data-ttu-id="42f59-123"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="42f59-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42f59-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="42f59-124">Library</span></span><br/> | <dl> <span data-ttu-id="42f59-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="42f59-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f59-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42f59-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f59-127">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="42f59-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




