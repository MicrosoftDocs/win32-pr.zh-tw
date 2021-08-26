---
description: 指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程，以供另一個執行緒寫入。
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: 'MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941028"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入屬性

指定位元組資料流程處理常式是否可以使用開啟的位元組資料流程，以供另一個執行緒寫入。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

位元組資料流程處理常式可以支援此屬性。 若要取得或設定屬性，請先查詢 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面的位元組資料流程處理常式。 然後呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 或 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

如果這個屬性為 **TRUE**，則表示位元組資料流程處理常式可以在另一個執行緒寫入相同的資料流程時，從資料流程讀取。 開啟資料流程以供另一個執行緒寫入時， [**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) 方法會傳回 **MFBYTESTREAM \_ 共用 \_ 寫入** 旗標。

這個屬性會影響來源解析。 如果位元組資料流程已設定 **MFBYTESTREAM \_ 共用 \_ 寫入** 旗標，則 [來源解析](source-resolver.md) 程式將不會將該資料流程傳遞至位元組資料流程處理常式，除非處理常式的 MF \_ BYTESTREAMHANDLER \_ 接受 \_ 共用 \_ 寫入屬性設定為 **TRUE**。

**MFBYTESTREAM \_ SHARE \_ WRITE** 旗標是在處理常式從它讀取時，資料流程長度可能會變更的提示。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




