---
description: 設定範例的金鑰識別碼。
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: 'MFSampleExtension_Content_KeyID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38498665dddaed0cd38082246f61f0f86c9b1b7a1e8cec7d19d476c860fe8d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848168"
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
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[MFSampleExtension \_ 加密 \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




