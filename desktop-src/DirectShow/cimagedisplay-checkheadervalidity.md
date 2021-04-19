---
description: CheckHeaderValidity 方法會驗證 BITMAPINFOHEADER 結構。 這個方法僅適用于未壓縮的 RGB 類型，不適用於壓縮類型或 YUV 類型。
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: 'CImageDisplay. CheckHeaderValidity 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995626"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="8432b-104">CImageDisplay. CheckHeaderValidity 方法</span><span class="sxs-lookup"><span data-stu-id="8432b-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="8432b-105">`CheckHeaderValidity`方法會驗證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。</span><span class="sxs-lookup"><span data-stu-id="8432b-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="8432b-106">這個方法僅適用于未壓縮的 RGB 類型，不適用於壓縮類型或 YUV 類型。</span><span class="sxs-lookup"><span data-stu-id="8432b-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8432b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8432b-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="8432b-108">參數</span><span class="sxs-lookup"><span data-stu-id="8432b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8432b-109">*pInput*</span><span class="sxs-lookup"><span data-stu-id="8432b-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8432b-110">包含 **BITMAPINFOHEADER** 結構之 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8432b-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8432b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8432b-111">Return value</span></span>

<span data-ttu-id="8432b-112">如果 **BITMAPINFOHEADER** 有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8432b-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8432b-113">備註</span><span class="sxs-lookup"><span data-stu-id="8432b-113">Remarks</span></span>

<span data-ttu-id="8432b-114">這個方法會檢查影像維度是否為非負值;壓縮類型為 BI \_ RGB 或 bi \_ 位欄位; 色彩深度和色彩遮罩有效; **biPlanes** 成員等於 1; **biSize** 和 **biSizeImage** 成員是正確的。</span><span class="sxs-lookup"><span data-stu-id="8432b-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="8432b-115">它也會檢查調色板專案中的常見錯誤（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="8432b-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="8432b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8432b-116">Requirements</span></span>



| <span data-ttu-id="8432b-117">需求</span><span class="sxs-lookup"><span data-stu-id="8432b-117">Requirement</span></span> | <span data-ttu-id="8432b-118">值</span><span class="sxs-lookup"><span data-stu-id="8432b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8432b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8432b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8432b-120"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8432b-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8432b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="8432b-121">Library</span></span><br/> | <dl> <span data-ttu-id="8432b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8432b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8432b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8432b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8432b-124">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="8432b-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




