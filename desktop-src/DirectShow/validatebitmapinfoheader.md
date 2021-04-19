---
description: ValidateBitmapInfoHeader 函式會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤，檢查 BITMAPINFOHEADER 結構。
ms.assetid: a797c286-ed77-437f-9ec1-1ef3a189bf62
title: 'ValidateBitmapInfoHeader 函式 (Checkbmi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ValidateBitmapInfoHeader
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: c7242778a2ff16414b07f887dc1e71a1547a88e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999398"
---
# <a name="validatebitmapinfoheader-function"></a><span data-ttu-id="ca942-103">ValidateBitmapInfoHeader 函式</span><span class="sxs-lookup"><span data-stu-id="ca942-103">ValidateBitmapInfoHeader function</span></span>

<span data-ttu-id="ca942-104">`ValidateBitmapInfoHeader`函數會針對可能造成緩衝區溢位或整數溢位的某些常見錯誤檢查 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。</span><span class="sxs-lookup"><span data-stu-id="ca942-104">The `ValidateBitmapInfoHeader` function checks a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="ca942-105">此函數不保證 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構有效，或使用結構的程式碼是安全的。</span><span class="sxs-lookup"><span data-stu-id="ca942-105">This function does not guarantee that the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ca942-106">語法</span><span class="sxs-lookup"><span data-stu-id="ca942-106">Syntax</span></span>


```C++
BOOL ValidateBitmapInfoHeader(
   const BITMAPINFOHEADER *pbmi,
         DWORD            cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="ca942-107">參數</span><span class="sxs-lookup"><span data-stu-id="ca942-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca942-108">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="ca942-108">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="ca942-109">要驗證之 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ca942-109">Pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure to validate.</span></span>

</dd> <dt>

<span data-ttu-id="ca942-110">*cbSize*</span><span class="sxs-lookup"><span data-stu-id="ca942-110">*cbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ca942-111">保存結構之記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ca942-111">Size of the memory block that holds the structure, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca942-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca942-112">Return value</span></span>

<span data-ttu-id="ca942-113">傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="ca942-113">Returns a Boolean value.</span></span> <span data-ttu-id="ca942-114">如果值為 **FALSE**，則表示 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構無效。</span><span class="sxs-lookup"><span data-stu-id="ca942-114">If the value is **FALSE**, the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca942-115">備註</span><span class="sxs-lookup"><span data-stu-id="ca942-115">Remarks</span></span>

<span data-ttu-id="ca942-116">此函數會針對下列錯誤進行防護：</span><span class="sxs-lookup"><span data-stu-id="ca942-116">This function guards against the following errors:</span></span>

-   <span data-ttu-id="ca942-117">結構大小或無效結構大小的算術溢位。</span><span class="sxs-lookup"><span data-stu-id="ca942-117">Arithmetic overflow in the structure size or an invalid structure size.</span></span>
-   <span data-ttu-id="ca942-118">**BiClrUsed** 成員的值無效。</span><span class="sxs-lookup"><span data-stu-id="ca942-118">Invalid value for the **biClrUsed** member.</span></span>
-   <span data-ttu-id="ca942-119">影像大小的算術溢位 (**biSizeImage**) 。</span><span class="sxs-lookup"><span data-stu-id="ca942-119">Arithmetic overflow in the image size (**biSizeImage**).</span></span>
-   <span data-ttu-id="ca942-120">針對 RGB 格式 (**biSizeImage**) 的影像大小值無效。</span><span class="sxs-lookup"><span data-stu-id="ca942-120">Invalid values for the image size (**biSizeImage**) for RGB formats.</span></span>

<span data-ttu-id="ca942-121">此函數不會檢查結構是否描述有效的影片格式。</span><span class="sxs-lookup"><span data-stu-id="ca942-121">The function does not check whether the structure describes a valid video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca942-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca942-122">Requirements</span></span>



| <span data-ttu-id="ca942-123">需求</span><span class="sxs-lookup"><span data-stu-id="ca942-123">Requirement</span></span> | <span data-ttu-id="ca942-124">值</span><span class="sxs-lookup"><span data-stu-id="ca942-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca942-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ca942-125">Header</span></span><br/> | <dl> <span data-ttu-id="ca942-126"><dt>Checkbmi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca942-126"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca942-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca942-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca942-128">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="ca942-128">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




