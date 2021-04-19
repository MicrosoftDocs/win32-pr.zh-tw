---
description: GetBitMasks 方法會抓取指定 VIDEOINFO 格式的色彩遮罩。
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: 'CImageDisplay. GetBitMasks 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998643"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="e5361-103">CImageDisplay. GetBitMasks 方法</span><span class="sxs-lookup"><span data-stu-id="e5361-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="e5361-104">方法會抓取 `GetBitMasks` 指定 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) 格式的色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="e5361-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5361-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5361-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e5361-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5361-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5361-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="e5361-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e5361-108">**VIDEOINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e5361-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5361-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5361-109">Return value</span></span>

<span data-ttu-id="e5361-110">傳回三個 **DWORD** 值的陣列。</span><span class="sxs-lookup"><span data-stu-id="e5361-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5361-111">備註</span><span class="sxs-lookup"><span data-stu-id="e5361-111">Remarks</span></span>

<span data-ttu-id="e5361-112">如果 **biCompression** 成員是 BI \_ 位欄位，此方法會傳回 **dwBitMasks** 成員中所提供之色彩遮罩的指標。</span><span class="sxs-lookup"><span data-stu-id="e5361-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="e5361-113">如果 **biCompression** 成員是 BI \_ RGB，則方法會傳回對應于位深度的色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="e5361-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="e5361-114">如果方法失敗 (例如，位深度小於 16) ，則方法會傳回陣列 {0,0,0} 。</span><span class="sxs-lookup"><span data-stu-id="e5361-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5361-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5361-115">Requirements</span></span>



| <span data-ttu-id="e5361-116">需求</span><span class="sxs-lookup"><span data-stu-id="e5361-116">Requirement</span></span> | <span data-ttu-id="e5361-117">值</span><span class="sxs-lookup"><span data-stu-id="e5361-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5361-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e5361-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e5361-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e5361-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5361-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5361-120">Library</span></span><br/> | <dl> <span data-ttu-id="e5361-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e5361-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5361-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5361-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5361-123">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="e5361-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




