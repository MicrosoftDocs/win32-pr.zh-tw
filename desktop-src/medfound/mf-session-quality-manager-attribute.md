---
description: 包含媒體會話之品質管制員的 CLSID。
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: 'MF_SESSION_QUALITY_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319639"
---
# <a name="mf_session_quality_manager-attribute"></a>MF \_ 會話 \_ 品質 \_ 管理員屬性

包含媒體會話之品質管制員的 CLSID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

您可以使用這個屬性來提供媒體會話的自訂品質管制員。

使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數來設定這個屬性。

如果設定此屬性，則媒體會話會使用指定的 CLSID 來呼叫 **CoCreateInstance** ，以建立「品質管制員」。 此 CLSID 所建立的物件必須公開 [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) 介面。

如果未設定此屬性，則媒體會話會建立媒體基礎中提供的預設品質管制員。

如果您想要執行不含品質管制員的媒體會話，請將此屬性設定為 **GUID \_ Null**。

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

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[媒體會話屬性](media-session-attributes.md)
</dt> </dl>

 

 




