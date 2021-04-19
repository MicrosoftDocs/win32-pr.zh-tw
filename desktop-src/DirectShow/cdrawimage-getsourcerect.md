---
description: GetSourceRect 方法會抓取目前的來源矩形。
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: 'CDrawImage. GetSourceRect 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994748"
---
# <a name="cdrawimagegetsourcerect-method"></a><span data-ttu-id="030c8-103">CDrawImage. GetSourceRect 方法</span><span class="sxs-lookup"><span data-stu-id="030c8-103">CDrawImage.GetSourceRect method</span></span>

<span data-ttu-id="030c8-104">方法會抓取 `GetSourceRect` 目前的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="030c8-104">The `GetSourceRect` method retrieves the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="030c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="030c8-105">Syntax</span></span>


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="030c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="030c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="030c8-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="030c8-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="030c8-108">接收來源矩形的 **RECT** 結構指標。</span><span class="sxs-lookup"><span data-stu-id="030c8-108">Pointer to a **RECT** structure that receives the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="030c8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="030c8-109">Return value</span></span>

<span data-ttu-id="030c8-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="030c8-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="030c8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="030c8-111">Requirements</span></span>



| <span data-ttu-id="030c8-112">需求</span><span class="sxs-lookup"><span data-stu-id="030c8-112">Requirement</span></span> | <span data-ttu-id="030c8-113">值</span><span class="sxs-lookup"><span data-stu-id="030c8-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="030c8-114">標頭</span><span class="sxs-lookup"><span data-stu-id="030c8-114">Header</span></span><br/>  | <dl> <span data-ttu-id="030c8-115"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="030c8-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="030c8-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="030c8-116">Library</span></span><br/> | <dl> <span data-ttu-id="030c8-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="030c8-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="030c8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="030c8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="030c8-119">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="030c8-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




