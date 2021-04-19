---
description: SetPalette 方法會安裝視窗的調色板。
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: 'CBaseWindow. SetPalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994210"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a><span data-ttu-id="db8c8-103">CBaseWindow. SetPalette 方法 (Winutil .h) </span><span class="sxs-lookup"><span data-stu-id="db8c8-103">CBaseWindow.SetPalette method (Winutil.h)</span></span>

<span data-ttu-id="db8c8-104">`SetPalette`方法會安裝視窗的調色板。</span><span class="sxs-lookup"><span data-stu-id="db8c8-104">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="db8c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="db8c8-105">Syntax</span></span>


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a><span data-ttu-id="db8c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="db8c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db8c8-107">*hPalette*</span><span class="sxs-lookup"><span data-stu-id="db8c8-107">*hPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="db8c8-108">新調色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="db8c8-108">Handle to the new palette.</span></span> <span data-ttu-id="db8c8-109">不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="db8c8-109">Cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db8c8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="db8c8-110">Return value</span></span>

<span data-ttu-id="db8c8-111">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="db8c8-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="db8c8-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db8c8-112">Return code</span></span>                                                                             | <span data-ttu-id="db8c8-113">Description</span><span class="sxs-lookup"><span data-stu-id="db8c8-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="db8c8-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="db8c8-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="db8c8-115">**GdiFlush** 的內部呼叫傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="db8c8-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="db8c8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="db8c8-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="db8c8-117">成功。</span><span class="sxs-lookup"><span data-stu-id="db8c8-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="db8c8-118">備註</span><span class="sxs-lookup"><span data-stu-id="db8c8-118">Remarks</span></span>

<span data-ttu-id="db8c8-119">如果 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數的值為 **FALSE** (預設) ，這個方法會選取並意識到這個調色板。</span><span class="sxs-lookup"><span data-stu-id="db8c8-119">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="db8c8-120">否則，它會選取元件，但不會察覺到。</span><span class="sxs-lookup"><span data-stu-id="db8c8-120">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="db8c8-121">物件不會刪除任何先前使用的調色板。</span><span class="sxs-lookup"><span data-stu-id="db8c8-121">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="db8c8-122">呼叫端負責刪除調色板。</span><span class="sxs-lookup"><span data-stu-id="db8c8-122">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="db8c8-123">任何執行緒都可以安全地呼叫這個方法，而不只是擁有視窗的執行緒。</span><span class="sxs-lookup"><span data-stu-id="db8c8-123">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="db8c8-124">視窗會將私用訊息傳送至本身，以觸發對 [**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="db8c8-124">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db8c8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="db8c8-125">Requirements</span></span>



| <span data-ttu-id="db8c8-126">需求</span><span class="sxs-lookup"><span data-stu-id="db8c8-126">Requirement</span></span> | <span data-ttu-id="db8c8-127">值</span><span class="sxs-lookup"><span data-stu-id="db8c8-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db8c8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="db8c8-128">Header</span></span><br/>  | <dl> <span data-ttu-id="db8c8-129"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="db8c8-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db8c8-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="db8c8-130">Library</span></span><br/> | <dl> <span data-ttu-id="db8c8-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="db8c8-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db8c8-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db8c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db8c8-133">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="db8c8-133">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




