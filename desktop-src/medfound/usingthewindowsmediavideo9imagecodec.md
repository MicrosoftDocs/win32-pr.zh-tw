---
description: 使用 Windows Media 視訊9.1 影像類別
ms.assetid: b77e955b-767b-4b64-9421-bacac9edf09c
title: 使用 Windows Media 視訊9.1 影像類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c630be78ec3edef1a47322b31f6a2331f15134a0cdffa4107b5a79daa86e9091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972627"
---
# <a name="using-the-windows-media-video-91-image-category"></a>使用 Windows Media 視訊9.1 影像類別

Windows Media 視訊9.1 影像類別與 Windows Media 視訊9編碼器和解碼器所支援的其他輸出分類不同。 它不會處理未壓縮的影片，而是採用特殊的輸入範例，其中包含結構化轉換資料，以及在其上執行轉換的 RGB 點陣圖影像。

編碼的 Windows Media 視訊9.1 影像內容幾乎與一般 Windows Media 視訊9編碼的內容相同，但它是由自己的 FOURCC ( "WMVP" ) 所識別。

影片影像的編碼器輸出類型會以與標準 Windows 媒體影片完全相同的方式來設定，不同之處在于子類型和壓縮值必須設定為影片影像識別碼。 這包括取得編解碼器私用資料，並將其附加至 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的需求。 如需詳細資訊，請參閱設定 [影片編碼](configuringvideoencoding.md)。

影片影像的輸入類型設定也非常類似于其他影片編碼器的輸入設定。 您可以藉由呼叫 [**IMediaObject：： GetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype)，或使用媒體基礎 SDK，藉由呼叫 [**IMFTransform：： GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ，並使用 [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)來取得 **DMO 的 \_ 媒體 \_ 類型**，以從編碼器取出部分完成的 [**DMO \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type)。 然後，您可以設定畫面格大小和 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式結構，就像標準影片一樣。 如同輸出型別，您必須確定子類型和壓縮值已正確設定。

## <a name="creating-input-samples"></a>建立輸入範例

影片影像編解碼器的輸入範例是結構化的。 影片影像所用的結構和常數定義不包含在 Windows Media 音訊和影片編解碼器介面中。 這些定義包含在 Windows 媒體格式 sdk 中，並在 Windows 媒體格式 sdk 檔中完整說明其使用方式。

## <a name="decoding"></a>解碼

解碼螢幕擷取畫面影片沒有特殊需求。 除了不同的子類型 (MEDIASUBTYPE \_ WMVP) 用於解碼輸入，壓縮的影片影像資料流程基本上與標準 Windows Media 視訊資料流程相同。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片](workingwithvideo.md)
</dt> </dl>

 

 
