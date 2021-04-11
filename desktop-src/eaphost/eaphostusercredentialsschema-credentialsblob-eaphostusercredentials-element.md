---
title: CredentialsBlob (EapHostUserCredentials) 元素
description: 當方法設定為二進位 BLOB 而非 XML 文字格式時，就會使用。
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- CredentialsBlob 元素 EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094187"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a>CredentialsBlob (EapHostUserCredentials) 元素

當方法設定是二進位 BLOB 而非 XML 文字格式時，就會使用 **CredentialsBlob (EapHostUserCredentials)** 元素。

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

**CredentialsBlob** 元素是由 [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)元素定義。

## <a name="remarks"></a>備註

[**認證**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)和 **CredentialsBlob** 元素不能同時使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[eaphostusercredentials 架構](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





