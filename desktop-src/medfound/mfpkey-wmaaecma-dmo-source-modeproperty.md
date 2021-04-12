---
description: 指定語音捕獲 DSP 是否使用來源模式或篩選模式。
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: 'MFPKEY_WMAAECMA_DMO_SOURCE_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191794"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="e18fd-103">MFPKEY \_ WMAAECMA \_ 中 \_ 來源 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="e18fd-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="e18fd-104">指定語音捕獲 DSP 是否使用來源模式或篩選模式。</span><span class="sxs-lookup"><span data-stu-id="e18fd-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e18fd-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="e18fd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e18fd-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="e18fd-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e18fd-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e18fd-107">Data Type</span></span>

<span data-ttu-id="e18fd-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="e18fd-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="e18fd-109">預設值</span><span class="sxs-lookup"><span data-stu-id="e18fd-109">Default Value</span></span>

<span data-ttu-id="e18fd-110">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="e18fd-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="e18fd-111">套用至</span><span class="sxs-lookup"><span data-stu-id="e18fd-111">Applies To</span></span>

-   [<span data-ttu-id="e18fd-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="e18fd-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="e18fd-113">備註</span><span class="sxs-lookup"><span data-stu-id="e18fd-113">Remarks</span></span>

<span data-ttu-id="e18fd-114">在來源模式中，應用程式不需要將輸入資料傳送給 DSP，因為 DSP 會自動從音訊裝置提取資料。</span><span class="sxs-lookup"><span data-stu-id="e18fd-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="e18fd-115">在篩選模式中，應用程式必須將輸入資料傳送給 DSP。</span><span class="sxs-lookup"><span data-stu-id="e18fd-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="e18fd-116">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="e18fd-116">This property can have the following values.</span></span>



| <span data-ttu-id="e18fd-117">值</span><span class="sxs-lookup"><span data-stu-id="e18fd-117">Value</span></span>          | <span data-ttu-id="e18fd-118">描述</span><span class="sxs-lookup"><span data-stu-id="e18fd-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="e18fd-119">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="e18fd-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="e18fd-120">篩選模式。</span><span class="sxs-lookup"><span data-stu-id="e18fd-120">Filter mode.</span></span> |
| <span data-ttu-id="e18fd-121">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="e18fd-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="e18fd-122">來源模式。</span><span class="sxs-lookup"><span data-stu-id="e18fd-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="e18fd-123">當 SQL-DMO 處於來源模式時，您應該只呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) 來設定輸出資料流程格式，而不要呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) 來設定輸入資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="e18fd-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="e18fd-124">否則，將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e18fd-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="e18fd-125">如果這個屬性的值為 VARIANT \_ TRUE，則表示 DSP 的輸入為零。</span><span class="sxs-lookup"><span data-stu-id="e18fd-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="e18fd-126">如果值為 VARIANT \_ FALSE，則根據 [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式](mfpkey-wmaaecma-system-modeproperty.md) 屬性的值而定，DSP 會有一或兩個輸入，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="e18fd-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="e18fd-127">值</span><span class="sxs-lookup"><span data-stu-id="e18fd-127">Value</span></span>                     | <span data-ttu-id="e18fd-128">輸入數目</span><span class="sxs-lookup"><span data-stu-id="e18fd-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="e18fd-129">OPTIBEAM \_ 陣列 \_ 和 \_ AEC</span><span class="sxs-lookup"><span data-stu-id="e18fd-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="e18fd-130">2</span><span class="sxs-lookup"><span data-stu-id="e18fd-130">2</span></span>                |
| <span data-ttu-id="e18fd-131">\_ \_ 僅限 OPTIBEAM 陣列</span><span class="sxs-lookup"><span data-stu-id="e18fd-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="e18fd-132">1</span><span class="sxs-lookup"><span data-stu-id="e18fd-132">1</span></span>                |
| <span data-ttu-id="e18fd-133">單一 \_ 通道 \_ AEC</span><span class="sxs-lookup"><span data-stu-id="e18fd-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="e18fd-134">2</span><span class="sxs-lookup"><span data-stu-id="e18fd-134">2</span></span>                |
| <span data-ttu-id="e18fd-135">單一 \_ 通道 \_ NSAGC</span><span class="sxs-lookup"><span data-stu-id="e18fd-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="e18fd-136">1</span><span class="sxs-lookup"><span data-stu-id="e18fd-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="e18fd-137">只有具有單一輸入的模式，才可以從 DirectShow 9.0 API 使用包裝函式篩選。</span><span class="sxs-lookup"><span data-stu-id="e18fd-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e18fd-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="e18fd-138">Requirements</span></span>



| <span data-ttu-id="e18fd-139">需求</span><span class="sxs-lookup"><span data-stu-id="e18fd-139">Requirement</span></span> | <span data-ttu-id="e18fd-140">值</span><span class="sxs-lookup"><span data-stu-id="e18fd-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e18fd-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e18fd-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e18fd-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e18fd-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e18fd-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e18fd-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e18fd-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e18fd-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e18fd-145">標頭</span><span class="sxs-lookup"><span data-stu-id="e18fd-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e18fd-146"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e18fd-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e18fd-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e18fd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e18fd-148">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e18fd-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e18fd-149">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="e18fd-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
