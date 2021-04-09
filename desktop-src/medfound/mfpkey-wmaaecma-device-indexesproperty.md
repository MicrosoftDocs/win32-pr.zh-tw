---
description: 指定語音捕獲 DSP 用來捕捉和呈現音訊的音訊裝置。
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: 'MFPKEY_WMAAECMA_DEVICE_INDEXES 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848451"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a><span data-ttu-id="13d57-103">MFPKEY \_ WMAAECMA \_ 裝置 \_ 索引屬性</span><span class="sxs-lookup"><span data-stu-id="13d57-103">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES Property</span></span>

<span data-ttu-id="13d57-104">指定語音捕獲 DSP 用來捕捉和呈現音訊的音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="13d57-104">Specifies which audio devices the Voice Capture DSP uses for capturing and rendering audio.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="13d57-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="13d57-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="13d57-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="13d57-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="13d57-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="13d57-107">Data Type</span></span>

<span data-ttu-id="13d57-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="13d57-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="13d57-109">預設值</span><span class="sxs-lookup"><span data-stu-id="13d57-109">Default Value</span></span>

<span data-ttu-id="13d57-110"> (-1，-1) 。</span><span class="sxs-lookup"><span data-stu-id="13d57-110">(-1, -1).</span></span>

## <a name="applies-to"></a><span data-ttu-id="13d57-111">套用至</span><span class="sxs-lookup"><span data-stu-id="13d57-111">Applies To</span></span>

-   [<span data-ttu-id="13d57-112">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="13d57-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="13d57-113">備註</span><span class="sxs-lookup"><span data-stu-id="13d57-113">Remarks</span></span>

<span data-ttu-id="13d57-114">如果您在來源模式中使用 DSP，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="13d57-114">Set this property if you are using the DSP in source mode.</span></span> <span data-ttu-id="13d57-115">DSP 會忽略篩選模式中的這個屬性。</span><span class="sxs-lookup"><span data-stu-id="13d57-115">The DSP ignores this property in filter mode.</span></span>

<span data-ttu-id="13d57-116">屬性的值是封裝成 **DWORD** 的 2 16 位 **字** 組。</span><span class="sxs-lookup"><span data-stu-id="13d57-116">The value of the property is two 16-bit **WORD** s packed into a **DWORD**.</span></span> <span data-ttu-id="13d57-117">上層16位指定音訊轉譯裝置 (通常是喇叭) ，而較低的16位則指定的捕獲裝置 (通常是麥克風) 。</span><span class="sxs-lookup"><span data-stu-id="13d57-117">The upper 16 bits specify the audio rendering device (typically a speaker), and the lower 16 bits specify the capture device (typically a microphone).</span></span> <span data-ttu-id="13d57-118">每個裝置都指定為音訊裝置集合的索引。</span><span class="sxs-lookup"><span data-stu-id="13d57-118">Each device is specified as an index into the audio device collection.</span></span> <span data-ttu-id="13d57-119">如果索引為-1，則會使用預設裝置。</span><span class="sxs-lookup"><span data-stu-id="13d57-119">If the index is -1, the default device is used.</span></span>

<span data-ttu-id="13d57-120">裝置索引會對應至 [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) 介面中所使用的集合索引。</span><span class="sxs-lookup"><span data-stu-id="13d57-120">The device index corresponds to the collection index used in the [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) interface.</span></span> <span data-ttu-id="13d57-121">應用程式必須透過選取的轉譯裝置來播放最遠的聲音。</span><span class="sxs-lookup"><span data-stu-id="13d57-121">The application must play the far-end voice through the selected rendering device.</span></span> <span data-ttu-id="13d57-122"> (最遠的聲音是電話線另一端的人心聲，會透過使用者電腦上的喇叭播放 ) 。如果選取的轉譯裝置沒有作用中的串流，則 DSP 無法處理任何輸出。</span><span class="sxs-lookup"><span data-stu-id="13d57-122">(The far-end voice is the voice of the person on the other end of the telephone line, which is played through the speaker on the user's computer.) If the selected rendering device does not have an active stream, the DSP cannot process any output.</span></span>

<span data-ttu-id="13d57-123">這個屬性的預設值是 (-1，-1) 。</span><span class="sxs-lookup"><span data-stu-id="13d57-123">The default value of this property is (-1, -1).</span></span>

<span data-ttu-id="13d57-124">下列範例示範如何初始化這個屬性的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="13d57-124">The following example shows how to initialize the **PROPVARIANT** for this property.</span></span>


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a><span data-ttu-id="13d57-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="13d57-125">Requirements</span></span>



| <span data-ttu-id="13d57-126">需求</span><span class="sxs-lookup"><span data-stu-id="13d57-126">Requirement</span></span> | <span data-ttu-id="13d57-127">值</span><span class="sxs-lookup"><span data-stu-id="13d57-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13d57-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13d57-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13d57-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13d57-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="13d57-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13d57-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13d57-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13d57-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13d57-132">標頭</span><span class="sxs-lookup"><span data-stu-id="13d57-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="13d57-133"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="13d57-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d57-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13d57-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d57-135">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="13d57-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="13d57-136">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="13d57-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
