---
description: ShouldUpdate 方法會判斷是否需要建立新的調色板。
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: 'CImagePalette. ShouldUpdate 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990098"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="a5661-103">CImagePalette. ShouldUpdate 方法</span><span class="sxs-lookup"><span data-stu-id="a5661-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="a5661-104">`ShouldUpdate`方法會判斷是否需要建立新的調色板。</span><span class="sxs-lookup"><span data-stu-id="a5661-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5661-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5661-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a5661-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5661-107">*pNewInfo*</span><span class="sxs-lookup"><span data-stu-id="a5661-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a5661-108">[**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的指標，其中包含新的色彩表。</span><span class="sxs-lookup"><span data-stu-id="a5661-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="a5661-109">*pOldInfo*</span><span class="sxs-lookup"><span data-stu-id="a5661-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="a5661-110">**VIDEOINFOHEADER** 結構的指標，其中包含舊的色彩表。</span><span class="sxs-lookup"><span data-stu-id="a5661-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="a5661-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a5661-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5661-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5661-112">Return value</span></span>

<span data-ttu-id="a5661-113">如果需要更新調色板，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a5661-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5661-114">備註</span><span class="sxs-lookup"><span data-stu-id="a5661-114">Remarks</span></span>

-   <span data-ttu-id="a5661-115">如果兩個 **VIDEOINFOHEADER** 結構都沒有包含色彩表，則此方法會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a5661-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="a5661-116">如果只有一個結構包含色彩表，或如果 *pOldInfo* 為 **Null**，則此方法會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a5661-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="a5661-117">如果這兩個結構都包含色彩表，而且色彩專案相符，則此方法會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a5661-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="a5661-118">如果這兩個結構都包含色彩表，但色彩專案不相符，則此方法會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a5661-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5661-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5661-119">Requirements</span></span>



| <span data-ttu-id="a5661-120">需求</span><span class="sxs-lookup"><span data-stu-id="a5661-120">Requirement</span></span> | <span data-ttu-id="a5661-121">值</span><span class="sxs-lookup"><span data-stu-id="a5661-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5661-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a5661-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a5661-123"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5661-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5661-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5661-124">Library</span></span><br/> | <dl> <span data-ttu-id="a5661-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5661-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5661-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5661-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5661-127">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="a5661-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




