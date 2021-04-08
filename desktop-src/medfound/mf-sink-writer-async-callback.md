---
description: 包含接收寫入器的應用程式回呼介面指標。
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: 'MF_SINK_WRITER_ASYNC_CALLBACK 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695020"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>MF \_ 接收 \_ 寫入器 \_ 非同步 \_ 回呼屬性

包含接收器寫入器的應用程式回呼介面指標。

## <a name="data-type"></a>資料類型

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ 儲存為 _*IUnknown \**_

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="remarks"></a>備註

這個屬性的值是應用程式 [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) 介面的指標。

使用這個屬性搭配下列函數：

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

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
</dt> </dl>

 

 




