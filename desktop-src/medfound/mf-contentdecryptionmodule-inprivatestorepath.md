---
description: 指定檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: bf03d4411ac2959a336b931bc5e45ec969772ab35c194de03cbd9c74aaca0c0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244771"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a>MF \_ CONTENTDECRYPTIONMODULE \_ INPRI加值稅ESTOREPATH 屬性

指定檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。


## <a name="data-type"></a>資料類型

**LPWSTR** (VT_LPWSTR) 

## <a name="property-guid"></a>屬性 GUID

**MF \_ CONTENTDECRYPTIONMODULE \_ INPRI加值稅ESTOREPATH**

## <a name="property-value"></a>屬性值

檔案路徑，代表內容解密模組 (CDM) 可用於內容特定資料的儲存位置。

## <a name="remarks"></a>備註

應用程式應該在 CDM 物件發行之後，刪除存放區位置。

如果未設定此屬性，系統將會使用以內容特定資料的 [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) 屬性指定的路徑。

當您藉由呼叫 [IMFContentDecryptionModuleAccess：： CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)來建立 CDM 時，請設定這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 102020年4月更新<br/>                                     |
| 標頭<br/>                   | <dl> <dt>mfcontentdecryptionmodule。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

- [媒體基礎屬性](media-foundation-properties.md)
- [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




