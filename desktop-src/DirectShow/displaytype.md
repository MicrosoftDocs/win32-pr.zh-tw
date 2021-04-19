---
description: DisplayType 函式會將媒體類型的相關資訊傳送至調試輸出位置。 在零售組建中略過。
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: 'DisplayType 函數 (Wxdebug .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976085"
---
# <a name="displaytype-function"></a><span data-ttu-id="7af2a-104">DisplayType 函數</span><span class="sxs-lookup"><span data-stu-id="7af2a-104">DisplayType function</span></span>

<span data-ttu-id="7af2a-105">函式會 `DisplayType` 將媒體類型的相關資訊傳送至調試輸出位置。</span><span class="sxs-lookup"><span data-stu-id="7af2a-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="7af2a-106">在零售組建中略過。</span><span class="sxs-lookup"><span data-stu-id="7af2a-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="7af2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="7af2a-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="7af2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="7af2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af2a-109">*label*</span><span class="sxs-lookup"><span data-stu-id="7af2a-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="7af2a-110">包含要以媒體類型資訊顯示之訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="7af2a-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="7af2a-111">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="7af2a-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="7af2a-112">ointer 至包含媒體類型的 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="7af2a-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af2a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7af2a-113">Return value</span></span>

<span data-ttu-id="7af2a-114">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="7af2a-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af2a-115">備註</span><span class="sxs-lookup"><span data-stu-id="7af2a-115">Remarks</span></span>

<span data-ttu-id="7af2a-116">此函數會產生數個記錄 \_ 追蹤訊息。</span><span class="sxs-lookup"><span data-stu-id="7af2a-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="7af2a-117">在記錄層級2或更高版本中，此函式會顯示主要類型、子類型和格式類型，以及來自格式區塊的資料。</span><span class="sxs-lookup"><span data-stu-id="7af2a-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="7af2a-118">在記錄層級5或更高時，此函式會顯示其他資訊，例如影片類型的來源和目標矩形。</span><span class="sxs-lookup"><span data-stu-id="7af2a-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af2a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="7af2a-119">Requirements</span></span>



| <span data-ttu-id="7af2a-120">需求</span><span class="sxs-lookup"><span data-stu-id="7af2a-120">Requirement</span></span> | <span data-ttu-id="7af2a-121">值</span><span class="sxs-lookup"><span data-stu-id="7af2a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af2a-122">標頭</span><span class="sxs-lookup"><span data-stu-id="7af2a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7af2a-123"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7af2a-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7af2a-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="7af2a-124">Library</span></span><br/> | <dl> <span data-ttu-id="7af2a-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7af2a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af2a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7af2a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af2a-127">Debug Output 函數</span><span class="sxs-lookup"><span data-stu-id="7af2a-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




