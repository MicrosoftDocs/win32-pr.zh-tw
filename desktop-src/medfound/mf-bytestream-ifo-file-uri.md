---
description: 包含 HTTP 標頭中 HTTP 伺服器所指定之 IFO (DVD 資訊) 檔案的 URL，&\# 0034;Pragma： ifoFileURI.dlna.org&\# 0034;。
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: 'MF_BYTESTREAM_IFO_FILE_URI 屬性 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4349f3319a875f428921b0a99aefa61e49340c240a87260c1132abcc7c45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723468"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>MF \_ BYTESTREAM \_ IFO \_ FILE \_ URI 屬性

包含 HTTP 標頭 "Pragma： ifoFileURI.dlna.org" 中 HTTP 伺服器所指定之 IFO (DVD 資訊) 檔案的 URL。

## <a name="data-type"></a>資料類型

**LPWSTR**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="applies-to"></a>適用於

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>備註

HTTP 位元組資料流程會在 HTTP 標頭中搜尋 "ifoFileURI.dlna.org" 字串。 如果找到該字串，則會將它複製到位元組資料流程上的這個屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                           |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[位元組資料流程屬性](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




