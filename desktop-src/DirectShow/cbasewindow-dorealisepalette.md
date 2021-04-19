---
description: DoRealisePalette 方法會發現視窗的目前調色板。
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: 'CBaseWindow. DoRealisePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991555"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="94772-103">CBaseWindow. DoRealisePalette 方法</span><span class="sxs-lookup"><span data-stu-id="94772-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="94772-104">方法會發現 `DoRealisePalette` 視窗的目前調色板。</span><span class="sxs-lookup"><span data-stu-id="94772-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="94772-105">語法</span><span class="sxs-lookup"><span data-stu-id="94772-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="94772-106">參數</span><span class="sxs-lookup"><span data-stu-id="94772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94772-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="94772-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="94772-108">布林值，指定是否要將調色板強制為背景調色板。</span><span class="sxs-lookup"><span data-stu-id="94772-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="94772-109">如需詳細資訊，請參閱 Platform SDK 中的 **SelectPalette** 。</span><span class="sxs-lookup"><span data-stu-id="94772-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94772-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="94772-110">Return value</span></span>

<span data-ttu-id="94772-111">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="94772-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="94772-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="94772-112">Return code</span></span>                                                                             | <span data-ttu-id="94772-113">Description</span><span class="sxs-lookup"><span data-stu-id="94772-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="94772-114"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="94772-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="94772-115">**GdiFlush** 的內部呼叫傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="94772-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="94772-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="94772-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="94772-117">成功。</span><span class="sxs-lookup"><span data-stu-id="94772-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="94772-118">備註</span><span class="sxs-lookup"><span data-stu-id="94772-118">Remarks</span></span>

<span data-ttu-id="94772-119">[**CBaseWindow：： OnPaletteChange**](cbasewindow-onpalettechange.md)方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="94772-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="94772-120">若要設定新的調色板，請呼叫 [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="94772-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94772-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="94772-121">Requirements</span></span>



| <span data-ttu-id="94772-122">需求</span><span class="sxs-lookup"><span data-stu-id="94772-122">Requirement</span></span> | <span data-ttu-id="94772-123">值</span><span class="sxs-lookup"><span data-stu-id="94772-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94772-124">標頭</span><span class="sxs-lookup"><span data-stu-id="94772-124">Header</span></span><br/>  | <dl> <span data-ttu-id="94772-125"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="94772-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94772-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="94772-126">Library</span></span><br/> | <dl> <span data-ttu-id="94772-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="94772-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94772-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94772-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94772-129">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="94772-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




