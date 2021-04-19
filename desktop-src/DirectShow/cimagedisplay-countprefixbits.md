---
description: CountPrefixBits 方法會計算指定位欄位開頭的零位位數。
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: 'CImageDisplay. CountPrefixBits 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990701"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="2faa2-103">CImageDisplay. CountPrefixBits 方法</span><span class="sxs-lookup"><span data-stu-id="2faa2-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="2faa2-104">`CountPrefixBits`方法會計算在指定位欄位開頭的零位位數。</span><span class="sxs-lookup"><span data-stu-id="2faa2-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="2faa2-105">語法</span><span class="sxs-lookup"><span data-stu-id="2faa2-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="2faa2-106">參數</span><span class="sxs-lookup"><span data-stu-id="2faa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2faa2-107">*欄位*</span><span class="sxs-lookup"><span data-stu-id="2faa2-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="2faa2-108">將位欄位指定為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="2faa2-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2faa2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="2faa2-109">Return value</span></span>

<span data-ttu-id="2faa2-110">傳回前1位之前發生的零位位數，如果所有位都是零，則傳回0x80000000。</span><span class="sxs-lookup"><span data-stu-id="2faa2-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2faa2-111">備註</span><span class="sxs-lookup"><span data-stu-id="2faa2-111">Remarks</span></span>

<span data-ttu-id="2faa2-112">這個方法適用于使用 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 結構中的色遮罩。</span><span class="sxs-lookup"><span data-stu-id="2faa2-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="2faa2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2faa2-113">Requirements</span></span>



| <span data-ttu-id="2faa2-114">需求</span><span class="sxs-lookup"><span data-stu-id="2faa2-114">Requirement</span></span> | <span data-ttu-id="2faa2-115">值</span><span class="sxs-lookup"><span data-stu-id="2faa2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2faa2-116">標頭</span><span class="sxs-lookup"><span data-stu-id="2faa2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2faa2-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2faa2-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2faa2-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="2faa2-118">Library</span></span><br/> | <dl> <span data-ttu-id="2faa2-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2faa2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2faa2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2faa2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2faa2-121">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="2faa2-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




