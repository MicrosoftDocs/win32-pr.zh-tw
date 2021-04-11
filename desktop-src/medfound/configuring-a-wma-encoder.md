---
description: 設定 WMA 編碼器的輸出類型
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: 設定 WMA 編碼器的輸出類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111845"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="c322b-103">設定 WMA 編碼器的輸出類型</span><span class="sxs-lookup"><span data-stu-id="c322b-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="c322b-104">若要建立 Windows Media 音訊 (WMA) 編碼器的有效輸出類型，您必須擁有下列資訊：</span><span class="sxs-lookup"><span data-stu-id="c322b-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="c322b-105">Repesents 編碼之 WMA 格式的音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="c322b-106">請參閱 [音訊子類型 guid](audio-subtype-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="c322b-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="c322b-107">要在編碼器上設定的設定屬性。</span><span class="sxs-lookup"><span data-stu-id="c322b-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="c322b-108">設定屬性記載于 Windows Media 音訊和影片編解碼器和 DSP Api 檔中。</span><span class="sxs-lookup"><span data-stu-id="c322b-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="c322b-109">如需詳細資訊，請參閱 [編碼屬性](configuring-the-encoder.md)中的「音訊串流屬性」。</span><span class="sxs-lookup"><span data-stu-id="c322b-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="c322b-110">Windows Vista 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c322b-110">Windows Vista or Later</span></span>

<span data-ttu-id="c322b-111">若要取得編碼器的有效輸出型別，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="c322b-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="c322b-112">使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來建立編碼器的實例。</span><span class="sxs-lookup"><span data-stu-id="c322b-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="c322b-113">查詢編碼器以取得 **IPropertyStore** 介面。</span><span class="sxs-lookup"><span data-stu-id="c322b-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="c322b-114">使用 **IPropertyStore** 介面設定編碼器。</span><span class="sxs-lookup"><span data-stu-id="c322b-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="c322b-115">藉由在迴圈中呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取出支援的輸出類型，直到編碼器傳回 **MF \_ E \_ NO \_ 其他 \_ 類型** ，而且您選擇目標媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="c322b-116">I</span><span class="sxs-lookup"><span data-stu-id="c322b-116">I</span></span>
5.  <span data-ttu-id="c322b-117">呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="c322b-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c322b-118">Windows 7</span></span>

<span data-ttu-id="c322b-119">若要在 Windows 7 中取得編碼器的有效輸出類型，媒體基礎提供 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 函數。</span><span class="sxs-lookup"><span data-stu-id="c322b-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="c322b-120">應用程式必須通過 repesents 編碼的 WMA 和編碼屬性所需的音訊子類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="c322b-121">這些屬性是必要的，因為編碼器會根據設定的模式變更支援的輸出類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="c322b-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)僅支援 [常數位速率編碼](constant-bit-rate-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="c322b-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="c322b-123">如果呼叫成功，應用程式會接收 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) 物件中所支援之輸出媒體類型的 IUnknown 指標清單。</span><span class="sxs-lookup"><span data-stu-id="c322b-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="c322b-124">若要設定輸出媒體類型，請尋找符合您目標型別的類型，然後呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c322b-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c322b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="c322b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c322b-126">具現化編碼器 MFT</span><span class="sxs-lookup"><span data-stu-id="c322b-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="c322b-127">Windows Media 編碼器</span><span class="sxs-lookup"><span data-stu-id="c322b-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



