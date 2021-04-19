---
description: 指定語音捕獲 DSP 的麥克風陣列幾何。
ms.assetid: 1d91bdc8-5a09-487d-b45e-80d57a44cd0e
title: 'MFPKEY_WMAAECMA_MICARRAY_DESCPTR 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e433f50d9d7640575f1314c5acc13d7751fde0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981461"
---
# <a name="mfpkey_wmaaecma_micarray_descptr-property"></a><span data-ttu-id="9522a-103">MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR 屬性</span><span class="sxs-lookup"><span data-stu-id="9522a-103">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR Property</span></span>

<span data-ttu-id="9522a-104">指定語音捕獲 DSP 的麥克風陣列幾何。</span><span class="sxs-lookup"><span data-stu-id="9522a-104">Specifies the microphone array geometry for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9522a-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="9522a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9522a-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="9522a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9522a-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="9522a-107">Data Type</span></span>

<span data-ttu-id="9522a-108">VT \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="9522a-108">VT\_BLOB</span></span>

## <a name="applies-to"></a><span data-ttu-id="9522a-109">套用至</span><span class="sxs-lookup"><span data-stu-id="9522a-109">Applies To</span></span>

-   [<span data-ttu-id="9522a-110">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="9522a-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="9522a-111">備註</span><span class="sxs-lookup"><span data-stu-id="9522a-111">Remarks</span></span>

<span data-ttu-id="9522a-112">這個屬性的值是 [**KSAUDIO \_ MIC \_ 陣列 \_ 幾何**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) 結構。</span><span class="sxs-lookup"><span data-stu-id="9522a-112">The value of this property is a [**KSAUDIO\_MIC\_ARRAY\_GEOMETRY**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-ksaudio_mic_array_geometry) structure.</span></span> <span data-ttu-id="9522a-113">此結構是在標頭檔 KsMedia 中定義。</span><span class="sxs-lookup"><span data-stu-id="9522a-113">This structure is defined in the header file KsMedia.h.</span></span> <span data-ttu-id="9522a-114">若要取得麥克風陣列幾何，請 \_ \_ \_ \_ 在裝置上呼叫 **IKsControl：： KSPROPERTY** 方法，以查詢音訊裝置以取得 KSPROPERTY 音訊 MIC 陣列幾何屬性。</span><span class="sxs-lookup"><span data-stu-id="9522a-114">To get the microphone array geometry, query the audio device for the KSPROPERTY\_AUDIO\_MIC\_ARRAY\_GEOMETRY property by calling the **IKsControl::KSProperty** method on the device.</span></span> <span data-ttu-id="9522a-115">如需麥克風陣列的詳細資訊，請下載技術白皮書， [以瞭解如何建立和使用適用于 Windows Vista 的麥克風陣列](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)。</span><span class="sxs-lookup"><span data-stu-id="9522a-115">For more information on microphone arrays, download the white paper [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

<span data-ttu-id="9522a-116">如果您在篩選模式中使用 DSP，且已啟用麥克風陣列處理，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="9522a-116">Set this property if you are using the DSP in filter mode and microphone array processing is enabled.</span></span> <span data-ttu-id="9522a-117">如果您在來源模式中使用 DSP，DSP 會自動查詢裝置的幾何資訊。</span><span class="sxs-lookup"><span data-stu-id="9522a-117">If you are using the DSP in source mode, the DSP automatically queries the device for the geometry information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9522a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9522a-118">Requirements</span></span>



| <span data-ttu-id="9522a-119">需求</span><span class="sxs-lookup"><span data-stu-id="9522a-119">Requirement</span></span> | <span data-ttu-id="9522a-120">值</span><span class="sxs-lookup"><span data-stu-id="9522a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9522a-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9522a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9522a-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9522a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9522a-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9522a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9522a-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9522a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9522a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9522a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9522a-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="9522a-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9522a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9522a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9522a-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="9522a-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9522a-129">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="9522a-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
