---
description: 包含媒體會話拓撲載入器的 CLSID。
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: 'MF_SESSION_TOPOLOADER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977101"
---
# <a name="mf_session_topoloader-attribute"></a>MF \_ 會話 \_ TOPOLOADER 屬性

包含媒體會話拓撲載入器的 CLSID。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

您可以使用這個屬性來提供媒體會話的自訂拓撲載入器。

使用 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)函數或 [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)函數的 *pConfiguration* 參數來設定這個屬性。

如果設定此屬性，媒體會話會在建立拓撲載入器時，使用指定的 CLSID 來呼叫 **CoCreateInstance** 。 此 CLSID 所建立的物件必須公開 [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) 介面。

如果未設定此屬性，則媒體會話會建立媒體基礎中提供的預設拓撲載入器。

拓撲載入器必須支援多執行緒單元。 您應該將拓撲載入器註冊為 >threadingmodel = "Both"。 此外，如果您在受保護的媒體路徑中使用拓撲載入器 (PMP) ，拓撲載入器必須是受信任的元件。 如需詳細資訊，請參閱 [受保護的媒體路徑](protected-media-path.md)。

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
</dt> <dt>

[自訂拓撲載入器](custom-topology-loaders.md)
</dt> </dl>

 

 




