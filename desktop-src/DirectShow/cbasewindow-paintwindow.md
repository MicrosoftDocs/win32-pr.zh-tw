---
description: PaintWindow 方法會讓視窗重新繪製。
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: 'CBaseWindow. PaintWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987946"
---
# <a name="cbasewindowpaintwindow-method"></a><span data-ttu-id="383dc-103">CBaseWindow. PaintWindow 方法</span><span class="sxs-lookup"><span data-stu-id="383dc-103">CBaseWindow.PaintWindow method</span></span>

<span data-ttu-id="383dc-104">`PaintWindow`方法會讓視窗重新繪製。</span><span class="sxs-lookup"><span data-stu-id="383dc-104">The `PaintWindow` method causes the window to be repainted.</span></span>

## <a name="syntax"></a><span data-ttu-id="383dc-105">語法</span><span class="sxs-lookup"><span data-stu-id="383dc-105">Syntax</span></span>


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a><span data-ttu-id="383dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="383dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383dc-107">*bErase*</span><span class="sxs-lookup"><span data-stu-id="383dc-107">*bErase*</span></span> 
</dt> <dd>

<span data-ttu-id="383dc-108">指定是否清除背景的布林值。</span><span class="sxs-lookup"><span data-stu-id="383dc-108">Boolean value that specifies whether the background is erased.</span></span> <span data-ttu-id="383dc-109">如果值為 **TRUE**，則會清除背景。</span><span class="sxs-lookup"><span data-stu-id="383dc-109">If the value is **TRUE**, the background is erased.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383dc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="383dc-110">Return value</span></span>

<span data-ttu-id="383dc-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="383dc-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="383dc-112">備註</span><span class="sxs-lookup"><span data-stu-id="383dc-112">Remarks</span></span>

<span data-ttu-id="383dc-113">這個方法會藉 \_ 由使視窗的整個工作區失效，以產生 WM 繪製訊息。</span><span class="sxs-lookup"><span data-stu-id="383dc-113">This method generates a WM\_PAINT message by invalidating the window's entire client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="383dc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="383dc-114">Requirements</span></span>



| <span data-ttu-id="383dc-115">需求</span><span class="sxs-lookup"><span data-stu-id="383dc-115">Requirement</span></span> | <span data-ttu-id="383dc-116">值</span><span class="sxs-lookup"><span data-stu-id="383dc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383dc-117">標頭</span><span class="sxs-lookup"><span data-stu-id="383dc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="383dc-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="383dc-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="383dc-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="383dc-119">Library</span></span><br/> | <dl> <span data-ttu-id="383dc-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="383dc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383dc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="383dc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="383dc-122">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="383dc-122">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




