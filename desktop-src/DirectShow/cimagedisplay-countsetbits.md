---
description: CountSetBits 方法會傳回在指定位欄位中設定為1的位數目。
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: 'CImageDisplay. CountSetBits 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978505"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="ed203-103">CImageDisplay. CountSetBits 方法</span><span class="sxs-lookup"><span data-stu-id="ed203-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="ed203-104">方法會傳回在 `CountSetBits` 指定位欄位中設定為1的位數目。</span><span class="sxs-lookup"><span data-stu-id="ed203-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed203-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed203-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="ed203-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed203-107">*欄位*</span><span class="sxs-lookup"><span data-stu-id="ed203-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="ed203-108">將位欄位指定為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="ed203-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed203-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed203-109">Return value</span></span>

<span data-ttu-id="ed203-110">傳回設定為1的位數目。</span><span class="sxs-lookup"><span data-stu-id="ed203-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed203-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed203-111">Requirements</span></span>



| <span data-ttu-id="ed203-112">需求</span><span class="sxs-lookup"><span data-stu-id="ed203-112">Requirement</span></span> | <span data-ttu-id="ed203-113">值</span><span class="sxs-lookup"><span data-stu-id="ed203-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed203-114">標頭</span><span class="sxs-lookup"><span data-stu-id="ed203-114">Header</span></span><br/>  | <dl> <span data-ttu-id="ed203-115"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ed203-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed203-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed203-116">Library</span></span><br/> | <dl> <span data-ttu-id="ed203-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ed203-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed203-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed203-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed203-119">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="ed203-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




