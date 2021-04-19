---
description: 指出媒體來源是否支援硬體資料流程。
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: 'MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979302"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>MF \_ 來源 \_ 資料流程 \_ 支援 \_ HW \_ 連接屬性

指出媒體來源是否支援硬體資料流程。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

當媒體來源 proxy 硬體裝置，而且能夠透過硬體匯流排傳輸下游資料，而不需要將資料傳送到 CPU 時，就會使用此屬性。 例如，網路攝影機可能會將 h.264 編碼的影片直接傳遞至整合式硬體解碼器。

在此案例中，來源和解碼器仍會以 [媒體來源](media-sources.md) 物件的 Microsoft 媒體基礎來表示，而 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。 不過，在管線層的這兩個物件之間不會有資料流程，如下圖所示。

![顯示硬體 proxy 來源的圖表。](images/proxy-mft3.png)

媒體來源和 MFT 之間的連接會以下面方式協商。

1.  管線會查詢 [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) 介面的媒體來源。  (此介面為支援媒體來源的選擇性。 ) 
2.  管線會呼叫 [**IMFMediaSourceEx：： GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) 來取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
3.  適用于 MF \_ 來來源資料流的管線 \_ 查詢 \_ 支援 \_ HW \_ 連接屬性。 如果屬性存在且等於 **TRUE**，則媒體來源支援硬體連接。
4.  此管線會檢查 mft 上的 [mft \_ 列舉 \_ 硬體 \_ URL \_ 屬性](mft-enum-hardware-url-attribute.md) 屬性，以檢查 mft 是否也是硬體 proxy。 如需詳細資訊，請參閱 [硬體 MFTs](hardware-mfts.md)。
5.  管線會在 MFT 上設定 [mft \_ 連線 \_ 資料流程 \_ 屬性](mft-connected-stream-attribute.md) 屬性。 這個屬性的值是從步驟2中的媒體來源取得的 [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標。
6.  管線會在媒體來源和 MFT 上將 [ \_ 連接 \_ 至 \_ HW \_ STREAM](mft-connected-to-hw-stream.md) 屬性的 MFT 設定為 **TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[硬體 MFTs](hardware-mfts.md)
</dt> </dl>

 

 




