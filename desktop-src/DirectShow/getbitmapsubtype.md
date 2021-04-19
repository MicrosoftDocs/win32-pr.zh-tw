---
description: GetBitmapSubtype 函數會傳回指定點陣圖的媒體子類型 GUID。
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: 'GetBitmapSubtype 函式 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993352"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="c93fd-103">GetBitmapSubtype 函式</span><span class="sxs-lookup"><span data-stu-id="c93fd-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="c93fd-104">函數會傳回 `GetBitmapSubtype` 指定點陣圖的媒體子類型 **GUID** 。</span><span class="sxs-lookup"><span data-stu-id="c93fd-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="c93fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="c93fd-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="c93fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="c93fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c93fd-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="c93fd-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="c93fd-108">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c93fd-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c93fd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c93fd-109">Return value</span></span>

<span data-ttu-id="c93fd-110">傳回媒體子類型 **GUID**。</span><span class="sxs-lookup"><span data-stu-id="c93fd-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c93fd-111">備註</span><span class="sxs-lookup"><span data-stu-id="c93fd-111">Remarks</span></span>

<span data-ttu-id="c93fd-112">針對未壓縮的 RGB 類型，此函式會將 **biBitCount** 欄位對應到子類型。</span><span class="sxs-lookup"><span data-stu-id="c93fd-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="c93fd-113">針對壓縮的影片類型，此函式會使用 [**FOURCCMap**](fourccmap.md) 類別，將 **biCompression** 欄位對應至子類型。</span><span class="sxs-lookup"><span data-stu-id="c93fd-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="c93fd-114">如果函式的格式不符合子類型，則傳回值為 GUID \_ Null。</span><span class="sxs-lookup"><span data-stu-id="c93fd-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c93fd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c93fd-115">Requirements</span></span>



| <span data-ttu-id="c93fd-116">需求</span><span class="sxs-lookup"><span data-stu-id="c93fd-116">Requirement</span></span> | <span data-ttu-id="c93fd-117">值</span><span class="sxs-lookup"><span data-stu-id="c93fd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c93fd-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c93fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c93fd-119"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c93fd-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c93fd-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="c93fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="c93fd-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c93fd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c93fd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c93fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c93fd-123">影片和影像函式</span><span class="sxs-lookup"><span data-stu-id="c93fd-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




