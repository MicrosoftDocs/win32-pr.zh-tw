---
description: 指定語音捕獲 DSP 是否執行中央裁剪。
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: 'MFPKEY_WMAAECMA_FEATR_CENTER_CLIP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191793"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="95eac-103">MFPKEY \_ WMAAECMA \_ FEATR \_ CENTER \_ 剪輯屬性</span><span class="sxs-lookup"><span data-stu-id="95eac-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="95eac-104">指定語音捕獲 DSP 是否執行中央裁剪。</span><span class="sxs-lookup"><span data-stu-id="95eac-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="95eac-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="95eac-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="95eac-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="95eac-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="95eac-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="95eac-107">Data Type</span></span>

<span data-ttu-id="95eac-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="95eac-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="95eac-109">預設值</span><span class="sxs-lookup"><span data-stu-id="95eac-109">Default Value</span></span>

<span data-ttu-id="95eac-110">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="95eac-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="95eac-111">套用至</span><span class="sxs-lookup"><span data-stu-id="95eac-111">Applies To</span></span>

-   [<span data-ttu-id="95eac-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="95eac-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="95eac-113">備註</span><span class="sxs-lookup"><span data-stu-id="95eac-113">Remarks</span></span>

<span data-ttu-id="95eac-114">置中裁剪是一種程式，可移除在 AEC 處理之後保留的小型 echo 殘差，在單一交談的情況下 (語音只會在一行) 的一端發生。</span><span class="sxs-lookup"><span data-stu-id="95eac-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="95eac-115">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="95eac-115">This property can have the following values.</span></span>



| <span data-ttu-id="95eac-116">值</span><span class="sxs-lookup"><span data-stu-id="95eac-116">Value</span></span>          | <span data-ttu-id="95eac-117">描述</span><span class="sxs-lookup"><span data-stu-id="95eac-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="95eac-118">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="95eac-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="95eac-119">停用中心裁剪。</span><span class="sxs-lookup"><span data-stu-id="95eac-119">Disable center clipping.</span></span> |
| <span data-ttu-id="95eac-120">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="95eac-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="95eac-121">啟用中央裁剪。</span><span class="sxs-lookup"><span data-stu-id="95eac-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="95eac-122">這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。</span><span class="sxs-lookup"><span data-stu-id="95eac-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="95eac-123">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="95eac-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="95eac-124">只有在啟用 AEC 處理時，DSP 才會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="95eac-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="95eac-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="95eac-125">Requirements</span></span>



| <span data-ttu-id="95eac-126">需求</span><span class="sxs-lookup"><span data-stu-id="95eac-126">Requirement</span></span> | <span data-ttu-id="95eac-127">值</span><span class="sxs-lookup"><span data-stu-id="95eac-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95eac-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95eac-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95eac-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95eac-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="95eac-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95eac-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95eac-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95eac-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="95eac-132">標頭</span><span class="sxs-lookup"><span data-stu-id="95eac-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="95eac-133"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="95eac-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95eac-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95eac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95eac-135">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="95eac-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="95eac-136">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="95eac-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
