---
description: GetVideoPaletteEntries 方法會抓取影片的某個範圍元件專案。
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: 'CBaseControlVideo. GetVideoPaletteEntries 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991341"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="9fd36-103">CBaseControlVideo. GetVideoPaletteEntries 方法</span><span class="sxs-lookup"><span data-stu-id="9fd36-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="9fd36-104">方法會抓取 `GetVideoPaletteEntries` 影片的某個範圍的元件專案。</span><span class="sxs-lookup"><span data-stu-id="9fd36-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fd36-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fd36-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="9fd36-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fd36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fd36-107">*StartIndex*</span><span class="sxs-lookup"><span data-stu-id="9fd36-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd36-108">以零為基底的啟動元件專案。</span><span class="sxs-lookup"><span data-stu-id="9fd36-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="9fd36-109">*項目*</span><span class="sxs-lookup"><span data-stu-id="9fd36-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd36-110">需要的專案數目。</span><span class="sxs-lookup"><span data-stu-id="9fd36-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="9fd36-111">*pRetrieved*</span><span class="sxs-lookup"><span data-stu-id="9fd36-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd36-112">所取得色彩數目的指標。</span><span class="sxs-lookup"><span data-stu-id="9fd36-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="9fd36-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="9fd36-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="9fd36-114">色彩的輸出緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="9fd36-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fd36-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fd36-115">Return value</span></span>

<span data-ttu-id="9fd36-116">如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR; 如果 \_ 影片樣本沒有色彩調色板，則會傳回 VFW e \_ NO \_ 調色板; 如果沒有足夠的 \_ \_ 記憶體可用，則為 e OUTOFMEMORY; 如果沒有可用的記憶體， \_ 則為 e INVALIDARG; 如果選擇區中沒有色彩，則 \_ 為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="9fd36-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd36-117">備註</span><span class="sxs-lookup"><span data-stu-id="9fd36-117">Remarks</span></span>

<span data-ttu-id="9fd36-118">此成員函式會以使用者配置的陣列形式傳回影片的目前調色板。</span><span class="sxs-lookup"><span data-stu-id="9fd36-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="9fd36-119">若要保持一致，請使用 Win32 **PALETTEENTRY** 結構中的成員來傳回色彩，而不是 **RGBQUAD** (結構中的成員，但參數是 **長**) 。</span><span class="sxs-lookup"><span data-stu-id="9fd36-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="9fd36-120">記憶體是由呼叫端配置，因此只要再複製一次即可。</span><span class="sxs-lookup"><span data-stu-id="9fd36-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="9fd36-121">判斷要求的專案數和開始位置位移都有效。</span><span class="sxs-lookup"><span data-stu-id="9fd36-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="9fd36-122">如果專案數評估為零，則會傳回 \_ FALSE 代碼。</span><span class="sxs-lookup"><span data-stu-id="9fd36-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd36-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fd36-123">Requirements</span></span>



| <span data-ttu-id="9fd36-124">需求</span><span class="sxs-lookup"><span data-stu-id="9fd36-124">Requirement</span></span> | <span data-ttu-id="9fd36-125">值</span><span class="sxs-lookup"><span data-stu-id="9fd36-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd36-126">標頭</span><span class="sxs-lookup"><span data-stu-id="9fd36-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9fd36-127"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9fd36-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9fd36-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="9fd36-128">Library</span></span><br/> | <dl> <span data-ttu-id="9fd36-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="9fd36-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd36-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fd36-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd36-131">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="9fd36-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




