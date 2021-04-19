---
description: 指定語音捕獲 DSP 執行的語音活動偵測類型。
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: 'MFPKEY_WMAAECMA_FEATR_VAD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997104"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="0d728-103">MFPKEY \_ WMAAECMA \_ FEATR \_ VAD 屬性</span><span class="sxs-lookup"><span data-stu-id="0d728-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="0d728-104">指定語音捕獲 DSP 執行的語音活動偵測類型。</span><span class="sxs-lookup"><span data-stu-id="0d728-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0d728-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="0d728-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0d728-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="0d728-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="0d728-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="0d728-107">Data Type</span></span>

<span data-ttu-id="0d728-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0d728-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0d728-109">預設值</span><span class="sxs-lookup"><span data-stu-id="0d728-109">Default Value</span></span>

<span data-ttu-id="0d728-110">0</span><span class="sxs-lookup"><span data-stu-id="0d728-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="0d728-111">套用至</span><span class="sxs-lookup"><span data-stu-id="0d728-111">Applies To</span></span>

-   [<span data-ttu-id="0d728-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="0d728-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="0d728-113">備註</span><span class="sxs-lookup"><span data-stu-id="0d728-113">Remarks</span></span>

<span data-ttu-id="0d728-114">這個屬性的值是 [AEC \_ VAD \_ 模式](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="0d728-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="0d728-115">語音活動偵測的輸出是從0到3的數位，為每個音訊畫面格計算。</span><span class="sxs-lookup"><span data-stu-id="0d728-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="0d728-116">DSP 會在每個音訊框架中的前兩個音訊樣本的最低位編碼結果。</span><span class="sxs-lookup"><span data-stu-id="0d728-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="0d728-117">值的意義取決於指定的模式。</span><span class="sxs-lookup"><span data-stu-id="0d728-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="0d728-118">下列程式碼示範如何從音訊資料中解壓縮結果。</span><span class="sxs-lookup"><span data-stu-id="0d728-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="0d728-119">在此範例中， *pOutput* 是輸出資料中音訊框架開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="0d728-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="0d728-120">這個屬性的預設值為 0 (停用) 。</span><span class="sxs-lookup"><span data-stu-id="0d728-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="0d728-121">設定此屬性之前，您必須將 [MFPKEY \_ WMAAECMA \_ 功能 \_ 模式](mfpkey-wmaaecma-feature-modeproperty.md) 屬性設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="0d728-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d728-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d728-122">Requirements</span></span>



| <span data-ttu-id="0d728-123">需求</span><span class="sxs-lookup"><span data-stu-id="0d728-123">Requirement</span></span> | <span data-ttu-id="0d728-124">值</span><span class="sxs-lookup"><span data-stu-id="0d728-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d728-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d728-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0d728-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d728-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d728-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d728-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0d728-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d728-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0d728-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0d728-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d728-130"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d728-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d728-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d728-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d728-132">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="0d728-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
