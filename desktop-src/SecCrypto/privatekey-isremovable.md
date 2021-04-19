---
description: 傳回布林值，指出私密金鑰是否位於卸除式存放裝置中。
ms.assetid: 9371d7cf-65b2-4c0f-a387-195a058d6a8b
title: PrivateKey. IsRemovable 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsRemovable
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6684d40302746a736701b824685a54faeff5354a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996411"
---
# <a name="privatekeyisremovable-method"></a>PrivateKey. IsRemovable 方法

\[**IsRemovable** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**IsRemovable** 方法會傳回布林值，指出私密金鑰是否位於卸除式存放裝置中。

## <a name="syntax"></a>語法


```VB
PrivateKey.IsRemovable()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

若為 true，則私密金鑰位於卸除式存放裝置中。

## <a name="remarks"></a>備註

此方法的傳回值相依于 (CSP) 使用的 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 。 如果使用 Microsoft CSP，則這個方法會傳回信任的值。 如果 CSP 不是 Microsoft CSP，則傳回值無法信任為正確。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
