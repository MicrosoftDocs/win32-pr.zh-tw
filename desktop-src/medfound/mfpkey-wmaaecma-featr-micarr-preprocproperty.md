---
description: 指定語音捕獲 DSP 是否執行麥克風陣列前置處理。
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983530"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="03f2f-103">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC 屬性</span><span class="sxs-lookup"><span data-stu-id="03f2f-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="03f2f-104">指定語音捕獲 DSP 是否執行麥克風陣列前置處理。</span><span class="sxs-lookup"><span data-stu-id="03f2f-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="03f2f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="03f2f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="03f2f-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="03f2f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="03f2f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="03f2f-107">Data Type</span></span>

<span data-ttu-id="03f2f-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="03f2f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="03f2f-109">預設值</span><span class="sxs-lookup"><span data-stu-id="03f2f-109">Default Value</span></span>

<span data-ttu-id="03f2f-110">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="03f2f-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="03f2f-111">套用至</span><span class="sxs-lookup"><span data-stu-id="03f2f-111">Applies To</span></span>

-   [<span data-ttu-id="03f2f-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="03f2f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="03f2f-113">備註</span><span class="sxs-lookup"><span data-stu-id="03f2f-113">Remarks</span></span>

<span data-ttu-id="03f2f-114">前置處理可以移除干擾處理的靜止聲音，例如具有固定音調的色調。</span><span class="sxs-lookup"><span data-stu-id="03f2f-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="03f2f-115">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="03f2f-115">This property can have the following values.</span></span>



| <span data-ttu-id="03f2f-116">值</span><span class="sxs-lookup"><span data-stu-id="03f2f-116">Value</span></span>          | <span data-ttu-id="03f2f-117">描述</span><span class="sxs-lookup"><span data-stu-id="03f2f-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="03f2f-118">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="03f2f-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="03f2f-119">停用前置處理。</span><span class="sxs-lookup"><span data-stu-id="03f2f-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="03f2f-120">VARIANT \_ TRUE</span><span class="sxs-lookup"><span data-stu-id="03f2f-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="03f2f-121">啟用前置處理。</span><span class="sxs-lookup"><span data-stu-id="03f2f-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="03f2f-122">這個屬性的預設值為 VARIANT \_ TRUE (enabled) 。</span><span class="sxs-lookup"><span data-stu-id="03f2f-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="03f2f-123">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="03f2f-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="03f2f-124">只有在啟用麥克風陣列處理時，DSP 才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="03f2f-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f2f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="03f2f-125">Requirements</span></span>



| <span data-ttu-id="03f2f-126">需求</span><span class="sxs-lookup"><span data-stu-id="03f2f-126">Requirement</span></span> | <span data-ttu-id="03f2f-127">值</span><span class="sxs-lookup"><span data-stu-id="03f2f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f2f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03f2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="03f2f-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03f2f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="03f2f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03f2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="03f2f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03f2f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="03f2f-132">標頭</span><span class="sxs-lookup"><span data-stu-id="03f2f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f2f-133"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="03f2f-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f2f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03f2f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f2f-135">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="03f2f-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="03f2f-136">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="03f2f-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
