---
description: 指定語音捕獲 DSP 是否套用麥克風增益區。
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: 'MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985424"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="7e29f-103">MFPKEY \_ WMAAECMA \_ MIC \_ 增益 \_ BOUNDER 屬性</span><span class="sxs-lookup"><span data-stu-id="7e29f-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="7e29f-104">指定語音捕獲 DSP 是否套用麥克風增益區。</span><span class="sxs-lookup"><span data-stu-id="7e29f-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7e29f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="7e29f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7e29f-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="7e29f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7e29f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="7e29f-107">Data Type</span></span>

<span data-ttu-id="7e29f-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="7e29f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="7e29f-109">預設值</span><span class="sxs-lookup"><span data-stu-id="7e29f-109">Default Value</span></span>

<span data-ttu-id="7e29f-110">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="7e29f-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="7e29f-111">套用至</span><span class="sxs-lookup"><span data-stu-id="7e29f-111">Applies To</span></span>

-   [<span data-ttu-id="7e29f-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="7e29f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="7e29f-113">備註</span><span class="sxs-lookup"><span data-stu-id="7e29f-113">Remarks</span></span>

<span data-ttu-id="7e29f-114">麥克風增益界限可確保麥克風具有正確的增益等級。</span><span class="sxs-lookup"><span data-stu-id="7e29f-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="7e29f-115">如果增益過高，則捕捉的信號可能會飽和，並會被裁剪。</span><span class="sxs-lookup"><span data-stu-id="7e29f-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="7e29f-116">裁剪是非線性效果，這會導致聲場回顯取消 (AEC) 演算法失敗。</span><span class="sxs-lookup"><span data-stu-id="7e29f-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="7e29f-117">如果增益過低，則信號雜訊比例很低，這也會導致 AEC 演算法失敗或無法正常執行。</span><span class="sxs-lookup"><span data-stu-id="7e29f-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="7e29f-118">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="7e29f-118">This property can have the following values.</span></span>



| <span data-ttu-id="7e29f-119">值</span><span class="sxs-lookup"><span data-stu-id="7e29f-119">Value</span></span>          | <span data-ttu-id="7e29f-120">描述</span><span class="sxs-lookup"><span data-stu-id="7e29f-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="7e29f-121">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="7e29f-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="7e29f-122">啟用麥克風增益範圍。</span><span class="sxs-lookup"><span data-stu-id="7e29f-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="7e29f-123">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="7e29f-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="7e29f-124">停用麥克風增益範圍。</span><span class="sxs-lookup"><span data-stu-id="7e29f-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="7e29f-125">這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。</span><span class="sxs-lookup"><span data-stu-id="7e29f-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="7e29f-126">只有在 DSP 以來源模式運作時，才會套用麥克風增益界限。</span><span class="sxs-lookup"><span data-stu-id="7e29f-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="7e29f-127">在篩選模式中，應用程式必須確定麥克風具有正確的增益等級。</span><span class="sxs-lookup"><span data-stu-id="7e29f-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e29f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e29f-128">Requirements</span></span>



| <span data-ttu-id="7e29f-129">需求</span><span class="sxs-lookup"><span data-stu-id="7e29f-129">Requirement</span></span> | <span data-ttu-id="7e29f-130">值</span><span class="sxs-lookup"><span data-stu-id="7e29f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e29f-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e29f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7e29f-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e29f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7e29f-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e29f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7e29f-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e29f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7e29f-135">標頭</span><span class="sxs-lookup"><span data-stu-id="7e29f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e29f-136"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e29f-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e29f-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e29f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e29f-138">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="7e29f-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7e29f-139">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="7e29f-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
