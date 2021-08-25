---
description: 從集合中移除已編制索引的屬性物件。
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributes. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea18aab32153c998a0ddbaced65727e1ecb43dc8c54a7e3989aadcb698693970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879768"
---
# <a name="attributesremove-method"></a>Attributes. Remove 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Remove** 方法會從集合中移除已編制索引的 [**屬性**](attribute.md)物件。

## <a name="syntax"></a>語法


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要移除之 [**屬性**](attribute.md) 物件的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。

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

 

 
