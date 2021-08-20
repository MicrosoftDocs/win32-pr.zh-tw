---
description: 編碼屬性
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: 編碼屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743490"
---
# <a name="encoding-properties"></a>編碼屬性

Windows Media 音訊和 Windows Media 視訊編碼器支援各種編碼模式。 這些模式通常是藉由設定編碼器 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 的屬性來設定。 若要執行檔案編碼，不論使用 WMContainer 層級元件或建立部分拓撲，您都必須根據編碼模式和資料流程的媒體類型設定屬性，以適當地設定編碼器。 您必須在編碼器和物件上設定相同的屬性集， (ASF 檔案接收或 ASF 多工器，) 您要用來寫入 ASF 檔。

編碼器屬性定義于 wmcodecdsp 中。 用來設定編碼器的特定屬性是使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的方法所設定。

-   [音訊串流屬性](#audio-stream-properties)
-   [影片資料流程屬性](#video-stream-properties)
-   [設定編碼器的屬性儲存區](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>音訊串流屬性

下表顯示音訊串流的編碼器設定。



| 編碼類型                                                                                        | 屬性名稱-值                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [常數位元速率編碼](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **FALSE** (選擇性) 預設 \_ 會將 MFPKEY VBRENABLED 設定為 **FALSE**。<br/>                                                                                             |
| [以品質為基礎的變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-1 (選擇性) <br/> 根據預設，MFPKEY \_ PASSESUSED 會設定為1。<br/> MFPKEY \_ 所需 \_ 的 VBRQUALITY-從0到100<br/> |
| [不受限制的變數位速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [尖峰限制的可變位速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-最大位元速率<br/> MFPKEY \_ BMAX-最大緩衝區視窗<br/>                               |



 

### <a name="video-stream-properties"></a>影片資料流程屬性

下表顯示影片串流的編碼器設定。



| 編碼類型                                                                                        | 屬性名稱                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [常數位元速率編碼](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED- **FALSE** (選用) <br/> 根據預設，MFPKEY \_ VBRENABLED 設定為 **FALSE**。<br/> MFPKEY \_ VIDEOWINDOW-緩衝區視窗<br/>                                  |
| [以品質為基礎的變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-1 (選擇性) <br/> 根據預設，MFPKEY \_ PASSESUSED 會設定為1。<br/> MFPKEY \_ 所需 \_ 的 VBRQUALITY-從0到100<br/> |
| [不受限制的變數位速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-2<br/>                                                                                                                          |
| [尖峰限制的可變位速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED- **TRUE**<br/> MFPKEY \_ PASSESUSED-2<br/> MFPKEY \_ RMAX-最大位元速率<br/> MFPKEY \_ BMAX-最大緩衝區視窗<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>設定編碼器的屬性儲存區

您必須在編碼會話之前，指定編碼類型和各種資料流程特定設定，以設定編碼器。 您也必須在 [ASF ContentInfo 物件](asf-contentinfo-object.md) 的屬性存放區中設定編碼器屬性，該物件代表輸出檔案的 Asf 標頭物件。

如果您使用編碼器 MFT：

1.  取得編碼器 MFT [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面的參考，如 [使用編碼器的 IMFTransform 介面](using-an-encoder-s-imftransform--interface.md)中所述。
2.  查詢編碼器 MFT 以取得 **IPropertyStore** 介面。
3.  藉由呼叫 **IPropertyStore：： SetValue** 來設定必要的屬性。

如果您使用內建的編碼器啟用物件，並已建立已設定的 ASF 檔案接收，則可以將 ASF 媒體接收器的屬性存放區傳遞給 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)。 編碼器會根據應用程式所指定的設定自動設定。 如需詳細資訊，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)中所述的程式。

如需使用啟用物件建立媒體基礎物件的詳細資訊，請參閱 [啟用物件](activation-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[具現化編碼器 MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows媒體編碼器](windows-media-encoders.md)
</dt> </dl>

 

 
