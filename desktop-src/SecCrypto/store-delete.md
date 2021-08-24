---
description: 刪除目前存放區物件所代表的憑證存放區。
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36c4a02795468ca719790707356b12a1aa24c1882a0cf57faa9e0454af33467a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972649"
---
# <a name="storedelete-method"></a>Store. Delete 方法

\[**Delete** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]

**Delete** 方法會刪除目前 [**存放區**](certificate.md)物件所代表的 [*憑證存放區*](../secgloss/c-gly.md)。 這個方法只會刪除非系統存放區。

## <a name="syntax"></a>語法


```VB
Store.Delete()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

下列存放區是系統存放區，無法刪除：

-   My
-   Root
-   信任
-   CA
-   UserDS
-   TrustedPublisher
-   不允許
-   AuthRoot
-   TrustedPeople

如果從 web 腳本呼叫， **Delete** 方法會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
