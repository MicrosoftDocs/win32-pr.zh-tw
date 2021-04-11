---
description: SetPalette 方法會安裝視窗的調色板。 這個方法沒有任何參數。
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: CBaseWindow. SetPalette 方法 (Winutil .h) -沒有參數
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
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104196474"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a><span data-ttu-id="3a68d-104">CBaseWindow. SetPalette 方法 (Winutil .h) -沒有參數</span><span class="sxs-lookup"><span data-stu-id="3a68d-104">CBaseWindow.SetPalette method (Winutil.h) - No parameters</span></span>

<span data-ttu-id="3a68d-105">`SetPalette`方法會安裝視窗的調色板。</span><span class="sxs-lookup"><span data-stu-id="3a68d-105">The `SetPalette` method installs a palette for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a68d-106">語法</span><span class="sxs-lookup"><span data-stu-id="3a68d-106">Syntax</span></span>


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a><span data-ttu-id="3a68d-107">參數</span><span class="sxs-lookup"><span data-stu-id="3a68d-107">Parameters</span></span>

<span data-ttu-id="3a68d-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3a68d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a68d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a68d-109">Return value</span></span>

<span data-ttu-id="3a68d-110">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3a68d-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3a68d-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3a68d-111">Return code</span></span>                                                                             | <span data-ttu-id="3a68d-112">Description</span><span class="sxs-lookup"><span data-stu-id="3a68d-112">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="3a68d-113"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3a68d-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3a68d-114">**GdiFlush** 的內部呼叫傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a68d-114">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="3a68d-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3a68d-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3a68d-116">成功。</span><span class="sxs-lookup"><span data-stu-id="3a68d-116">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3a68d-117">備註</span><span class="sxs-lookup"><span data-stu-id="3a68d-117">Remarks</span></span>

<span data-ttu-id="3a68d-118">已選取 [**CBaseWindow：： m \_ hPalette**](cbasewindow-m-hpalette.md) 成員變數所指定的調色板。</span><span class="sxs-lookup"><span data-stu-id="3a68d-118">The palette given by the [**CBaseWindow::m\_hPalette**](cbasewindow-m-hpalette.md) member variable is selected.</span></span> <span data-ttu-id="3a68d-119">呼叫端必須確保 **m \_ hPalette** 的有效性。</span><span class="sxs-lookup"><span data-stu-id="3a68d-119">The caller must ensure the validity of **m\_hPalette**.</span></span>

<span data-ttu-id="3a68d-120">如果 [**CBaseWindow：： m \_ bNoRealize**](cbasewindow-m-bnorealize.md) 成員變數的值為 **FALSE** (預設) ，這個方法會選取並意識到這個調色板。</span><span class="sxs-lookup"><span data-stu-id="3a68d-120">If the value of the [**CBaseWindow::m\_bNoRealize**](cbasewindow-m-bnorealize.md) member variable is **FALSE** (the default), this method selects the palette and realizes it.</span></span> <span data-ttu-id="3a68d-121">否則，它會選取元件，但不會察覺到。</span><span class="sxs-lookup"><span data-stu-id="3a68d-121">Otherwise, it selects the palette but does not realize it.</span></span> <span data-ttu-id="3a68d-122">物件不會刪除任何先前使用的調色板。</span><span class="sxs-lookup"><span data-stu-id="3a68d-122">The object does not delete any previous palette that it was using.</span></span> <span data-ttu-id="3a68d-123">呼叫端負責刪除調色板。</span><span class="sxs-lookup"><span data-stu-id="3a68d-123">The caller is responsible for deleting palettes.</span></span>

<span data-ttu-id="3a68d-124">任何執行緒都可以安全地呼叫這個方法，而不只是擁有視窗的執行緒。</span><span class="sxs-lookup"><span data-stu-id="3a68d-124">Any thread can safely call this method, not just the thread that owns the window.</span></span> <span data-ttu-id="3a68d-125">視窗會將私用訊息傳送至本身，以觸發對 [**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3a68d-125">The window sends a private message to itself, which triggers a call to the [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a68d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a68d-126">Requirements</span></span>

| <span data-ttu-id="3a68d-127">需求</span><span class="sxs-lookup"><span data-stu-id="3a68d-127">Requirement</span></span> | <span data-ttu-id="3a68d-128">值</span><span class="sxs-lookup"><span data-stu-id="3a68d-128">Value</span></span> |
|-|-|
| <span data-ttu-id="3a68d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3a68d-129">Header</span></span> | <span data-ttu-id="3a68d-130">Winutil (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="3a68d-130">Winutil.h (include Streams.h)</span></span> |
| <span data-ttu-id="3a68d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3a68d-131">Library</span></span>| <span data-ttu-id="3a68d-132"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="3a68d-132">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="3a68d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a68d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a68d-134">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="3a68d-134">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




