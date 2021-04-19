---
description: GetBitmapSize 函式會計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。 此函數只會呼叫 DIBSIZE 宏。
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: 'GetBitmapSize 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995320"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="130ed-104">GetBitmapSize 函式</span><span class="sxs-lookup"><span data-stu-id="130ed-104">GetBitmapSize function</span></span>

<span data-ttu-id="130ed-105">函 `GetBitmapSize` 式會計算與裝置無關的點陣圖 (DIB) 所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="130ed-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="130ed-106">此函數只會呼叫 [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) 宏。</span><span class="sxs-lookup"><span data-stu-id="130ed-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="130ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="130ed-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="130ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="130ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="130ed-109">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="130ed-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="130ed-110">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="130ed-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="130ed-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="130ed-111">Return value</span></span>

<span data-ttu-id="130ed-112">傳回以位元組為單位的大小。</span><span class="sxs-lookup"><span data-stu-id="130ed-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="130ed-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="130ed-113">Requirements</span></span>



| <span data-ttu-id="130ed-114">需求</span><span class="sxs-lookup"><span data-stu-id="130ed-114">Requirement</span></span> | <span data-ttu-id="130ed-115">值</span><span class="sxs-lookup"><span data-stu-id="130ed-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="130ed-116">標頭</span><span class="sxs-lookup"><span data-stu-id="130ed-116">Header</span></span><br/>  | <dl> <span data-ttu-id="130ed-117"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="130ed-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="130ed-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="130ed-118">Library</span></span><br/> | <dl> <span data-ttu-id="130ed-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="130ed-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="130ed-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="130ed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="130ed-121">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="130ed-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




