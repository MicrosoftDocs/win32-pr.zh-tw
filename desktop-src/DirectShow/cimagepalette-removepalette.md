---
description: RemovePalette 方法會刪除現有的邏輯元件，並在 CBaseWindow 物件上呼叫 CBaseWindow：： UnsetPalette。
ms.assetid: fab531b8-8630-43f8-bf08-cd8f24659bef
title: 'CImagePalette. RemovePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.RemovePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0410772203a22655968fba393c707bda790a5a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999114"
---
# <a name="cimagepaletteremovepalette-method"></a><span data-ttu-id="0b412-103">CImagePalette. RemovePalette 方法</span><span class="sxs-lookup"><span data-stu-id="0b412-103">CImagePalette.RemovePalette method</span></span>

<span data-ttu-id="0b412-104">`RemovePalette`方法會刪除現有的邏輯元件，並在 **CBaseWindow** 物件上呼叫 [**CBaseWindow：： UnsetPalette**](cbasewindow-unsetpalette.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b412-104">The `RemovePalette` method deletes the existing logical palette and calls [**CBaseWindow::UnsetPalette**](cbasewindow-unsetpalette.md) on the **CBaseWindow** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b412-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b412-105">Syntax</span></span>


```C++
HRESULT RemovePalette();
```



## <a name="parameters"></a><span data-ttu-id="0b412-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b412-106">Parameters</span></span>

<span data-ttu-id="0b412-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0b412-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b412-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b412-108">Return value</span></span>

<span data-ttu-id="0b412-109">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0b412-109">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b412-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b412-110">Requirements</span></span>



| <span data-ttu-id="0b412-111">需求</span><span class="sxs-lookup"><span data-stu-id="0b412-111">Requirement</span></span> | <span data-ttu-id="0b412-112">值</span><span class="sxs-lookup"><span data-stu-id="0b412-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b412-113">標頭</span><span class="sxs-lookup"><span data-stu-id="0b412-113">Header</span></span><br/>  | <dl> <span data-ttu-id="0b412-114"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0b412-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b412-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="0b412-115">Library</span></span><br/> | <dl> <span data-ttu-id="0b412-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0b412-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b412-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b412-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b412-118">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="0b412-118">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




