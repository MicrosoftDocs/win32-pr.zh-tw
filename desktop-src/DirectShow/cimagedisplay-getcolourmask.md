---
description: GetColourMask 方法會抓取目前顯示格式的色彩遮罩。
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: 'CImageDisplay. GetColourMask 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000988"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="8c7a9-103">CImageDisplay. GetColourMask 方法</span><span class="sxs-lookup"><span data-stu-id="8c7a9-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="8c7a9-104">方法會抓取 `GetColourMask` 目前顯示格式的色彩遮罩。</span><span class="sxs-lookup"><span data-stu-id="8c7a9-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c7a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="8c7a9-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="8c7a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="8c7a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c7a9-107">*pMaskRed*</span><span class="sxs-lookup"><span data-stu-id="8c7a9-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7a9-108">接收紅色元件遮罩之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8c7a9-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="8c7a9-109">*pMaskGreen*</span><span class="sxs-lookup"><span data-stu-id="8c7a9-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7a9-110">接收綠色元件遮罩之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8c7a9-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="8c7a9-111">*pMaskBlue*</span><span class="sxs-lookup"><span data-stu-id="8c7a9-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="8c7a9-112">接收藍色元件遮罩之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="8c7a9-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c7a9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c7a9-113">Return value</span></span>

<span data-ttu-id="8c7a9-114">如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8c7a9-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c7a9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c7a9-115">Requirements</span></span>



| <span data-ttu-id="8c7a9-116">需求</span><span class="sxs-lookup"><span data-stu-id="8c7a9-116">Requirement</span></span> | <span data-ttu-id="8c7a9-117">值</span><span class="sxs-lookup"><span data-stu-id="8c7a9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7a9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="8c7a9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8c7a9-119"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8c7a9-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c7a9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c7a9-120">Library</span></span><br/> | <dl> <span data-ttu-id="8c7a9-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8c7a9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c7a9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c7a9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c7a9-123">**CImageDisplay 類別**</span><span class="sxs-lookup"><span data-stu-id="8c7a9-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




