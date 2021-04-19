---
description: 關閉開啟的憑證存放區。
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001153"
---
# <a name="storeclose-method"></a>Store. Close 方法

\[**Close** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]

**Close** 方法會關閉已開啟的 [*憑證存放區*](../secgloss/c-gly.md)。

## <a name="syntax"></a>語法


```VB
Store.Close()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

呼叫 **Close** 方法之後，就會終結 [**存放區**](store.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**市集**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**打開**](store-open.md)
</dt> </dl>

 

 
