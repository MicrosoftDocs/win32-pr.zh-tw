---
description: 讓來源讀取器或接收寫入器使用硬體媒體基礎轉換 (MFTs) 。
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: 'MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319979"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換屬性

讓來源讀取器或接收寫入器使用硬體媒體基礎轉換 (MFTs) 。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

根據預設，來源讀取器和接收寫入器不會使用硬體解碼器或編碼器。 若要啟用硬體 MFTs，請在建立來源讀取器或接收寫入器時，將此屬性設定為 **TRUE** 。

使用這個屬性搭配下列函數：

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

預設行為有一個例外狀況。 來源讀取器和接收寫入器會自動使用在呼叫端進程的本機註冊的 MFTs。 若要在本機註冊 MFT，請呼叫 [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) 或 [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)。 即使未設定 [ **MF \_ READWRITE \_ 啟用 \_ 硬體 \_ 轉換** ] 屬性，仍會使用在本機註冊的硬體 MFTs。

此屬性不會影響使用 DirectX Video 加速 (DXVA) 的硬體加速影片解碼。 若要在來源讀取器中啟用 DXVA 解碼，請設定 [ [MF 來源讀取器] 「 \_ \_ \_ D3D \_ 管理員](mf-source-reader-d3d-manager.md) 」屬性。

如果此屬性為 **TRUE**，請勿將 [ [MF \_ READWRITE 停 \_ 用 \_ 轉換器](mf-readwrite-disable-converters.md) ] 屬性設定為 [否]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[接收寫入器屬性](sink-writer-attributes.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




