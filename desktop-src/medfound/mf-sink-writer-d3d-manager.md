---
description: 包含接收寫入器之 DXGI 裝置管理員的指標。
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: 'MF_SINK_WRITER_D3D_MANAGER 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706287b6001ba52c8bf5ba8a19326948afcf4f7f7569c606507115f484c46f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714308"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>MF \_ 接收 \_ 寫入器 \_ D3D \_ 管理員屬性

包含 [接收寫入器](sink-writer.md)之 DXGI 裝置管理員的指標。

## <a name="data-type"></a>資料類型

**IMFDXGIDeviceManager \* *_ 儲存為 _* IUnknown\***

## <a name="remarks"></a>備註

這個屬性的值是 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。

使用此屬性可為接收寫入器載入的任何影片編碼器或媒體接收器提供 Direct3D 裝置。

使用這個屬性搭配下列函數：

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[接收寫入器](sink-writer.md)
</dt> </dl>

 

 




