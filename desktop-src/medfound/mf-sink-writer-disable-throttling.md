---
description: 指定接收寫入器是否限制傳入資料的速率。
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: 'MF_SINK_WRITER_DISABLE_THROTTLING 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999938"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a>MF \_ 接收 \_ 寫入器 \_ 停用 \_ 節流屬性

指定接收寫入器是否限制傳入資料的速率。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

根據預設，接收寫入器的 [**IMFSinkWriter：： WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) 方法會封鎖呼叫的執行緒，以限制資料的速率。 這可防止應用程式太快傳遞範例。 若要停用此行為，請 \_ \_ \_ \_ 在建立接收寫入器時 ，將 [MF 接收寫入器停用節流] 屬性設定為 [TRUE]。

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

 

 




