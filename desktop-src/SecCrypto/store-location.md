---
description: 抓取此物件所代表之憑證存放區的位置。
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983222"
---
# <a name="storelocation-property"></a>Store. Location 屬性

\[[ **位置** ] 屬性可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

**Location** 屬性會抓取此物件所代表之憑證存放區的位置。

## <a name="syntax"></a>Syntax


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a>屬性值

表示憑證存放區位置的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md) 值。

## <a name="remarks"></a>備註

**Location** 屬性的值與開啟存放區時，針對 [**Open**](store-open.md)方法的 *StoreLocation* 參數所提供的值相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**市集**](store.md)
</dt> </dl>

 

 
