---
description: 指定上一次修改位元組資料流程的時間。
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: 'MF_BYTESTREAM_LAST_MODIFIED_TIME 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b476a78dba2bf757ed37b6029d67d5084804d1360dbc61e7c8861005b74a3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113968"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a>MF \_ BYTESTREAM \_ 上次 \_ 修改 \_ 時間屬性

指定上一次修改位元組資料流程的時間。

## <a name="data-type"></a>資料類型

位元組陣列

## <a name="remarks"></a>備註

此屬性是選擇性的。 屬性的值是 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                                              |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[位元組資料流程屬性](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
