---
description: 指定語音捕獲 DSP 用來處理麥克風陣列的橫樑。
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_BEAM 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983531"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="ff28e-103">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 橫樑屬性</span><span class="sxs-lookup"><span data-stu-id="ff28e-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="ff28e-104">指定語音捕獲 DSP 用來處理麥克風陣列的橫樑。</span><span class="sxs-lookup"><span data-stu-id="ff28e-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ff28e-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ff28e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ff28e-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="ff28e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ff28e-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ff28e-107">Data Type</span></span>

<span data-ttu-id="ff28e-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ff28e-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="ff28e-109">套用至</span><span class="sxs-lookup"><span data-stu-id="ff28e-109">Applies To</span></span>

-   [<span data-ttu-id="ff28e-110">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ff28e-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ff28e-111">備註</span><span class="sxs-lookup"><span data-stu-id="ff28e-111">Remarks</span></span>

<span data-ttu-id="ff28e-112">如果 [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) 屬性的值為 MICARRAY EXTERN 橫樑，請設定此屬性 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="ff28e-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="ff28e-113">如果 [**MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) 的值是 MICARRAY \_ 單一 \_ 橫樑，您可以讀取此屬性，以查詢 DSP 所選取的橫樑。</span><span class="sxs-lookup"><span data-stu-id="ff28e-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="ff28e-114">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="ff28e-114">This property can have the following values.</span></span> <span data-ttu-id="ff28e-115">值是以度為單位的水準。</span><span class="sxs-lookup"><span data-stu-id="ff28e-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="ff28e-116">值</span><span class="sxs-lookup"><span data-stu-id="ff28e-116">Value</span></span> | <span data-ttu-id="ff28e-117">描述</span><span class="sxs-lookup"><span data-stu-id="ff28e-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="ff28e-118">0</span><span class="sxs-lookup"><span data-stu-id="ff28e-118">0</span></span>     | <span data-ttu-id="ff28e-119">-50 度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-119">-50 degrees.</span></span>             |
| <span data-ttu-id="ff28e-120">1</span><span class="sxs-lookup"><span data-stu-id="ff28e-120">1</span></span>     | <span data-ttu-id="ff28e-121">-40 度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-121">-40 degrees.</span></span>             |
| <span data-ttu-id="ff28e-122">2</span><span class="sxs-lookup"><span data-stu-id="ff28e-122">2</span></span>     | <span data-ttu-id="ff28e-123">-30 度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-123">-30 degrees.</span></span>             |
| <span data-ttu-id="ff28e-124">3</span><span class="sxs-lookup"><span data-stu-id="ff28e-124">3</span></span>     | <span data-ttu-id="ff28e-125">-20 度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-125">-20 degrees.</span></span>             |
| <span data-ttu-id="ff28e-126">4</span><span class="sxs-lookup"><span data-stu-id="ff28e-126">4</span></span>     | <span data-ttu-id="ff28e-127">-10 度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-127">-10 degrees.</span></span>             |
| <span data-ttu-id="ff28e-128">5</span><span class="sxs-lookup"><span data-stu-id="ff28e-128">5</span></span>     | <span data-ttu-id="ff28e-129">0度 (中心的橫樑) 。</span><span class="sxs-lookup"><span data-stu-id="ff28e-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="ff28e-130">6</span><span class="sxs-lookup"><span data-stu-id="ff28e-130">6</span></span>     | <span data-ttu-id="ff28e-131">10度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-131">10 degrees.</span></span>              |
| <span data-ttu-id="ff28e-132">7</span><span class="sxs-lookup"><span data-stu-id="ff28e-132">7</span></span>     | <span data-ttu-id="ff28e-133">20度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-133">20 degrees.</span></span>              |
| <span data-ttu-id="ff28e-134">8</span><span class="sxs-lookup"><span data-stu-id="ff28e-134">8</span></span>     | <span data-ttu-id="ff28e-135">30度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-135">30 degrees.</span></span>              |
| <span data-ttu-id="ff28e-136">9</span><span class="sxs-lookup"><span data-stu-id="ff28e-136">9</span></span>     | <span data-ttu-id="ff28e-137">40度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-137">40 degrees.</span></span>              |
| <span data-ttu-id="ff28e-138">10</span><span class="sxs-lookup"><span data-stu-id="ff28e-138">10</span></span>    | <span data-ttu-id="ff28e-139">50度。</span><span class="sxs-lookup"><span data-stu-id="ff28e-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="ff28e-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff28e-140">Requirements</span></span>



| <span data-ttu-id="ff28e-141">需求</span><span class="sxs-lookup"><span data-stu-id="ff28e-141">Requirement</span></span> | <span data-ttu-id="ff28e-142">值</span><span class="sxs-lookup"><span data-stu-id="ff28e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff28e-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff28e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ff28e-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff28e-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ff28e-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff28e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ff28e-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff28e-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff28e-147">標頭</span><span class="sxs-lookup"><span data-stu-id="ff28e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff28e-148"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff28e-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff28e-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff28e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff28e-150">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ff28e-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ff28e-151">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ff28e-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
