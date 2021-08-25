---
description: 清除集合中的所有屬性物件。
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Attributes。 Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c2e5aa0f99824d87b865a56fe336161b8963bb9ba1da338bb8603f722085cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879858"
---
# <a name="attributesclear-method"></a>Attributes。 Clear 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Clear** 方法會清除集合中的所有 [**屬性**](attribute.md)物件。

## <a name="syntax"></a>語法


```VB
Attributes.Clear()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 
