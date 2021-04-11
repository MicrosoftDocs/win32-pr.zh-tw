---
description: 指定編解碼器是否會使用影片調整優化。
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: 'MFPKEY_VIDEOSCALING 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848723"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="5db1d-103">MFPKEY \_ VIDEOSCALING 屬性</span><span class="sxs-lookup"><span data-stu-id="5db1d-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="5db1d-104">指定編解碼器是否會使用影片調整優化。</span><span class="sxs-lookup"><span data-stu-id="5db1d-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5db1d-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="5db1d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5db1d-106">g \_ wszWMVCVideoScaling</span><span class="sxs-lookup"><span data-stu-id="5db1d-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="5db1d-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="5db1d-107">Data Type</span></span>

<span data-ttu-id="5db1d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5db1d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="5db1d-109">預設值</span><span class="sxs-lookup"><span data-stu-id="5db1d-109">Default Value</span></span>

<span data-ttu-id="5db1d-110">0</span><span class="sxs-lookup"><span data-stu-id="5db1d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="5db1d-111">備註</span><span class="sxs-lookup"><span data-stu-id="5db1d-111">Remarks</span></span>

<span data-ttu-id="5db1d-112">影片調整是一種可感知的優化，可改善以低位費率編碼的視覺效果品質。</span><span class="sxs-lookup"><span data-stu-id="5db1d-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="5db1d-113">影片調整優化可減少發音構件，但可能會犧牲影像詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5db1d-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="5db1d-114">這項優化會影響編碼影片的 luma 範圍（如下所述），但不會影響輸出影片的實體解析度。</span><span class="sxs-lookup"><span data-stu-id="5db1d-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="5db1d-115">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5db1d-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="5db1d-116">值</span><span class="sxs-lookup"><span data-stu-id="5db1d-116">Value</span></span> | <span data-ttu-id="5db1d-117">描述</span><span class="sxs-lookup"><span data-stu-id="5db1d-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db1d-118">0</span><span class="sxs-lookup"><span data-stu-id="5db1d-118">0</span></span>     | <span data-ttu-id="5db1d-119">不會使用影片縮放。</span><span class="sxs-lookup"><span data-stu-id="5db1d-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="5db1d-120">1</span><span class="sxs-lookup"><span data-stu-id="5db1d-120">1</span></span>     | <span data-ttu-id="5db1d-121">編碼器將使用保守的視頻調整優化。</span><span class="sxs-lookup"><span data-stu-id="5db1d-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="5db1d-122">Luma 範圍將會從 0 ... 255 調整為 26 ... 229。</span><span class="sxs-lookup"><span data-stu-id="5db1d-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="5db1d-123">2</span><span class="sxs-lookup"><span data-stu-id="5db1d-123">2</span></span>     | <span data-ttu-id="5db1d-124">編碼器將使用主動式的視頻調整優化。</span><span class="sxs-lookup"><span data-stu-id="5db1d-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="5db1d-125">Luma 範圍將會從0到255的範圍調整為 ... 224。</span><span class="sxs-lookup"><span data-stu-id="5db1d-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="5db1d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="5db1d-126">Requirements</span></span>



| <span data-ttu-id="5db1d-127">需求</span><span class="sxs-lookup"><span data-stu-id="5db1d-127">Requirement</span></span> | <span data-ttu-id="5db1d-128">值</span><span class="sxs-lookup"><span data-stu-id="5db1d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db1d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5db1d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5db1d-130">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db1d-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5db1d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5db1d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5db1d-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5db1d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5db1d-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5db1d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db1d-134"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="5db1d-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db1d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5db1d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db1d-136">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="5db1d-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




