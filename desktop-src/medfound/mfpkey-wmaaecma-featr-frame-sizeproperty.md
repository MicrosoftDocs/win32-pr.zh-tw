---
description: 指定語音捕獲 DSP 所使用的音訊框架大小。
ms.assetid: b414ac34-c60a-4f43-924f-43431d6ba25f
title: 'MFPKEY_WMAAECMA_FEATR_FRAME_SIZE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5623cf3d26b968c7e7745fa0c01c69c034505cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982302"
---
# <a name="mfpkey_wmaaecma_featr_frame_size-property"></a><span data-ttu-id="b24d5-103">MFPKEY \_ WMAAECMA \_ FEATR \_ FRAME \_ SIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="b24d5-103">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE Property</span></span>

<span data-ttu-id="b24d5-104">指定語音捕獲 DSP 所使用的音訊框架大小。</span><span class="sxs-lookup"><span data-stu-id="b24d5-104">Specifies the audio frame size used by the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b24d5-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="b24d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b24d5-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="b24d5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b24d5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b24d5-107">Data Type</span></span>

<span data-ttu-id="b24d5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b24d5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b24d5-109">預設值</span><span class="sxs-lookup"><span data-stu-id="b24d5-109">Default Value</span></span>

<span data-ttu-id="b24d5-110">0</span><span class="sxs-lookup"><span data-stu-id="b24d5-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="b24d5-111">套用至</span><span class="sxs-lookup"><span data-stu-id="b24d5-111">Applies To</span></span>

-   [<span data-ttu-id="b24d5-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="b24d5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="b24d5-113">備註</span><span class="sxs-lookup"><span data-stu-id="b24d5-113">Remarks</span></span>

<span data-ttu-id="b24d5-114">聲場 echo 取消 (AEC) 演算法一次處理一個畫面格的 PCM 音訊範例。</span><span class="sxs-lookup"><span data-stu-id="b24d5-114">The acoustic echo cancellation (AEC) algorithm processes PCM audio samples one frame at a time.</span></span> <span data-ttu-id="b24d5-115">這個屬性的值是音訊框架的大小（在範例中）。</span><span class="sxs-lookup"><span data-stu-id="b24d5-115">The value of this property is the size of the audio frame, in samples.</span></span> <span data-ttu-id="b24d5-116">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="b24d5-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="b24d5-117">語音捕獲 DSP 支援下列畫面格大小：</span><span class="sxs-lookup"><span data-stu-id="b24d5-117">The Voice Capture DSP supports the following frame sizes:</span></span>

-   <span data-ttu-id="b24d5-118">80</span><span class="sxs-lookup"><span data-stu-id="b24d5-118">80</span></span>
-   <span data-ttu-id="b24d5-119">128</span><span class="sxs-lookup"><span data-stu-id="b24d5-119">128</span></span>
-   <span data-ttu-id="b24d5-120">160</span><span class="sxs-lookup"><span data-stu-id="b24d5-120">160</span></span>
-   <span data-ttu-id="b24d5-121">240</span><span class="sxs-lookup"><span data-stu-id="b24d5-121">240</span></span>
-   <span data-ttu-id="b24d5-122">256</span><span class="sxs-lookup"><span data-stu-id="b24d5-122">256</span></span>
-   <span data-ttu-id="b24d5-123">320</span><span class="sxs-lookup"><span data-stu-id="b24d5-123">320</span></span>

<span data-ttu-id="b24d5-124">如果這個屬性的值為零，則 DSP 會根據系統模式和輸出格式來選取框架大小。</span><span class="sxs-lookup"><span data-stu-id="b24d5-124">If the value of this property is zero, the DSP selects the frame size based on the system mode and the output format.</span></span>

<span data-ttu-id="b24d5-125">但為了達到最佳效能，建議應用程式使用預設值。</span><span class="sxs-lookup"><span data-stu-id="b24d5-125">For the best performance, however, it is recommended that applications use the default value.</span></span> <span data-ttu-id="b24d5-126">如果處理模式僅為麥克風陣列，則預設值為320範例。</span><span class="sxs-lookup"><span data-stu-id="b24d5-126">If the processing mode is microphone array only, the default value is 320 samples.</span></span> <span data-ttu-id="b24d5-127">針對所有其他處理模式，預設值為160範例。</span><span class="sxs-lookup"><span data-stu-id="b24d5-127">For all other processing modes, the default value is 160 samples.</span></span> <span data-ttu-id="b24d5-128">如需語音捕獲 DSP 處理模式的詳細資訊，請參閱 [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式](mfpkey-wmaaecma-system-modeproperty.md)。</span><span class="sxs-lookup"><span data-stu-id="b24d5-128">For more information about the processing modes of the Voice Capture DSP, see [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md).</span></span>

<span data-ttu-id="b24d5-129">第一次呼叫 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) 或 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput)之後，您就可以讀取此屬性來取得實際使用的框架大小，即使 [**MFPKEY \_ WMAAECMA \_ 功能 \_ 模式**](mfpkey-wmaaecma-feature-modeproperty.md) 為 false 也是如此。</span><span class="sxs-lookup"><span data-stu-id="b24d5-129">After the first call to [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) or [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput), you can read this property to get the actual frame size in use, even when [**MFPKEY\_WMAAECMA\_FEATURE\_MODE**](mfpkey-wmaaecma-feature-modeproperty.md) is false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24d5-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b24d5-130">Requirements</span></span>



| <span data-ttu-id="b24d5-131">需求</span><span class="sxs-lookup"><span data-stu-id="b24d5-131">Requirement</span></span> | <span data-ttu-id="b24d5-132">值</span><span class="sxs-lookup"><span data-stu-id="b24d5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b24d5-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b24d5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b24d5-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b24d5-134">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b24d5-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b24d5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b24d5-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b24d5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b24d5-137">標頭</span><span class="sxs-lookup"><span data-stu-id="b24d5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b24d5-138"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b24d5-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b24d5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b24d5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24d5-140">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="b24d5-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b24d5-141">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="b24d5-141">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
