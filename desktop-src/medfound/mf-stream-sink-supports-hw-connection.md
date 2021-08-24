---
description: 指出媒體接收器是否支援硬體資料流程。
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: 'MF_STREAM_SINK_SUPPORTS_HW_CONNECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714371"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>MF \_ 資料流程 \_ 接收 \_ 支援 \_ HW \_ 連接屬性

指出媒體接收器是否支援硬體資料流程。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

當媒體接收器 proxy 硬體裝置，而且能夠透過硬體匯流排接收資料時，就會使用此屬性。 例如，硬體音訊解碼器可能會直接將音訊資料傳送到音訊轉譯硬體。

在此案例中， [媒體基礎轉換](media-foundation-transforms.md) (MFT) 和媒體接收器仍會在 Microsoft 媒體基礎中表示解碼器和接收器。 不過，在管線層的這兩個物件之間不會有資料流程，如下圖所示。

![顯示硬體 proxy 來源的圖表。](images/proxy-mft4.png)

MFT 和媒體接收器之間的連接會以下面方式進行協商。

1.  此管線會檢查 mft 上的 [mft \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性，以檢查 mft 是否為硬體 proxy。 如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。
2.  管線會取得媒體接收器上資料流程接收之 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 介面的指標。
3.  此管線會使用 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) 指標來查詢 MF \_ 資料流程接收， \_ 以 \_ 支援 \_ HW \_ 連接屬性。 如果此屬性存在且等於 **TRUE**，則媒體來源支援硬體連接。
4.  管線會在資料流程接收上設定 [MFT \_ 連接的 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md) 屬性。 這個屬性的值是從 MFT [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 的指標。
5.  此管線會在串流接收和 MFT 上將 [ \_ 連接 \_ 至 \_ HW \_ 串流](mft-connected-to-hw-stream.md) 屬性的 MFT 設定為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




