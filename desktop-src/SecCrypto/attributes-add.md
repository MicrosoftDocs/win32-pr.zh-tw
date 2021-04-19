---
description: 將屬性物件加入至集合。
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: 屬性。新增方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979472"
---
# <a name="attributesadd-method"></a>屬性。新增方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Add** 方法會將 [**屬性**](attribute.md)物件加入至集合。

## <a name="syntax"></a>語法


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

要加入至集合結尾的 [**屬性**](attribute.md) 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[加密物件](cryptography-objects.md)
</dt> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 
