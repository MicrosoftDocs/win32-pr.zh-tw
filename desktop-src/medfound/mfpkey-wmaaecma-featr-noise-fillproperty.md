---
description: 指定語音捕獲 DSP 是否執行雜訊填滿。
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: 'MFPKEY_WMAAECMA_FEATR_NOISE_FILL 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989282"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="ba5fe-103">MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿屬性</span><span class="sxs-lookup"><span data-stu-id="ba5fe-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="ba5fe-104">指定語音捕獲 DSP 是否執行雜訊填滿。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ba5fe-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ba5fe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ba5fe-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ba5fe-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ba5fe-107">Data Type</span></span>

<span data-ttu-id="ba5fe-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="ba5fe-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="ba5fe-109">預設值</span><span class="sxs-lookup"><span data-stu-id="ba5fe-109">Default Value</span></span>

<span data-ttu-id="ba5fe-110">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="ba5fe-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="ba5fe-111">套用至</span><span class="sxs-lookup"><span data-stu-id="ba5fe-111">Applies To</span></span>

-   [<span data-ttu-id="ba5fe-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ba5fe-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ba5fe-113">備註</span><span class="sxs-lookup"><span data-stu-id="ba5fe-113">Remarks</span></span>

<span data-ttu-id="ba5fe-114">「雜訊填滿」會將少量的雜訊新增至「中心」裁剪已移除剩餘回應的部分信號。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="ba5fe-115">這可為使用者提供更好的體驗，而不會在信號中留下無訊息的間隔。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="ba5fe-116">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-116">This property can have the following values.</span></span>



| <span data-ttu-id="ba5fe-117">值</span><span class="sxs-lookup"><span data-stu-id="ba5fe-117">Value</span></span>          | <span data-ttu-id="ba5fe-118">描述</span><span class="sxs-lookup"><span data-stu-id="ba5fe-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="ba5fe-119">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="ba5fe-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="ba5fe-120">啟用雜訊填滿。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="ba5fe-121">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="ba5fe-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="ba5fe-122">停用雜訊填滿。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="ba5fe-123">這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="ba5fe-124">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="ba5fe-125">只有在啟用 AEC 處理時，DSP 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ba5fe-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba5fe-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba5fe-126">Requirements</span></span>



| <span data-ttu-id="ba5fe-127">需求</span><span class="sxs-lookup"><span data-stu-id="ba5fe-127">Requirement</span></span> | <span data-ttu-id="ba5fe-128">值</span><span class="sxs-lookup"><span data-stu-id="ba5fe-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5fe-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba5fe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5fe-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba5fe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ba5fe-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba5fe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5fe-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba5fe-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba5fe-133">標頭</span><span class="sxs-lookup"><span data-stu-id="ba5fe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba5fe-134"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba5fe-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba5fe-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba5fe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5fe-136">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ba5fe-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ba5fe-137">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ba5fe-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
