---
description: Put \_ width 方法會設定視窗寬度。
ms.assetid: eb5ad1c2-ba39-4c06-84d2-6708dc8796d8
title: 'CBaseControlWindow.put_Width 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Width
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5235e2b842b26f3f05c31c9f19a16c7630c80c13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995507"
---
# <a name="cbasecontrolwindowput_width-method"></a><span data-ttu-id="cf8a0-103">CBaseControlWindow。 put \_ Width 方法</span><span class="sxs-lookup"><span data-stu-id="cf8a0-103">CBaseControlWindow.put\_Width method</span></span>

<span data-ttu-id="cf8a0-104">`put_Width`方法會設定視窗寬度。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-104">The `put_Width` method sets the window width.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf8a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="cf8a0-105">Syntax</span></span>


```C++
HRESULT put_Width(
   long Width
);
```



## <a name="parameters"></a><span data-ttu-id="cf8a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="cf8a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf8a0-107">*寬度*</span><span class="sxs-lookup"><span data-stu-id="cf8a0-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="cf8a0-108">新視窗寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-108">New window width, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf8a0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf8a0-109">Return value</span></span>

<span data-ttu-id="cf8a0-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf8a0-111">備註</span><span class="sxs-lookup"><span data-stu-id="cf8a0-111">Remarks</span></span>

<span data-ttu-id="cf8a0-112">視窗具有桌面上的位置。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-112">The window has a position on the desktop.</span></span> <span data-ttu-id="cf8a0-113">這是以圖元為單位來表示， (左、上、右和下) 。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-113">This is expressed in pixels by four coordinates (left, top, right, and bottom).</span></span> <span data-ttu-id="cf8a0-114">OLE 自動化的介面通常會以左、上、寬度和高度表示此位置;這是用於 DirectShow 的慣例。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-114">Interfaces that are automated by OLE typically express this position through left, top, width, and height; this is the convention used in DirectShow.</span></span> <span data-ttu-id="cf8a0-115">所有座標都會以圖元表示，而變更任何座標都會立即更新視窗。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-115">All coordinates are expressed in pixels and changing any coordinate will update the window immediately.</span></span>

<span data-ttu-id="cf8a0-116">設定左方或上座標會將視窗分別向上或向下移動;這些座標不會影響視窗的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-116">Setting the left or top coordinates moves the window left or up respectively; these coordinates have no effect on the width and height of the window.</span></span> <span data-ttu-id="cf8a0-117">同樣地，設定寬度和高度並不會影響左邊和上座標。</span><span class="sxs-lookup"><span data-stu-id="cf8a0-117">Likewise, setting the width and height does not affect the left and top coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf8a0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf8a0-118">Requirements</span></span>



| <span data-ttu-id="cf8a0-119">需求</span><span class="sxs-lookup"><span data-stu-id="cf8a0-119">Requirement</span></span> | <span data-ttu-id="cf8a0-120">值</span><span class="sxs-lookup"><span data-stu-id="cf8a0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf8a0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cf8a0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cf8a0-122"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a0-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cf8a0-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf8a0-123">Library</span></span><br/> | <dl> <span data-ttu-id="cf8a0-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cf8a0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf8a0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf8a0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf8a0-126">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="cf8a0-126">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




