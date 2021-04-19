---
description: CheckPaletteHeader 方法會驗證 VIDEOINFO 結構中的調色板專案。
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: 'CImageDisplay. CheckPaletteHeader 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981388"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="a2636-103">CImageDisplay. CheckPaletteHeader 方法</span><span class="sxs-lookup"><span data-stu-id="a2636-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="a2636-104">`CheckPaletteHeader`方法會驗證 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的調色板專案。</span><span class="sxs-lookup"><span data-stu-id="a2636-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2636-105">語法</span><span class="sxs-lookup"><span data-stu-id="a2636-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="a2636-106">參數</span><span class="sxs-lookup"><span data-stu-id="a2636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2636-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="a2636-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a2636-108">**VIDEOINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a2636-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2636-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2636-109">Return value</span></span>

<span data-ttu-id="a2636-110">如果調色板專案有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a2636-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2636-111">備註</span><span class="sxs-lookup"><span data-stu-id="a2636-111">Remarks</span></span>

<span data-ttu-id="a2636-112">如果影像格式不是調色盤，方法會確認 **biClrUsed** 等於零。</span><span class="sxs-lookup"><span data-stu-id="a2636-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="a2636-113">否則，此方法會驗證 **biCompression** 旗標是否為 BI \_ RGB; **biClrImportant** 不大於 **biClrUsed**;而且，如果有色彩深度，則調色板專案的數目不會超過最大值。</span><span class="sxs-lookup"><span data-stu-id="a2636-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2636-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2636-114">Requirements</span></span>



| <span data-ttu-id="a2636-115">需求</span><span class="sxs-lookup"><span data-stu-id="a2636-115">Requirement</span></span> | <span data-ttu-id="a2636-116">值</span><span class="sxs-lookup"><span data-stu-id="a2636-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2636-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a2636-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2636-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a2636-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2636-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2636-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2636-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a2636-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2636-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2636-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2636-122">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="a2636-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




