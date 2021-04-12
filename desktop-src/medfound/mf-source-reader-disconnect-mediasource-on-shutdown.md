---
description: 指定來源讀取器是否關閉媒體來源。
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: 'MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321663"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>MF \_ 來源 \_ 讀取 \_ 器 \_ \_ 在 \_ SHUTDOWN 屬性中斷 MEDIASOURCE

指定 [來源讀取器](source-reader.md) 是否關閉媒體來源。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

只有當應用程式透過呼叫 [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) 或呼叫 [**IMFReadWriteClassFactory：： CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)，從現有的媒體來源物件建立來源讀取器時，才會套用此屬性。

根據預設，當應用程式釋放來源讀取器時，來源讀取器會藉由呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 來關閉媒體來源。 屆時，應用程式將無法再使用媒體來源。

但是，如果 MF \_ 來源 \_ 讀取器 \_ \_ 在 SHUTDOWN 上中斷連線 MEDIASOURCE \_ \_ 屬性為 **TRUE**，則來源讀取器不會關閉媒體來源。 這表示應用程式在釋放來源讀取器之後，仍然可以使用媒體來源。 這也表示應用程式會負責呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 。

如果應用程式從 URL 或位元組資料流程建立來源讀取器，來源讀取器一律會關閉媒體來源。 \_ \_ \_ \_ \_ \_ 在此情況下，會忽略 MEDIASOURCE ON SHUTDOWN 屬性的 MF 來源讀取器中斷連線。

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

 

 




