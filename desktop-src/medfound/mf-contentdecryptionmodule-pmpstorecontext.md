---
description: 指定內容解密模組所使用的內容字串 (CDM 使用 MediaProtectionPMPServer 的) 。
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: e82bfb5bcf833957fa07ec5aa5c6dacdab346905692ab7cfcf6cbb18b940817b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060712"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT 屬性

指定內容解密模組所使用的內容字串 (CDM 使用 [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)的) 。


## <a name="data-type"></a>資料類型

**LPWSTR** (VT_LPWSTR) 

## <a name="property-guid"></a>屬性 GUID

**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**

## <a name="property-value"></a>屬性值

內容解密模組所使用的內容字串 (CDM) 的實作為。

## <a name="remarks"></a>備註

CDM 實作者應該尋找此值，並使用屬性名稱 "Windows 將值傳遞至[MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor)的函式。PMPStoreCoNtext」。


呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)時，應用程式不應該建立這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 102020年4月更新<br/>                                     |
| 標頭<br/>                   | <dl> <dt>mfcontentdecryptionmodule。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

- [媒體基礎屬性](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




