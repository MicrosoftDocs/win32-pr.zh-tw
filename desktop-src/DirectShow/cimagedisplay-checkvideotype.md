---
description: CheckVideoType 方法會檢查指定的 VIDEOINFO 格式是否與顯示格式相容。
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: 'CImageDisplay. CheckVideoType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000931"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="ebbb3-103">CImageDisplay. CheckVideoType 方法</span><span class="sxs-lookup"><span data-stu-id="ebbb3-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="ebbb3-104">`CheckVideoType`方法會檢查指定的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)格式是否與顯示格式相容。</span><span class="sxs-lookup"><span data-stu-id="ebbb3-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebbb3-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebbb3-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="ebbb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="ebbb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebbb3-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="ebbb3-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="ebbb3-108">**VIDEOINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ebbb3-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebbb3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebbb3-109">Return value</span></span>

<span data-ttu-id="ebbb3-110">\_如果格式相容，則傳回 S OK，否則傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="ebbb3-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebbb3-111">備註</span><span class="sxs-lookup"><span data-stu-id="ebbb3-111">Remarks</span></span>

<span data-ttu-id="ebbb3-112">\_如果建議的型別可以在目前的顯示設定下輕鬆顯示，則這個方法會傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="ebbb3-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebbb3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebbb3-113">Requirements</span></span>



| <span data-ttu-id="ebbb3-114">需求</span><span class="sxs-lookup"><span data-stu-id="ebbb3-114">Requirement</span></span> | <span data-ttu-id="ebbb3-115">值</span><span class="sxs-lookup"><span data-stu-id="ebbb3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebbb3-116">標頭</span><span class="sxs-lookup"><span data-stu-id="ebbb3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ebbb3-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ebbb3-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ebbb3-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebbb3-118">Library</span></span><br/> | <dl> <span data-ttu-id="ebbb3-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ebbb3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebbb3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebbb3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebbb3-121">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="ebbb3-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




