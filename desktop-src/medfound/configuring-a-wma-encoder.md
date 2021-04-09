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
# <a name="setting-an-output-type-for-a-wma-encoder"></a>設定 WMA 編碼器的輸出類型

若要建立 Windows Media 音訊 (WMA) 編碼器的有效輸出類型，您必須擁有下列資訊：

-   Repesents 編碼之 WMA 格式的音訊子類型。 請參閱 [音訊子類型 guid](audio-subtype-guids.md)。
-   要在編碼器上設定的設定屬性。

    設定屬性記載于 Windows Media 音訊和影片編解碼器和 DSP Api 檔中。 如需詳細資訊，請參閱 [編碼屬性](configuring-the-encoder.md)中的「音訊串流屬性」。

### <a name="windows-vista-or-later"></a>Windows Vista 或更新版本

若要取得編碼器的有效輸出型別，請執行下列步驟。

1.  使用 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 或 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函數來建立編碼器的實例。
2.  查詢編碼器以取得 **IPropertyStore** 介面。
3.  使用 **IPropertyStore** 介面設定編碼器。
4.  藉由在迴圈中呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) 來取出支援的輸出類型，直到編碼器傳回 **MF \_ E \_ NO \_ 其他 \_ 類型** ，而且您選擇目標媒體類型。 I
5.  呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。

### <a name="windows-7"></a>Windows 7

若要在 Windows 7 中取得編碼器的有效輸出類型，媒體基礎提供 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) 函數。 應用程式必須通過 repesents 編碼的 WMA 和編碼屬性所需的音訊子類型。 這些屬性是必要的，因為編碼器會根據設定的模式變更支援的輸出類型。

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)僅支援 [常數位速率編碼](constant-bit-rate-encoding.md)。

 

如果呼叫成功，應用程式會接收 [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) 物件中所支援之輸出媒體類型的 IUnknown 指標清單。 若要設定輸出媒體類型，請尋找符合您目標型別的類型，然後呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 來設定編碼器上的壓縮媒體類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> </dl>

 

 



