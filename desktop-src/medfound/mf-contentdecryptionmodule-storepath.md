---
description: 指定檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8126bfea15f9946bb9950293a6c39c101f9c37c8870176fb4bb0108aa5862bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723458"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH 屬性

指定檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。


## <a name="data-type"></a>資料類型

**LPWSTR** (VT_LPWSTR) 

## <a name="property-guid"></a>屬性 GUID

**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**

## <a name="property-value"></a>屬性值

檔案路徑，代表內容解密模組 (CDM) 可用於初始化的儲存位置。

## <a name="remarks"></a>備註

如果未設定 [MF_CONTENTDECRYPTIONMODULE_INPRI加值稅ESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) 屬性，則使用這個屬性指定的路徑也將用於內容特定資料。

為了改善 COM 效能，應用程式不應該在釋放 CDM 物件後刪除存放區位置。



當您藉由呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)來建立 CDM 時，請設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 102020年4月更新<br/>                                     |
| 標頭<br/>                   | <dl> <dt>mfcontentdecryptionmodule。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

- [媒體基礎屬性](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




