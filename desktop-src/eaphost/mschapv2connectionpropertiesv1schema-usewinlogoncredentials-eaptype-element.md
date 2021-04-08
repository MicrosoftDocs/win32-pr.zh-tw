---
title: UseWinLogonCredentials (EapType) 元素
description: 瞭解 UseWinLogonCredentials (EapType) 元素。 此元素控制 winlogin 認證的使用。
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- UseWinLogonCredentials 元素 EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683125"
---
# <a name="usewinlogoncredentials-eaptype-element"></a>UseWinLogonCredentials (EapType) 元素

**UseWinLogonCredentials (EapType)** 元素會控制 winlogin 認證的使用。

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

**UseWinLogonCredentials** 元素是由 [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)元素定義。

## <a name="remarks"></a>備註

若為 TRUE，則表示 EAP MS-CHAPv2 從 winlogon 取得認證。 如果為 FALSE，則表示 EAP MS-CHAPv2 取得使用者的認證。 **UseWinLogonCredentials (EapType)** 元素是選擇性的。

## <a name="requirements"></a>規格需求



| 角色 | 支援的最低 OS 版本 |
|------|-------------------------------|
| 用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[EAPHost 和舊版架構](eaphost-schemas.md)
</dt> <dt>

[mschapv2connectionpropertiesv1 架構](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





