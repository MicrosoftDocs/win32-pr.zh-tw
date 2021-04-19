---
description: CheckVideoInfoType 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查包含 VIDEOINFOHEADER 格式結構的媒體類型。
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: 'CheckVideoInfoType 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993519"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="99344-103">CheckVideoInfoType 函式</span><span class="sxs-lookup"><span data-stu-id="99344-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="99344-104">此函式會 `CheckVideoInfoType` 檢查包含可能造成緩衝區溢位或整數溢位之特定常見錯誤的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式結構的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="99344-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="99344-105">此函式不保證媒體類型有效，或使用結構的程式碼是安全的。</span><span class="sxs-lookup"><span data-stu-id="99344-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="99344-106">語法</span><span class="sxs-lookup"><span data-stu-id="99344-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="99344-107">參數</span><span class="sxs-lookup"><span data-stu-id="99344-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99344-108">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="99344-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="99344-109">要驗證的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構指標</span><span class="sxs-lookup"><span data-stu-id="99344-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99344-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="99344-110">Return value</span></span>

<span data-ttu-id="99344-111">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="99344-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="99344-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="99344-112">Return code</span></span>                                                                                                | <span data-ttu-id="99344-113">Description</span><span class="sxs-lookup"><span data-stu-id="99344-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="99344-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="99344-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="99344-115">成功。</span><span class="sxs-lookup"><span data-stu-id="99344-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="99344-116"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="99344-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="99344-117">**Null** 指標值。</span><span class="sxs-lookup"><span data-stu-id="99344-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="99344-118"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="99344-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="99344-119">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="99344-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="99344-120">備註</span><span class="sxs-lookup"><span data-stu-id="99344-120">Remarks</span></span>

<span data-ttu-id="99344-121">此函數會呼叫 [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) 來驗證媒體類型中的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構。</span><span class="sxs-lookup"><span data-stu-id="99344-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="99344-122">如果格式類型不是 VideoInfo 格式 \_ ，則函式會傳回 \_ 不接受的 VFW E \_ 類型 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="99344-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="99344-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="99344-123">Requirements</span></span>



| <span data-ttu-id="99344-124">需求</span><span class="sxs-lookup"><span data-stu-id="99344-124">Requirement</span></span> | <span data-ttu-id="99344-125">值</span><span class="sxs-lookup"><span data-stu-id="99344-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99344-126">標頭</span><span class="sxs-lookup"><span data-stu-id="99344-126">Header</span></span><br/> | <dl> <span data-ttu-id="99344-127"><dt>Checkbmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="99344-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99344-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99344-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99344-129">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="99344-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




