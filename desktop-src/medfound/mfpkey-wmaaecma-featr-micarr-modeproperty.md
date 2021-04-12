---
description: 指定語音捕獲 DSP 如何執行麥克風陣列處理。
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: 'MFPKEY_WMAAECMA_FEATR_MICARR_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191791"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="ab7f1-103">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE 屬性</span><span class="sxs-lookup"><span data-stu-id="ab7f1-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="ab7f1-104">指定語音捕獲 DSP 如何執行麥克風陣列處理。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ab7f1-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="ab7f1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ab7f1-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ab7f1-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="ab7f1-107">Data Type</span></span>

<span data-ttu-id="ab7f1-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ab7f1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ab7f1-109">預設值</span><span class="sxs-lookup"><span data-stu-id="ab7f1-109">Default Value</span></span>

<span data-ttu-id="ab7f1-110">MICARRAY \_ 單一 \_ 橫樑</span><span class="sxs-lookup"><span data-stu-id="ab7f1-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="ab7f1-111">套用至</span><span class="sxs-lookup"><span data-stu-id="ab7f1-111">Applies To</span></span>

-   [<span data-ttu-id="ab7f1-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ab7f1-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="ab7f1-113">備註</span><span class="sxs-lookup"><span data-stu-id="ab7f1-113">Remarks</span></span>

<span data-ttu-id="ab7f1-114">這個屬性的值是 [MIC \_ 陣列 \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="ab7f1-115">預設值為 MICARRAY \_ 單一 \_ 橫樑。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="ab7f1-116">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="ab7f1-117">只有在啟用麥克風陣列處理時，DSP 才會使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="ab7f1-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7f1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab7f1-118">Requirements</span></span>



| <span data-ttu-id="ab7f1-119">需求</span><span class="sxs-lookup"><span data-stu-id="ab7f1-119">Requirement</span></span> | <span data-ttu-id="ab7f1-120">值</span><span class="sxs-lookup"><span data-stu-id="ab7f1-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7f1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab7f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7f1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7f1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ab7f1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab7f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7f1-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab7f1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab7f1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ab7f1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7f1-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7f1-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7f1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab7f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7f1-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ab7f1-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ab7f1-129">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="ab7f1-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
