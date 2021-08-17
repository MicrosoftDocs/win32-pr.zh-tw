---
description: 設定或抓取屬性的 CAPICOM 名稱。 這是預設屬性。
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773652"
---
# <a name="attributename-property"></a>Attribute.Name 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Name** 屬性會設定或抓取屬性的 CAPICOM 名稱。 這是預設屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>屬性值

指定屬性之 CAPICOM 名稱的 [**capicom \_ 屬性**](capicom-attribute.md) 列舉值。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                                                 | 意義                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**CAPICOM \_ 驗證 \_ 屬性 \_ 簽署 \_ 時間**</dt> </dl>                         | 屬性包含建立簽章的時間。<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 名稱**</dt> </dl>                      | 屬性包含已簽署檔的名稱。<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**CAPICOM \_ 驗證的 \_ 屬性 \_ 檔 \_ 描述**</dt> </dl> | 屬性包含已簽署檔的描述。<br/>    |



 

## <a name="remarks"></a>備註

當這個屬性的值是直接或間接重設時，會重設物件的整個狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性**](attribute.md)
</dt> </dl>

 

 
