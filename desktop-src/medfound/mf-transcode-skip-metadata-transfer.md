---
description: 指定中繼資料是否要寫入至轉碼檔案。
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: 'MF_TRANSCODE_SKIP_METADATA_TRANSFER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191623"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸屬性

指定中繼資料是否要寫入至轉碼檔案。 此容器屬性會儲存在轉碼設定檔中。

## <a name="data-type"></a>資料類型

**UINT32**

\_ \_ 下表說明 MF 轉碼略過 \_ 中繼資料 \_ 傳輸屬性的可能值。



| 值                                                                        | 意義                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 自動將檔案層級中繼資料從來源檔案傳送至轉碼檔案。<br/> |
| <dl> <dt>1</dt> </dl> | 來源檔案中繼資料不會寫入至轉碼檔案。<br/>                          |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="remarks"></a>備註

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTranscodeProfile::GetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




