---
description: Put \_ BackgroundPalette 方法會設定旗標，以在背景中實現調色板。
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: 'CBaseControlWindow.put_BackgroundPalette 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989612"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a><span data-ttu-id="c34bc-103">CBaseControlWindow. put \_ BackgroundPalette 方法</span><span class="sxs-lookup"><span data-stu-id="c34bc-103">CBaseControlWindow.put\_BackgroundPalette method</span></span>

<span data-ttu-id="c34bc-104">`put_BackgroundPalette`方法會設定旗標，以在背景中實現調色板。</span><span class="sxs-lookup"><span data-stu-id="c34bc-104">The `put_BackgroundPalette` method sets a flag to realize the palette in the background.</span></span>

## <a name="syntax"></a><span data-ttu-id="c34bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="c34bc-105">Syntax</span></span>


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c34bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="c34bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34bc-107">*BackgroundPalette*</span><span class="sxs-lookup"><span data-stu-id="c34bc-107">*BackgroundPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="c34bc-108">自動化布林值旗標 (0 是 off，1是) 。</span><span class="sxs-lookup"><span data-stu-id="c34bc-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34bc-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c34bc-109">Return value</span></span>

<span data-ttu-id="c34bc-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c34bc-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c34bc-111">備註</span><span class="sxs-lookup"><span data-stu-id="c34bc-111">Remarks</span></span>

<span data-ttu-id="c34bc-112">若要在另一個應用程式或檔內播放影片，應用程式可能會想要使用自己的調色板。</span><span class="sxs-lookup"><span data-stu-id="c34bc-112">To play a video within another application or document, the application might want to use its own palette.</span></span> <span data-ttu-id="c34bc-113">它可以將此旗標設定為1，要求影片使用目前的前景調色板，而不是它自己的背景調色板。</span><span class="sxs-lookup"><span data-stu-id="c34bc-113">It can ask that the video use the current foreground palette rather than its own as the background palette by setting this flag to  1.</span></span> <span data-ttu-id="c34bc-114">如果此設定為0，則視窗將會安裝並瞭解它自己慣用的調色板。</span><span class="sxs-lookup"><span data-stu-id="c34bc-114">If this is set to 0, the window will install and realize its own preferred palette.</span></span> <span data-ttu-id="c34bc-115">要求視窗使用不同的調色板將會造成嚴重的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="c34bc-115">Asking the window to use a different palette will cause severe performance penalties.</span></span>

## <a name="requirements"></a><span data-ttu-id="c34bc-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c34bc-116">Requirements</span></span>



| <span data-ttu-id="c34bc-117">需求</span><span class="sxs-lookup"><span data-stu-id="c34bc-117">Requirement</span></span> | <span data-ttu-id="c34bc-118">值</span><span class="sxs-lookup"><span data-stu-id="c34bc-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c34bc-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c34bc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c34bc-120"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c34bc-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c34bc-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="c34bc-121">Library</span></span><br/> | <dl> <span data-ttu-id="c34bc-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c34bc-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34bc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c34bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34bc-124">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="c34bc-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




