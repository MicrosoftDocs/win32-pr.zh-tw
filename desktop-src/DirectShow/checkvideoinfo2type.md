---
description: CheckVideoInfo2Type 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查包含 VIDEOINFOHEADER2 格式結構的媒體類型。
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: 'CheckVideoInfo2Type 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978773"
---
# <a name="checkvideoinfo2type-function"></a><span data-ttu-id="e1b0e-103">CheckVideoInfo2Type 函式</span><span class="sxs-lookup"><span data-stu-id="e1b0e-103">CheckVideoInfo2Type function</span></span>

<span data-ttu-id="e1b0e-104">此函式會 `CheckVideoInfo2Type` 檢查包含可能造成緩衝區溢位或整數溢位之特定常見錯誤的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式結構的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-104">The `CheckVideoInfo2Type` function checks a media type that contains a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="e1b0e-105">此函式不保證媒體類型有效，或使用結構的程式碼是安全的。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e1b0e-106">語法</span><span class="sxs-lookup"><span data-stu-id="e1b0e-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e1b0e-107">參數</span><span class="sxs-lookup"><span data-stu-id="e1b0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b0e-108">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="e1b0e-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e1b0e-109">要驗證的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b0e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1b0e-110">Return value</span></span>

<span data-ttu-id="e1b0e-111">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="e1b0e-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e1b0e-112">Return code</span></span>                                                                                                | <span data-ttu-id="e1b0e-113">Description</span><span class="sxs-lookup"><span data-stu-id="e1b0e-113">Description</span></span>                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="e1b0e-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e1b0e-115">Success</span><span class="sxs-lookup"><span data-stu-id="e1b0e-115">Success</span></span><br/>                |
| <dl> <span data-ttu-id="e1b0e-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="e1b0e-117">**Null** 指標值</span><span class="sxs-lookup"><span data-stu-id="e1b0e-117">**NULL** pointer value</span></span><br/> |
| <dl> <span data-ttu-id="e1b0e-118"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="e1b0e-119">不正確媒體類型</span><span class="sxs-lookup"><span data-stu-id="e1b0e-119">Invalid media type</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e1b0e-120">備註</span><span class="sxs-lookup"><span data-stu-id="e1b0e-120">Remarks</span></span>

<span data-ttu-id="e1b0e-121">此函數會呼叫 [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) 來驗證媒體類型中的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="e1b0e-122">如果格式類型不是 **\_ VideoInfo2 格式**，則函式會 **傳回 \_ \_ \_ 不 \_ 接受的 VFW E 類型**。</span><span class="sxs-lookup"><span data-stu-id="e1b0e-122">If the format type is not **FORMAT\_VideoInfo2**, the function returns **VFW\_E\_TYPE\_NOT\_ACCEPTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b0e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1b0e-123">Requirements</span></span>



| <span data-ttu-id="e1b0e-124">需求</span><span class="sxs-lookup"><span data-stu-id="e1b0e-124">Requirement</span></span> | <span data-ttu-id="e1b0e-125">值</span><span class="sxs-lookup"><span data-stu-id="e1b0e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b0e-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e1b0e-126">Header</span></span><br/> | <dl> <span data-ttu-id="e1b0e-127"><dt>Checkbmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b0e-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b0e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1b0e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b0e-129">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="e1b0e-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




