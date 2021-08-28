---
description: 設定影片編碼
ms.assetid: 917600f5-5580-4ca5-bce9-70eadec40df7
title: '設定影片編碼 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c6cb95a0bbe13ac9311bd55d45c67b3bcf4d0fc671fc6e6a6c3731081c2e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974837"
---
# <a name="configuring-video-encoding-microsoft-media-foundation"></a>設定影片編碼 (Microsoft 媒體基礎) 

若要設定影片編碼器，請執行下列步驟：

1.  使用 **IPropertyBag：： Write**，在編碼器 DMO 上設定任何屬性。 下列清單摘要說明編碼 CBR 影片資料流程所需的最基本屬性集合 (所有這些值都有可用於) 的預設值：

    -   [MFPKEY \_ VIDEOWINDOW](mfpkey-videowindowproperty.md)屬性會指定用於資料流程的緩衝區視窗。 如需有關緩衝區視窗設定以及它如何影響內容的詳細資訊，請參閱 [編碼方法](encodingmethods.md)。 預設的緩衝區視窗是三秒，適用于許多案例。
    -   影片複雜性的設定是決定編碼內容品質與編碼所需時間之間的取捨。 如果您未設定值，則會使用預設值。 不過，您可以藉由呼叫 [IWMCodecProps：： GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) 來取出 g \_ wszWMVCComplexityExLive、g \_ wszWMVCComplexityExOffline 和 g wszWMVCComplexityExMax，來尋找特定編解碼器的建議模式 \_ 。 然後，您可以將 [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md) 設定為介於0和回報的最大複雜性之間的值。
    -   [MFPKEY \_清晰](mfpkey-crispproperty.md) 地指定影片平滑的相對重要性，以及編碼框架的影像品質。 在大多數情況下，預設值都可以正常運作。
    -   針對儲存在 ASF 以外之容器中的影片內容， [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md) 屬性必須設定為0。 這不是預設值。

    如需設定 VBR 資料流程的詳細資訊，請參閱 [使用 Vbr 編碼](usingvbrencoding.md)。

2.  針對輸入類型設定 [**DMO 的 \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構，或者，如果您使用媒體基礎 SDK，請使用 [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader)函數。 使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構，描述未壓縮的輸入內容。 編解碼器不會調整影片大小或轉換色彩空間。
3.  使用 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) 或 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)設定輸入類型。
4.  設定編碼器的輸出類型。 在設定輸入類型之後，編碼器會列舉 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構的 **dwBitrate** 成員以外的輸出類型，或 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)介面的 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)] 屬性。 如果您在設定輸入類型之前先取出輸出型別，則傳遞的 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構將不會有相關聯的 **VIDEOINFOHEADER**。
5.  抓取編解碼器私用資料，並將它附加至您傳遞給 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構或 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構。 如需詳細資訊，請參閱 [使用影片編解碼器私用資料](usingvideocodecprivatedata.md)。
6.  藉由呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) 或 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 方法來設定輸出類型。 將 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)結構傳遞至已完成的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構 (包括 **pbFormat** 成員所參考) 附加私用資料，或呼叫 [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader)來建立 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 。

> [!Note]  
> 影片編碼器物件支援兩個輸出。 第二個輸出適用于編碼器「後置視圖」。 它會提供未壓縮的範例，因為它們將從解碼器傳遞。 這可讓您監視編碼的品質，而不必等到整個資料流程處理完畢。 這個輸出是選擇性的。 如果您想要使用它，請在用來設定編碼器輸入類型的相同進程下設定其類型。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 
