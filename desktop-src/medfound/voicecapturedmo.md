---
description: 封裝與語音捕捉相關之多個 Dsp 的物件。
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: '語音捕捉 DSP (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692291"
---
# <a name="voice-capture-dsp"></a><span data-ttu-id="b5a4f-103">語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="b5a4f-103">Voice Capture DSP</span></span>

<span data-ttu-id="b5a4f-104">封裝與語音捕捉相關之多個 Dsp 的物件。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-104">An object that encapsulates several DSPs related to voice capture.</span></span>

## <a name="clsid"></a><span data-ttu-id="b5a4f-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5a4f-105">CLSID</span></span>

<span data-ttu-id="b5a4f-106">CLSID \_ CWMAudioAEC</span><span class="sxs-lookup"><span data-stu-id="b5a4f-106">CLSID\_CWMAudioAEC</span></span>

## <a name="interfaces"></a><span data-ttu-id="b5a4f-107">介面</span><span class="sxs-lookup"><span data-stu-id="b5a4f-107">Interfaces</span></span>

-   [<span data-ttu-id="b5a4f-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="b5a4f-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   <span data-ttu-id="b5a4f-109">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="b5a4f-109">**IPropertyStore**</span></span>

## <a name="properties"></a><span data-ttu-id="b5a4f-110">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a4f-110">Properties</span></span>



| <span data-ttu-id="b5a4f-111">屬性</span><span class="sxs-lookup"><span data-stu-id="b5a4f-111">Property</span></span>                                                                                     | <span data-ttu-id="b5a4f-112">描述</span><span class="sxs-lookup"><span data-stu-id="b5a4f-112">Description</span></span>                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5a4f-113">MFPKEY \_ WMAAECMA \_ 裝置 \_ 索引</span><span class="sxs-lookup"><span data-stu-id="b5a4f-113">MFPKEY\_WMAAECMA\_DEVICE\_INDEXES</span></span>](mfpkey-wmaaecma-device-indexesproperty.md)              | <span data-ttu-id="b5a4f-114">指定用來捕捉和轉譯音訊的 SQL-DMO 音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-114">Specifies which audio devices the DMO uses for capturing and rendering audio.</span></span>                     |
| [<span data-ttu-id="b5a4f-115">MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID</span><span class="sxs-lookup"><span data-stu-id="b5a4f-115">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID</span></span>](mfpkey-wmaaecma-devicepair-guidproperty.md)            | <span data-ttu-id="b5a4f-116">識別應用程式目前使用的音訊裝置組合。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-116">Identifies the combination of audio devices that the application is currently using.</span></span>              |
| [<span data-ttu-id="b5a4f-117">MFPKEY \_ WMAAECMA \_ SQL-DMO \_ 來源 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="b5a4f-117">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE</span></span>](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | <span data-ttu-id="b5a4f-118">指定是使用來源模式或篩選模式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-118">Specifies whether the DMO uses source mode or filter mode.</span></span>                                        |
| [<span data-ttu-id="b5a4f-119">MFPKEY \_ WMAAECMA \_ FEATR \_ AES</span><span class="sxs-lookup"><span data-stu-id="b5a4f-119">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)                        | <span data-ttu-id="b5a4f-120">指定當您在剩餘的信號上 (AES) 執行聲場 echo 抑制的次數。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-120">Specifies how many times the DMO performs acoustic echo suppression (AES) on the residual signal.</span></span> |
| [<span data-ttu-id="b5a4f-121">MFPKEY \_ WMAAECMA \_ FEATR \_ AGC</span><span class="sxs-lookup"><span data-stu-id="b5a4f-121">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)                        | <span data-ttu-id="b5a4f-122">指定，是否執行自動增益控制項。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-122">Specifies whether the DMO performs automatic gain control.</span></span>                                        |
| [<span data-ttu-id="b5a4f-123">MFPKEY \_ WMAAECMA \_ FEATR \_ 中心 \_ 剪輯</span><span class="sxs-lookup"><span data-stu-id="b5a4f-123">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)       | <span data-ttu-id="b5a4f-124">指定，是否執行中心裁剪。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-124">Specifies whether the DMO performs center clipping.</span></span>                                               |
| [<span data-ttu-id="b5a4f-125">MFPKEY \_ WMAAECMA \_ FEATR \_ ECHO \_ LENGTH</span><span class="sxs-lookup"><span data-stu-id="b5a4f-125">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | <span data-ttu-id="b5a4f-126">指定聲場 echo 取消 (AEC) 演算法可以處理的回應持續時間。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-126">Specifies the duration of echo that the acoustic echo cancellation (AEC) algorithm can handle.</span></span>    |
| [<span data-ttu-id="b5a4f-127">MFPKEY \_ WMAAECMA \_ FEATR \_ 畫面格 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="b5a4f-127">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | <span data-ttu-id="b5a4f-128">指定音訊框架大小。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-128">Specifies the audio frame size.</span></span>                                                                   |
| [<span data-ttu-id="b5a4f-129">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 橫樑</span><span class="sxs-lookup"><span data-stu-id="b5a4f-129">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM</span></span>](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | <span data-ttu-id="b5a4f-130">指定用來處理麥克風陣列的橫樑。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-130">Specifies which beam the DMO uses for microphone array processing.</span></span>                                |
| [<span data-ttu-id="b5a4f-131">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ 模式</span><span class="sxs-lookup"><span data-stu-id="b5a4f-131">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | <span data-ttu-id="b5a4f-132">指定 SQL-DMO 執行麥克風陣列處理的方式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-132">Specifies how the DMO performs microphone array processing.</span></span>                                       |
| [<span data-ttu-id="b5a4f-133">MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC</span><span class="sxs-lookup"><span data-stu-id="b5a4f-133">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | <span data-ttu-id="b5a4f-134">指定，是否執行麥克風陣列前置處理。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-134">Specifies whether the DMO performs microphone array preprocessing.</span></span>                                |
| [<span data-ttu-id="b5a4f-135">MFPKEY \_ WMAAECMA \_ FEATR \_ 雜訊 \_ 填滿</span><span class="sxs-lookup"><span data-stu-id="b5a4f-135">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | <span data-ttu-id="b5a4f-136">指定，是否執行雜訊填滿。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-136">Specifies whether the DMO performs noise filling.</span></span>                                                 |
| [<span data-ttu-id="b5a4f-137">MFPKEY \_ WMAAECMA \_ FEATR \_ NS</span><span class="sxs-lookup"><span data-stu-id="b5a4f-137">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)                          | <span data-ttu-id="b5a4f-138">指定是否執行雜訊隱藏。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-138">Specifies whether the DMO performs noise suppression.</span></span>                                             |
| [<span data-ttu-id="b5a4f-139">MFPKEY \_ WMAAECMA \_ FEATR \_ VAD</span><span class="sxs-lookup"><span data-stu-id="b5a4f-139">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)                        | <span data-ttu-id="b5a4f-140">指定由的語音活動偵測類型。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-140">Specifies the type of voice activity detection that the DMO performs.</span></span>                             |
| [<span data-ttu-id="b5a4f-141">MFPKEY \_ WMAAECMA \_ 功能 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="b5a4f-141">MFPKEY\_WMAAECMA\_FEATURE\_MODE</span></span>](mfpkey-wmaaecma-feature-modeproperty.md)                  | <span data-ttu-id="b5a4f-142">讓應用程式覆寫各種屬性的預設設定。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-142">Enables the application to override the default settings on various properties.</span></span>                   |
| [<span data-ttu-id="b5a4f-143">MFPKEY \_ WMAAECMA \_ MIC \_ 增益 \_ BOUNDER</span><span class="sxs-lookup"><span data-stu-id="b5a4f-143">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER</span></span>](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | <span data-ttu-id="b5a4f-144">指定是否套用麥克風增益周框。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-144">Specifies whether the DMO applies microphone gain bounding.</span></span>                                       |
| [<span data-ttu-id="b5a4f-145">MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR</span><span class="sxs-lookup"><span data-stu-id="b5a4f-145">MFPKEY\_WMAAECMA\_MICARRAY\_DESCPTR</span></span>](mfpkey-wmaaecma-micarray-descptrproperty.md)          | <span data-ttu-id="b5a4f-146">指定麥克風陣列幾何。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-146">Specifies the microphone array geometry.</span></span>                                                          |
| [<span data-ttu-id="b5a4f-147">MFPKEY \_ WMAAECMA \_ 品質 \_ 計量</span><span class="sxs-lookup"><span data-stu-id="b5a4f-147">MFPKEY\_WMAAECMA\_QUALITY\_METRICS</span></span>](mfpkey-wmaaecma-quality-metricsproperty.md)            | <span data-ttu-id="b5a4f-148">取得 AEC 的品質計量。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-148">Retrieves quality metrics for AEC.</span></span>                                                                |
| [<span data-ttu-id="b5a4f-149">MFPKEY \_ WMAAECMA \_ 取得 \_ TS \_ 統計資料</span><span class="sxs-lookup"><span data-stu-id="b5a4f-149">MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS</span></span>](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | <span data-ttu-id="b5a4f-150">指定是否將時間戳記統計資料儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-150">Specifies whether the DMO stores time stamp statistics in the registry.</span></span>                           |
| [<span data-ttu-id="b5a4f-151">MFPKEY \_ WMAAECMA \_ 系統 \_ 模式</span><span class="sxs-lookup"><span data-stu-id="b5a4f-151">MFPKEY\_WMAAECMA\_SYSTEM\_MODE</span></span>](mfpkey-wmaaecma-system-modeproperty.md)                    | <span data-ttu-id="b5a4f-152">設定處理模式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-152">Sets the processing mode.</span></span>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="b5a4f-153">備註</span><span class="sxs-lookup"><span data-stu-id="b5a4f-153">Remarks</span></span>

<span data-ttu-id="b5a4f-154">與其他 Dsp 不同的是，語音捕捉物件會將多個 Dsp 封裝在單一物件中，而物件只是一種物件， (不會執行 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)) 。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-154">Unlike the other DSPs, the voice capture object encapsulates multiple DSPs in a single object, and the object is a DMO object only (it does not implement [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)).</span></span> <span data-ttu-id="b5a4f-155">語音捕獲中包含下列 DSP 元件：</span><span class="sxs-lookup"><span data-stu-id="b5a4f-155">The voice capture DMO includes the following DSP components:</span></span>

-   <span data-ttu-id="b5a4f-156">聲場 echo 取消 (AEC) </span><span class="sxs-lookup"><span data-stu-id="b5a4f-156">Acoustic echo cancellation (AEC)</span></span>
-   <span data-ttu-id="b5a4f-157">麥克風陣列處理</span><span class="sxs-lookup"><span data-stu-id="b5a4f-157">Microphone array processing</span></span>
-   <span data-ttu-id="b5a4f-158">雜訊隱藏</span><span class="sxs-lookup"><span data-stu-id="b5a4f-158">Noise suppression</span></span>
-   <span data-ttu-id="b5a4f-159">自動增益控制</span><span class="sxs-lookup"><span data-stu-id="b5a4f-159">Automatic gain control</span></span>
-   <span data-ttu-id="b5a4f-160">語音活動偵測</span><span class="sxs-lookup"><span data-stu-id="b5a4f-160">Voice activity detection</span></span>

<span data-ttu-id="b5a4f-161">應用程式可以個別開啟和關閉每個元件。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-161">Applications can turn each component on and off individually.</span></span>

<span data-ttu-id="b5a4f-162">語音捕獲（voice capture）支援兩種作業模式： *篩選* 模式和 *來源* 模式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-162">The voice capture DMO supports two modes of operation, *filter* mode and *source* mode.</span></span> <span data-ttu-id="b5a4f-163">在篩選模式中，應用程式會從麥克風和說話者將音訊樣本傳送至，並產生輸出。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-163">In filter mode, the application sends audio samples from the microphone and from the speaker line to the DMO, and the DMO produces output.</span></span>

<span data-ttu-id="b5a4f-164">在來源模式中，應用程式不需要將範例傳遞給 SQL-DMO。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-164">In source mode, the application does not need to deliver samples to the DMO.</span></span> <span data-ttu-id="b5a4f-165">取而代之的是，一來管理音訊裝置上的所有作業，包括初始化裝置、捕獲和同步處理音訊串流、計算時間戳記，以及取得麥克風陣列的幾何。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-165">Instead, the DMO manages all of the operations on the audio devices, including initializing the devices, capturing and synchronizing the audio streams, calculating time stamps, and retrieving the geometry of the microphone array.</span></span> <span data-ttu-id="b5a4f-166">使用來源模式時，應用程式只會設定 SQL-DMO，而來自的輸出是乾淨且經過處理的麥克風信號。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-166">Using source mode, the application simply configures the DMO, and the output from the DMO is a clean, processed microphone signal.</span></span> <span data-ttu-id="b5a4f-167">來源模式比篩選模式更容易使用，而且建議用於大部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-167">Source mode is significantly easier to use than filter mode, and is recommended for most applications.</span></span>

<span data-ttu-id="b5a4f-168">目前，語音捕獲僅支援單聲道的聲場 echo 取消 (AEC) ，因此喇叭線的輸出必須是單一通道。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-168">Currently the voice capture DMO supports only single-channel acoustic echo cancellation (AEC), so the output from the speaker line must be single-channel.</span></span> <span data-ttu-id="b5a4f-169">如果已停用麥克風陣列處理，多重通道輸入會折迭至一個通道以進行 AEC 處理。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-169">If microphone array processing is disabled, multi-channel input is folded down to one channel for AEC processing.</span></span> <span data-ttu-id="b5a4f-170">如果麥克風陣列處理和 AEC 處理都已啟用，則會在麥克風陣列處理之前，在每個麥克風元素上執行 AEC。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-170">If both microphone array processing and AEC processing are enabled, AEC is performed on each microphone element before microphone array processing.</span></span>

### <a name="microphone-array-processing"></a><span data-ttu-id="b5a4f-171">麥克風陣列處理</span><span class="sxs-lookup"><span data-stu-id="b5a4f-171">Microphone Array Processing</span></span>

<span data-ttu-id="b5a4f-172">麥克風陣列是一組緊密定位的麥克風。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-172">A microphone array is a set of closely positioned microphones.</span></span> <span data-ttu-id="b5a4f-173">麥克風陣列的方向比單一麥克風更好，因為聲場會以稍微不同的時間抵達每個麥克風。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-173">Microphone arrays achieve better directionality than a single microphone, because the acoustic waves arrive at each microphone at a slightly different time.</span></span> <span data-ttu-id="b5a4f-174">如需麥克風陣列的詳細資訊，請參閱 [Windows vista 中的 web 文章麥克風陣列支援](/windows-hardware/design/component-guidelines/audio) ，以及 [如何建立和使用適用于 Windows vista 的麥克風](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format)陣列。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-174">For more information on microphone arrays see the web articles [Microphone Array Support in Windows Vista](/windows-hardware/design/component-guidelines/audio) and [How to Build and Use Microphone Arrays for Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).</span></span>

### <a name="using-the-voice-capture-dsp"></a><span data-ttu-id="b5a4f-175">使用語音捕獲 DSP</span><span class="sxs-lookup"><span data-stu-id="b5a4f-175">Using the Voice Capture DSP</span></span>

<span data-ttu-id="b5a4f-176">若要使用語音捕獲 DSP，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-176">To use the Voice Capture DSP, perform the following steps.</span></span>

### <a name="1-initialize-the-dmo"></a><span data-ttu-id="b5a4f-177">1. 初始化 SQL-DMO</span><span class="sxs-lookup"><span data-stu-id="b5a4f-177">1. Initialize the DMO</span></span>

<span data-ttu-id="b5a4f-178">使用 CLSID **clsid \_ CWMAudioAEC** 呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立語音捕獲。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-178">Create the voice capture DMO by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the CLSID **CLSID\_CWMAudioAEC**.</span></span> <span data-ttu-id="b5a4f-179">語音捕獲 DSDP 只會公開 [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) 和 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面，因此只能用來做為。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-179">The voice capture DSDP exposes only the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) and [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces, so it can only be used as a DMO.</span></span>

<span data-ttu-id="b5a4f-180">的預設值為來源模式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-180">The DMO defaults to source mode.</span></span> <span data-ttu-id="b5a4f-181">若要選取篩選模式，請將 [MFPKEY \_ WMAAECMA \_ sql-dmo \_ 來源 \_ 模式](mfpkey-wmaaecma-dmo-source-modeproperty.md) 屬性設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-181">To select filter mode, set the [MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md) property to **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="b5a4f-182">接下來，使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面設定 sql-dmo 的內部屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-182">Next, configure the internal properties of the DMO by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span> <span data-ttu-id="b5a4f-183">應用程式必須設定的唯一屬性是 [ [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式]](mfpkey-wmaaecma-system-modeproperty.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-183">The only property that an application must set is the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property.</span></span> <span data-ttu-id="b5a4f-184">這個屬性會設定在中的處理管線。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-184">This property configures the processing pipeline within the DMO.</span></span> <span data-ttu-id="b5a4f-185">其他屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-185">The other properties are optional.</span></span>

### <a name="2-set-the-input-and-output-formats"></a><span data-ttu-id="b5a4f-186">2. 設定輸入和輸出格式</span><span class="sxs-lookup"><span data-stu-id="b5a4f-186">2. Set the Input and Output Formats</span></span>

<span data-ttu-id="b5a4f-187">如果您在篩選模式中使用 SQL-DMO，請呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype)來設定輸入格式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-187">If you are using the DMO in filter mode, set the input format by calling [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype).</span></span> <span data-ttu-id="b5a4f-188">輸入格式幾乎可以是任何有效的未壓縮 PCM 或 IEEE 浮點音訊類型。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-188">The input format can be almost any valid uncompressed PCM or IEEE floating-point audio type.</span></span> <span data-ttu-id="b5a4f-189">如果輸入格式不符合輸出格式，則會自動執行取樣速率轉換。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-189">If the input format does not match the output format, the DMO automatically performs sample-rate conversion.</span></span>

<span data-ttu-id="b5a4f-190">如果您在來源模式中使用的是，請勿設定輸入格式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-190">If you are using the DMO in source mode, do not set the input format.</span></span> <span data-ttu-id="b5a4f-191">SQL-DMO 會根據音訊裝置自動設定輸入格式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-191">The DMO automatically configures the input format based on the audio devices.</span></span>

<span data-ttu-id="b5a4f-192">在任一種模式中，藉由呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)來設定輸出格式。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-192">In either mode, set the output format by calling [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype).</span></span> <span data-ttu-id="b5a4f-193">SQL-DMO 可以接受下列輸出格式：</span><span class="sxs-lookup"><span data-stu-id="b5a4f-193">The DMO can accept the following output formats:</span></span>

-   <span data-ttu-id="b5a4f-194">子類型： **MEDIASUBTYPE \_ PCM** 或 **MEDIASUBTYPE \_ IEEE \_ FLOAT**</span><span class="sxs-lookup"><span data-stu-id="b5a4f-194">Subtype: **MEDIASUBTYPE\_PCM** or **MEDIASUBTYPE\_IEEE\_FLOAT**</span></span>
-   <span data-ttu-id="b5a4f-195">格式區塊： [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) 或 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b5a4f-195">Format block: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) or [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span>
-   <span data-ttu-id="b5a4f-196">每秒樣本數： 8000;11025;16000;或22050</span><span class="sxs-lookup"><span data-stu-id="b5a4f-196">Samples per second: 8,000; 11,025; 16,000; or 22,050</span></span>
-   <span data-ttu-id="b5a4f-197">通道：1表示僅限 AEC 模式，2或4表示麥克風陣列處理</span><span class="sxs-lookup"><span data-stu-id="b5a4f-197">Channels: 1 for AEC-only mode, 2 or 4 for microphone array processing</span></span>
-   <span data-ttu-id="b5a4f-198">每個樣本位數：16</span><span class="sxs-lookup"><span data-stu-id="b5a4f-198">Bits per sample: 16</span></span>

<span data-ttu-id="b5a4f-199">下列程式碼會將輸出型別設定為16位單一通道 PCM 音訊：</span><span class="sxs-lookup"><span data-stu-id="b5a4f-199">The following code sets the output type to 16-bit single-channel PCM audio:</span></span>


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a><span data-ttu-id="b5a4f-200">3. 處理資料</span><span class="sxs-lookup"><span data-stu-id="b5a4f-200">3. Process Data</span></span>

<span data-ttu-id="b5a4f-201">在處理任何資料之前，建議您呼叫 [**IMediaObject：： AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources)。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-201">Before processing any data, it is recommended to call [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources).</span></span> <span data-ttu-id="b5a4f-202">這個方法會配置用來在內部使用的資源。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-202">This method allocates the resources used internally by the DMO.</span></span> <span data-ttu-id="b5a4f-203">在先前所列的步驟之後（而非之前）呼叫 **AllocateStreamingResources** 。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-203">Call **AllocateStreamingResources** after the steps listed previously, not before.</span></span> <span data-ttu-id="b5a4f-204">如果您沒有呼叫這個方法，則會在資料處理開始時自動設定資源。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-204">If you do not call this method, the DMO automatically allocates resources when data processing starts.</span></span>

<span data-ttu-id="b5a4f-205">如果您在篩選模式中使用 SQL-DMO，則必須呼叫 [**IMediaObject：:P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput)，將輸入資料傳遞給：</span><span class="sxs-lookup"><span data-stu-id="b5a4f-205">If you are using the DMO in filter mode, you must pass input data to the DMO by calling [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput).</span></span> <span data-ttu-id="b5a4f-206">來自麥克風的音訊資料會進入串流0，而喇叭線的音訊資料則會移至串流1。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-206">The audio data from the microphone goes to stream 0, and the audio data from the speaker line goes to stream 1.</span></span> <span data-ttu-id="b5a4f-207">如果您在來源模式中使用的是，就不需要呼叫 **ProcessInput**。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-207">If you are using the DMO in source mode, you do not need to call **ProcessInput**.</span></span>

<span data-ttu-id="b5a4f-208">若要從 DSP 取得輸出資料，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b5a4f-208">To get output data from the DSP, perform the following steps:</span></span>

1.  <span data-ttu-id="b5a4f-209">建立緩衝區物件以保存輸出資料。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-209">Create a buffer object to hold the output data.</span></span> <span data-ttu-id="b5a4f-210">緩衝區物件必須執行 [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-210">The buffer object must implement the [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) interface.</span></span> <span data-ttu-id="b5a4f-211">緩衝區的大小取決於您的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-211">The size of the buffer depends on the requirements of your application.</span></span> <span data-ttu-id="b5a4f-212">配置較大的緩衝區可減少發生問題的機會。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-212">Allocating a larger buffer can reduce the chances of glitches occurring.</span></span>
2.  <span data-ttu-id="b5a4f-213">宣告 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) 結構，並設定 **pBuffer** 成員以指向您的緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-213">Declare a [**DMO\_OUTPUT\_DATA\_BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) structure and set the **pBuffer** member to point to your buffer object.</span></span>
3.  <span data-ttu-id="b5a4f-214">將 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) 結構傳遞至 [**IMediaObject：:P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) 方法。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-214">Pass the [**DMO\_OUTPUT\_DATA\_BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) structure to the [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) method.</span></span>
4.  <span data-ttu-id="b5a4f-215">只要每個值都有輸出資料，繼續呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-215">Continue to call this method for as long as the DMO has output data.</span></span> <span data-ttu-id="b5a4f-216">DSP 會在 [**Sql-dmo \_ 輸出 \_ 資料 \_ 緩衝區**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)結構的 **dwStatus** 成員中設定 [ **sql-dmo \_ 輸出 \_ 資料 \_ BUFFERF \_ 未完成**] 旗標，以表示它有更多輸出。</span><span class="sxs-lookup"><span data-stu-id="b5a4f-216">The DSP signals that it has more output by setting the **DMO\_OUTPUT\_DATA\_BUFFERF\_INCOMPLETE** flag in the **dwStatus** member of the [**DMO\_OUTPUT\_DATA\_BUFFER**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a4f-217">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5a4f-217">Requirements</span></span>



| <span data-ttu-id="b5a4f-218">需求</span><span class="sxs-lookup"><span data-stu-id="b5a4f-218">Requirement</span></span> | <span data-ttu-id="b5a4f-219">值</span><span class="sxs-lookup"><span data-stu-id="b5a4f-219">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5a4f-220">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5a4f-220">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a4f-221">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5a4f-221">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b5a4f-222">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5a4f-222">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a4f-223">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5a4f-223">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b5a4f-224">標頭</span><span class="sxs-lookup"><span data-stu-id="b5a4f-224">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a4f-225"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a4f-225"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b5a4f-226">DLL</span><span class="sxs-lookup"><span data-stu-id="b5a4f-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5a4f-227"><dt>Mfwmaaec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5a4f-227"><dt>Mfwmaaec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a4f-228">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5a4f-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a4f-229">數位訊號處理器</span><span class="sxs-lookup"><span data-stu-id="b5a4f-229">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
