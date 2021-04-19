---
description: PreparePalette 方法會根據擁有篩選器中的媒體類型來設定調色板。
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: 'CImagePalette. PreparePalette 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992801"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="85af9-103">CImagePalette. PreparePalette 方法</span><span class="sxs-lookup"><span data-stu-id="85af9-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="85af9-104">`PreparePalette`方法會根據擁有篩選準則的媒體類型來設定調色板。</span><span class="sxs-lookup"><span data-stu-id="85af9-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="85af9-105">語法</span><span class="sxs-lookup"><span data-stu-id="85af9-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="85af9-106">參數</span><span class="sxs-lookup"><span data-stu-id="85af9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85af9-107">*pmtNew*</span><span class="sxs-lookup"><span data-stu-id="85af9-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="85af9-108">新媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="85af9-108">Pointer to the new media type.</span></span> <span data-ttu-id="85af9-109">格式區塊必須是 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="85af9-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="85af9-110">*pmtOld*</span><span class="sxs-lookup"><span data-stu-id="85af9-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="85af9-111">舊媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="85af9-111">Pointer to the old media type.</span></span> <span data-ttu-id="85af9-112">如果是第一次設定媒體類型，這個參數可以是空的型別，而且沒有格式區塊。</span><span class="sxs-lookup"><span data-stu-id="85af9-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="85af9-113">否則，格式區塊必須是 **VIDEOINFOHEADER** 結構。</span><span class="sxs-lookup"><span data-stu-id="85af9-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="85af9-114">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="85af9-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="85af9-115">字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="85af9-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="85af9-116">若要使用主顯示器裝置，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="85af9-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85af9-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="85af9-117">Return value</span></span>

<span data-ttu-id="85af9-118">如果已 \_ 更新調色板，則傳回，如果調色板未變更，則傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="85af9-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="85af9-119">備註</span><span class="sxs-lookup"><span data-stu-id="85af9-119">Remarks</span></span>

<span data-ttu-id="85af9-120">如果需要更新調色板，這個方法會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="85af9-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="85af9-121">呼叫 [**CImagePalette：： MakePalette**](cimagepalette-makepalette.md) 來建立新的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="85af9-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="85af9-122">將 [**EC \_ 調色板 \_ 已變更**](ec-palette-changed.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="85af9-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="85af9-123">在 **CBaseWindow** 物件上呼叫 [**CBaseWindow：： SetPalette**](cbasewindow-setpalette.md) 。</span><span class="sxs-lookup"><span data-stu-id="85af9-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="85af9-124">在 **CDrawImage** 物件上呼叫 [**CDrawImage：： IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) 。</span><span class="sxs-lookup"><span data-stu-id="85af9-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="85af9-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="85af9-125">Requirements</span></span>



| <span data-ttu-id="85af9-126">需求</span><span class="sxs-lookup"><span data-stu-id="85af9-126">Requirement</span></span> | <span data-ttu-id="85af9-127">值</span><span class="sxs-lookup"><span data-stu-id="85af9-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85af9-128">標頭</span><span class="sxs-lookup"><span data-stu-id="85af9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="85af9-129"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="85af9-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85af9-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="85af9-130">Library</span></span><br/> | <dl> <span data-ttu-id="85af9-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="85af9-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85af9-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85af9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85af9-133">**CImagePalette 類別**</span><span class="sxs-lookup"><span data-stu-id="85af9-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




