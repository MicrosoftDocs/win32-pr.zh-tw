---
description: 可讓兩個媒體會話實例共用相同的受保護媒體路徑 (PMP) 進程。
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: 'MF_SESSION_SERVER_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102334"
---
# <a name="mf_session_server_context-attribute"></a>MF \_ 會話 \_ 伺服器 \_ 內容屬性

可讓兩個媒體會話實例共用相同的受保護媒體路徑 (PMP) 進程。

## <a name="data-type"></a>資料類型

**IUnknown\***

## <a name="remarks"></a>備註

如果您想要在現有的 PMP 流程中建立 PMP 媒體會話，請使用此屬性。 屬性的值是 [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) 介面的指標。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
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
</dt> </dl>

 

 




