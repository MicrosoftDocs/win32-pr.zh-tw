---
title: IManipulationProcessor MinimumScaleRotateRadius 屬性
description: 指定縮放或旋轉手勢上的連絡人要觸發操作所需的距離。
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- MinimumScaleRotateRadius 屬性 Windows Touch
- MinimumScaleRotateRadius 屬性 Windows Touch，IManipulationProcessor 介面
- IManipulationProcessor 介面 Windows Touch，MinimumScaleRotateRadius 屬性
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678612"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="ecc37-106">IManipulationProcessor：： MinimumScaleRotateRadius 屬性</span><span class="sxs-lookup"><span data-stu-id="ecc37-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="ecc37-107">指定縮放或旋轉手勢上的連絡人要觸發操作所需的距離。</span><span class="sxs-lookup"><span data-stu-id="ecc37-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="ecc37-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ecc37-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc37-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecc37-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="ecc37-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ecc37-110">Property value</span></span>

<span data-ttu-id="ecc37-111">指定連絡人之間的最小距離，以觸發縮放或旋轉手勢。</span><span class="sxs-lookup"><span data-stu-id="ecc37-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ecc37-112">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="ecc37-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="ecc37-113">備註</span><span class="sxs-lookup"><span data-stu-id="ecc37-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ecc37-114">這個屬性是在圖元) 的 centipixels (100ths 中設定。</span><span class="sxs-lookup"><span data-stu-id="ecc37-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="ecc37-115">設定此值會讓操作處理器忽略半徑太小的手勢。</span><span class="sxs-lookup"><span data-stu-id="ecc37-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="ecc37-116">如果您想要防止使用者將物件操作成太小的半徑，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="ecc37-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="ecc37-117">例如，如果您使用具有圓形的操作處理器，而且想要確保它維持大於100圖元的半徑，則會將此值設定為10000。</span><span class="sxs-lookup"><span data-stu-id="ecc37-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="ecc37-118">範例</span><span class="sxs-lookup"><span data-stu-id="ecc37-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="ecc37-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecc37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc37-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="ecc37-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




