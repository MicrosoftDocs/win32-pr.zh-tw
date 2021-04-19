---
description: 指定語音捕獲 DSP 是否執行雜訊抑制。
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: 'MFPKEY_WMAAECMA_FEATR_NS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969247"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="e8cd7-103">MFPKEY \_ WMAAECMA \_ FEATR \_ NS 屬性</span><span class="sxs-lookup"><span data-stu-id="e8cd7-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="e8cd7-104">指定語音捕獲 DSP 是否執行雜訊抑制。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e8cd7-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="e8cd7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e8cd7-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="e8cd7-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="e8cd7-107">Data Type</span></span>

<span data-ttu-id="e8cd7-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e8cd7-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e8cd7-109">預設值</span><span class="sxs-lookup"><span data-stu-id="e8cd7-109">Default Value</span></span>

<span data-ttu-id="e8cd7-110">1</span><span class="sxs-lookup"><span data-stu-id="e8cd7-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="e8cd7-111">套用至</span><span class="sxs-lookup"><span data-stu-id="e8cd7-111">Applies To</span></span>

-   [<span data-ttu-id="e8cd7-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="e8cd7-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="e8cd7-113">備註</span><span class="sxs-lookup"><span data-stu-id="e8cd7-113">Remarks</span></span>

<span data-ttu-id="e8cd7-114">雜訊隱藏是 (DSP) 元件的數位信號處理，可抑制或減少音訊信號中的靜止背景雜音。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="e8cd7-115">雜訊抑制會在聲場 echo 取消 (AEC) 和麥克風陣列處理之後套用。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="e8cd7-116">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-116">This property can have the following values.</span></span>



| <span data-ttu-id="e8cd7-117">值</span><span class="sxs-lookup"><span data-stu-id="e8cd7-117">Value</span></span> | <span data-ttu-id="e8cd7-118">描述</span><span class="sxs-lookup"><span data-stu-id="e8cd7-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="e8cd7-119">0</span><span class="sxs-lookup"><span data-stu-id="e8cd7-119">0</span></span>     | <span data-ttu-id="e8cd7-120">停用雜訊抑制。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="e8cd7-121">1</span><span class="sxs-lookup"><span data-stu-id="e8cd7-121">1</span></span>     | <span data-ttu-id="e8cd7-122">啟用雜訊抑制。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="e8cd7-123">這個屬性的預設值為 1 (已啟用) 。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="e8cd7-124">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="e8cd7-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cd7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8cd7-125">Requirements</span></span>



| <span data-ttu-id="e8cd7-126">需求</span><span class="sxs-lookup"><span data-stu-id="e8cd7-126">Requirement</span></span> | <span data-ttu-id="e8cd7-127">值</span><span class="sxs-lookup"><span data-stu-id="e8cd7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cd7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8cd7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8cd7-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8cd7-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8cd7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8cd7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8cd7-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8cd7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8cd7-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e8cd7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8cd7-133"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8cd7-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8cd7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8cd7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cd7-135">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e8cd7-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e8cd7-136">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="e8cd7-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
