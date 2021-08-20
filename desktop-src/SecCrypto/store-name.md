---
description: 抓取此物件所代表的憑證存放區名稱。
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dad326baca135e9cdb04c63e9e26176ff4f6b7486b5fb7aedb71dc010391f4a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972484"
---
# <a name="storename-property"></a>Store.Name 屬性

\[[ [**名稱**](store-location.md) ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

[**Name**](store-location.md)屬性會抓取此物件所代表的憑證存放區名稱。

## <a name="syntax"></a>Syntax


```VB
Store.Name As String
```



## <a name="property-value"></a>屬性值

表示憑證存放區名稱的 **字串** 值。

## <a name="remarks"></a>備註

憑證存放區名稱的範例包括 My 和 Root。

[**Name**](store-location.md)屬性的值與開啟存放區時，針對 [**Open**](store-open.md)方法的 *StoreName* 參數所提供的值相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> </dl>

 

 
