---
description: 包含適用于來源讀取器的 Microsoft Direct3D 裝置管理員的指標。
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: 'MF_SOURCE_READER_D3D_MANAGER 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849521"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>MF \_ 來源 \_ 讀取器 \_ D3D \_ 管理員屬性

包含適用于[來源讀取器](source-reader.md)的 Microsoft [Direct3D 裝置管理員](direct3d-device-manager.md)的指標。

## <a name="data-type"></a>資料類型

**IDirect3DDeviceManager9 \* 或 IMFDXGIDeviceManager \*** 儲存為 **IUnknown \** _

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

這個屬性的值可以是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標或 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager)。

使用此屬性可為來源讀取器所載入的任何影片解碼器提供 Direct3D 裝置。 如果您設定此屬性，且解碼器支援 Microsoft DirectX Video 加速 (DXVA) ，則來源讀取器會使用 Direct3D 裝置來配置影片緩衝區。 這些緩衝區與 DXVA 2 video 處理器相容。  (參閱 [DXVA Video 處理](dxva-video-processing.md)。 ) 

使用這個屬性搭配下列函數：

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

如果您要使用來源讀取器來取得已解碼的影片畫面，並使用 Direct3D 來顯示畫面格，通常會設定此屬性。 設定此屬性可讓解碼器使用 DXVA。

如果有下列情況，您就不會設定這個屬性：

-   您使用來源讀取器來處理音訊，而非影片。
-   您正在從來源讀取程式取得壓縮的影片。 在此情況下，來源讀取器不會建立解碼器。

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

[來源讀取程式](source-reader.md)
</dt> <dt>

[來源讀取器屬性](source-reader-attributes.md)
</dt> </dl>

 

 




