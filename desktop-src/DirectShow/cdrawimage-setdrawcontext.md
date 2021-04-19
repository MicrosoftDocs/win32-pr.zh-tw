---
description: SetDrawCoNtext 方法會設定用於繪製的裝置內容。
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: 'CDrawImage. SetDrawCoNtext 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982990"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="3cc50-103">CDrawImage. SetDrawCoNtext 方法</span><span class="sxs-lookup"><span data-stu-id="3cc50-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="3cc50-104">`SetDrawContext`方法會設定用於繪製的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="3cc50-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc50-105">語法</span><span class="sxs-lookup"><span data-stu-id="3cc50-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="3cc50-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cc50-106">Parameters</span></span>

<span data-ttu-id="3cc50-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3cc50-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cc50-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cc50-108">Return value</span></span>

<span data-ttu-id="3cc50-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="3cc50-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc50-110">備註</span><span class="sxs-lookup"><span data-stu-id="3cc50-110">Remarks</span></span>

<span data-ttu-id="3cc50-111">這個方法會從擁有的 [**CBaseWindow**](cbasewindow.md) 物件抓取視窗和記憶體裝置內容。</span><span class="sxs-lookup"><span data-stu-id="3cc50-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="3cc50-112">請在初始化視窗之後，但在開始繪製之前呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3cc50-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc50-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cc50-113">Requirements</span></span>



| <span data-ttu-id="3cc50-114">需求</span><span class="sxs-lookup"><span data-stu-id="3cc50-114">Requirement</span></span> | <span data-ttu-id="3cc50-115">值</span><span class="sxs-lookup"><span data-stu-id="3cc50-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc50-116">標頭</span><span class="sxs-lookup"><span data-stu-id="3cc50-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3cc50-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3cc50-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cc50-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="3cc50-118">Library</span></span><br/> | <dl> <span data-ttu-id="3cc50-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3cc50-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cc50-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cc50-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc50-121">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="3cc50-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




