---
description: 從收件者集合抓取物件。
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: 收件者. 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a80b472c8257597356c626a9e88aad97c447f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000005"
---
# <a name="recipientsitem-property"></a>收件者. 專案屬性

\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Item** 屬性會從收件 [**者集合抓取**](recipients.md)物件。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>屬性值

代表收件 [**者集合中**](recipients.md) 索引項目目的 variant。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**收件者**](recipients.md)
</dt> </dl>

 

 
