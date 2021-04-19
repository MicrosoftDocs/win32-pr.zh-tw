---
description: CheckMediaType 方法會判斷建議的媒體類型是否與顯示格式相容。
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: 'CImageDisplay. CheckMediaType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994192"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="885d0-103">CImageDisplay. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="885d0-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="885d0-104">`CheckMediaType`方法會判斷建議的媒體類型是否與顯示格式相容。</span><span class="sxs-lookup"><span data-stu-id="885d0-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="885d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="885d0-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="885d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="885d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885d0-107">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="885d0-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="885d0-108">包含媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="885d0-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885d0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="885d0-109">Return value</span></span>

<span data-ttu-id="885d0-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="885d0-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="885d0-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="885d0-111">Possible values include the following.</span></span>



| <span data-ttu-id="885d0-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="885d0-112">Return code</span></span>                                                                                  | <span data-ttu-id="885d0-113">Description</span><span class="sxs-lookup"><span data-stu-id="885d0-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="885d0-114"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="885d0-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="885d0-115">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="885d0-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="885d0-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="885d0-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="885d0-117">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="885d0-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="885d0-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="885d0-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="885d0-119">媒體類型是相容的。</span><span class="sxs-lookup"><span data-stu-id="885d0-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="885d0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="885d0-120">Requirements</span></span>



| <span data-ttu-id="885d0-121">需求</span><span class="sxs-lookup"><span data-stu-id="885d0-121">Requirement</span></span> | <span data-ttu-id="885d0-122">值</span><span class="sxs-lookup"><span data-stu-id="885d0-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="885d0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="885d0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="885d0-124"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="885d0-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="885d0-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="885d0-125">Library</span></span><br/> | <dl> <span data-ttu-id="885d0-126"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="885d0-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="885d0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="885d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="885d0-128">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="885d0-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




