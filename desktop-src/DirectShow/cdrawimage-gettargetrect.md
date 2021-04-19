---
description: GetTargetRect 方法會抓取目前的目的地矩形。
ms.assetid: b6542b06-af36-4666-b6fa-d9fa3c6c7044
title: 'CDrawImage. GetTargetRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 547dd12117cec95ad1cb0159667a8dd72a95a6e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977682"
---
# <a name="cdrawimagegettargetrect-method"></a><span data-ttu-id="9c9b9-103">CDrawImage. GetTargetRect 方法</span><span class="sxs-lookup"><span data-stu-id="9c9b9-103">CDrawImage.GetTargetRect method</span></span>

<span data-ttu-id="9c9b9-104">方法會抓取 `GetTargetRect` 目前的目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="9c9b9-104">The `GetTargetRect` method retrieves the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9b9-105">語法</span><span class="sxs-lookup"><span data-stu-id="9c9b9-105">Syntax</span></span>


```C++
void GetTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="9c9b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="9c9b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c9b9-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="9c9b9-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="9c9b9-108">接收目標矩形的 **RECT** 結構指標。</span><span class="sxs-lookup"><span data-stu-id="9c9b9-108">Pointer to a **RECT** structure that receives the target rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c9b9-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c9b9-109">Return value</span></span>

<span data-ttu-id="9c9b9-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9c9b9-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c9b9-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c9b9-111">Requirements</span></span>



| <span data-ttu-id="9c9b9-112">需求</span><span class="sxs-lookup"><span data-stu-id="9c9b9-112">Requirement</span></span> | <span data-ttu-id="9c9b9-113">值</span><span class="sxs-lookup"><span data-stu-id="9c9b9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c9b9-114">標頭</span><span class="sxs-lookup"><span data-stu-id="9c9b9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9c9b9-115"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9c9b9-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9c9b9-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="9c9b9-116">Library</span></span><br/> | <dl> <span data-ttu-id="9c9b9-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9c9b9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c9b9-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c9b9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c9b9-119">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="9c9b9-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




