---
description: CheckBitFields 方法會驗證 VIDEOINFO 結構中的色遮罩。
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: 'CImageDisplay. CheckBitFields 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995202"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="8a5c4-103">CImageDisplay. CheckBitFields 方法</span><span class="sxs-lookup"><span data-stu-id="8a5c4-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="8a5c4-104">`CheckBitFields`方法會驗證 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)結構中的色遮罩。</span><span class="sxs-lookup"><span data-stu-id="8a5c4-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a5c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a5c4-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="8a5c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a5c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a5c4-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="8a5c4-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="8a5c4-108">**VIDEOINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8a5c4-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a5c4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a5c4-109">Return value</span></span>

<span data-ttu-id="8a5c4-110">如果色彩遮罩有效，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8a5c4-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a5c4-111">備註</span><span class="sxs-lookup"><span data-stu-id="8a5c4-111">Remarks</span></span>

<span data-ttu-id="8a5c4-112">這個方法會確認每個色彩元件的色彩遮罩長度介於1到8個位之間，而且每個色彩遮罩都是連續的位序列。</span><span class="sxs-lookup"><span data-stu-id="8a5c4-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="8a5c4-113">只有當 **biCompression** 成員設定為 BI 位欄位時，才會呼叫這個方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="8a5c4-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a5c4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a5c4-114">Requirements</span></span>



| <span data-ttu-id="8a5c4-115">需求</span><span class="sxs-lookup"><span data-stu-id="8a5c4-115">Requirement</span></span> | <span data-ttu-id="8a5c4-116">值</span><span class="sxs-lookup"><span data-stu-id="8a5c4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a5c4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8a5c4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8a5c4-118"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8a5c4-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a5c4-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8a5c4-119">Library</span></span><br/> | <dl> <span data-ttu-id="8a5c4-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8a5c4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a5c4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a5c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a5c4-122">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="8a5c4-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




