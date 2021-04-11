---
description: 讓應用程式覆寫語音捕獲 DSP 之各種屬性的預設設定。
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: 'MFPKEY_WMAAECMA_FEATURE_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691656"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a><span data-ttu-id="c18d5-103">MFPKEY \_ WMAAECMA \_ 功能 \_ 模式屬性</span><span class="sxs-lookup"><span data-stu-id="c18d5-103">MFPKEY\_WMAAECMA\_FEATURE\_MODE Property</span></span>

<span data-ttu-id="c18d5-104">讓應用程式覆寫語音捕獲 DSP 之各種屬性的預設設定。</span><span class="sxs-lookup"><span data-stu-id="c18d5-104">Enables the application to override the default settings on various properties of the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c18d5-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="c18d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c18d5-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="c18d5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c18d5-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="c18d5-107">Data Type</span></span>

<span data-ttu-id="c18d5-108">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="c18d5-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="c18d5-109">預設值</span><span class="sxs-lookup"><span data-stu-id="c18d5-109">Default Value</span></span>

<span data-ttu-id="c18d5-110">VARIANT \_ FALSE</span><span class="sxs-lookup"><span data-stu-id="c18d5-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="c18d5-111">套用至</span><span class="sxs-lookup"><span data-stu-id="c18d5-111">Applies To</span></span>

-   [<span data-ttu-id="c18d5-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="c18d5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="c18d5-113">備註</span><span class="sxs-lookup"><span data-stu-id="c18d5-113">Remarks</span></span>

<span data-ttu-id="c18d5-114">如果此屬性為 VARIANT \_ TRUE，則應用程式可以在 DSP 上設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="c18d5-114">If this property is VARIANT\_TRUE, the application can set the following properties on the DSP:</span></span>

-   [<span data-ttu-id="c18d5-115">MFPKEY \_ WMAAECMA \_ FEATR \_ AES</span><span class="sxs-lookup"><span data-stu-id="c18d5-115">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)
-   [<span data-ttu-id="c18d5-116">MFPKEY \_ WMAAECMA \_ FEATR \_ AGC</span><span class="sxs-lookup"><span data-stu-id="c18d5-116">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)
-   [<span data-ttu-id="c18d5-117">MFPKEY \_ WMAAECMA \_ FEATR \_ 中心 \_ 剪輯</span><span class="sxs-lookup"><span data-stu-id="c18d5-117">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [<span data-ttu-id="c18d5-118">MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH</span><span class="sxs-lookup"><span data-stu-id="c18d5-118">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [<span data-ttu-id="c18d5-119">MFPKEY \_ WMAAECMA \_ FEATR \_ 畫面格 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="c18d5-119">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [<span data-ttu-id="c18d5-120">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式</span><span class="sxs-lookup"><span data-stu-id="c18d5-120">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [<span data-ttu-id="c18d5-121">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC</span><span class="sxs-lookup"><span data-stu-id="c18d5-121">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [<span data-ttu-id="c18d5-122">MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="c18d5-122">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [<span data-ttu-id="c18d5-123">MFPKEY \_ WMAAECMA \_ FEATR \_ NS</span><span class="sxs-lookup"><span data-stu-id="c18d5-123">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)
-   [<span data-ttu-id="c18d5-124">MFPKEY \_ WMAAECMA \_ FEATR \_ VAD</span><span class="sxs-lookup"><span data-stu-id="c18d5-124">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)

<span data-ttu-id="c18d5-125">如果此屬性為 VARIANT \_ FALSE，則 DSP 會忽略這些屬性，並使用其預設設定。</span><span class="sxs-lookup"><span data-stu-id="c18d5-125">If this property is VARIANT\_FALSE, the DSP ignores these properties and uses its default settings.</span></span> <span data-ttu-id="c18d5-126">這個屬性的預設值為 VARIANT \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="c18d5-126">The default value of this property is VARIANT\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="c18d5-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c18d5-127">Requirements</span></span>



| <span data-ttu-id="c18d5-128">需求</span><span class="sxs-lookup"><span data-stu-id="c18d5-128">Requirement</span></span> | <span data-ttu-id="c18d5-129">值</span><span class="sxs-lookup"><span data-stu-id="c18d5-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c18d5-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c18d5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c18d5-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c18d5-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c18d5-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c18d5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c18d5-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c18d5-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c18d5-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c18d5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c18d5-135"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="c18d5-135"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c18d5-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c18d5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c18d5-137">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="c18d5-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c18d5-138">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="c18d5-138">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
