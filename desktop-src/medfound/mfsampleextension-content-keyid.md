---
description: 設定範例的金鑰識別碼。
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: 'MFSampleExtension_Content_KeyID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989938"
---
# <a name="mfsampleextension_content_keyid-attribute"></a>MFSampleExtension \_ 內容 \_ KeyID 屬性

設定範例的金鑰識別碼。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="examples"></a>範例

下列範例顯示如何設定範例的金鑰識別碼。


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ 加密 \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




