---
description: 編碼器上的媒體類型協商
ms.assetid: c8ae543e-68f7-4c74-9cb7-2a200bd51820
title: 編碼器上的媒體類型協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7845e9d50c5d418198dc0e08313e2e9329ffab8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945706"
---
# <a name="media-type-negotiation-on-the-encoder"></a>編碼器上的媒體類型協商

在 Microsoft 媒體基礎中，會使用一個輸入和一個輸出，將編碼器實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFTs) 。 在編碼會話之前，編碼器必須知道它將收到的資料流程特性（作為輸入），以及它將產生的資料流程格式（作為輸出）。 您必須先設定輸入和輸出媒體類型和相關特性，才能透過編碼器傳遞資料。 您必須提供輸入和輸出格式，方法是指定適當的 [媒體類型 guid](media-type-guids.md) ，並在輸出媒體類型上設定相關的 [媒體類型屬性](media-type-attributes.md) ，以設定輸出資料流程的特性。 新具現化的編碼器沒有任何已設定的媒體類型。

輸入媒體類型是未壓縮的格式，例如 PCM 音訊或 RGB 影片。 編碼器所使用的格式類型會限制為 **VIDEOINFOHEADER** 和 **WAVEFORMATEX** 結構所描述的格式類型。 如需這些結構的詳細資訊，請參閱 Windows SDK 檔。媒體基礎提供 helper 函式，以從格式結構建立媒體類型。 例如， [**MFInitMediaTypeFromVideoInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader) 函式會從 **VIDEOINFOHEADER** 結構初始化影片類型，而 [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) 函式會從 **WAVEFORMATEX** 或 **WAVEFORMATEXTENSIBLE** 結構初始化影片類型。 如需詳細資訊，請參閱 [媒體類型轉換](media-type-conversions.md)。 您必須藉由呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)，在編碼器上設定輸入媒體類型。

輸出媒體類型是最終來來源資料流或檔案中使用的壓縮格式。 只有在設定輸入媒體類型之後，才可以設定可用的輸出媒體類型。 您可以在迴圈中呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以抓取支援的輸出類型，直到編碼器傳回 **MF \_ E \_ NO 以上的 \_ \_ 類型**。 使用每個反復專案遞增型別索引。 當您找到適當的媒體類型時，請呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)來設定輸出媒體類型。

選擇輸出媒體類型的決定因素取決於編碼類型和編碼需求。 例如，針對以 CBR 編碼的音訊串流，您想要尋找符合輸入的媒體類型，並具有比目標值更接近的位元速率。

如果您想要使用 CBR 以外的編碼模式，您必須設定模式，然後列舉該模式的輸出類型，因為編碼器會根據設定的模式變更支援的輸出類型。 控制編碼模式的屬性為 [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) 和 [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)。 例如，如果您要列舉的是 VBR 品質編碼的輸出類型，則媒體類型會取決於您決定要使用的品質值。 如需有關設定這些屬性的詳細資訊，請參閱 [編碼屬性](configuring-the-encoder.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media 編碼器](windows-media-encoders.md)
</dt> </dl>

 

 



