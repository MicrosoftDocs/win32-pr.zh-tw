---
description: 提供回呼介面，讓應用程式從受保護的媒體路徑接收內容啟用程式物件 (PMP) 會話。
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: 'MF_SESSION_CONTENT_PROTECTION_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981186"
---
# <a name="mf_session_content_protection_manager-attribute"></a>MF \_ 會話 \_ 內容 \_ 保護 \_ 管理員屬性

提供回呼介面，讓應用程式從受保護的媒體路徑接收內容啟用程式物件 (PMP) 會話。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="remarks"></a>備註

這個屬性的值是應用程式 [_ *IMFContentProtectionManager* *](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)介面的指標。

使用 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數，在 PMP 會話上設定此屬性。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[媒體會話屬性](media-session-attributes.md)
</dt> <dt>

[如何播放受保護的媒體檔案](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




