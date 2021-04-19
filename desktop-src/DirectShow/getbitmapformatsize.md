---
description: GetBitmapFormatSize 函式會計算 VIDEOINFO 結構所需的大小，以容納指定的 BITMAPINFOHEADER 結構。
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: 'GetBitmapFormatSize 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990234"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="ad395-103">GetBitmapFormatSize 函式</span><span class="sxs-lookup"><span data-stu-id="ad395-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="ad395-104">`GetBitmapFormatSize`函數會計算 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構所需的大小，以保存指定的 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構。</span><span class="sxs-lookup"><span data-stu-id="ad395-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad395-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad395-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="ad395-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad395-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="ad395-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="ad395-108">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ad395-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad395-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad395-109">Return value</span></span>

<span data-ttu-id="ad395-110">傳回大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad395-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad395-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad395-111">Remarks</span></span>

<span data-ttu-id="ad395-112">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構之後可能會有色彩遮罩或調色板專案，因此很難判斷從現有的 **BITMAPINFOHEADER** 結構來建立 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ad395-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="ad395-113">若要將 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構複製到 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中，請使用 [**標頭**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) 宏來計算正確的位移。</span><span class="sxs-lookup"><span data-stu-id="ad395-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="ad395-114">範例</span><span class="sxs-lookup"><span data-stu-id="ad395-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="ad395-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad395-115">Requirements</span></span>



| <span data-ttu-id="ad395-116">需求</span><span class="sxs-lookup"><span data-stu-id="ad395-116">Requirement</span></span> | <span data-ttu-id="ad395-117">值</span><span class="sxs-lookup"><span data-stu-id="ad395-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad395-118">標頭</span><span class="sxs-lookup"><span data-stu-id="ad395-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ad395-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ad395-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ad395-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad395-120">Library</span></span><br/> | <dl> <span data-ttu-id="ad395-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ad395-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad395-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad395-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad395-123">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="ad395-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




