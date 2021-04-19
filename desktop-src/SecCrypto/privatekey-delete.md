---
description: 刪除 PrivateKey 物件所參考的私用金鑰容器。
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993974"
---
# <a name="privatekeydelete-method"></a>PrivateKey 方法

\[**Delete** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]

**Delete** 方法會刪除 [**PrivateKey**](privatekey.md)物件所參考的私用金鑰容器。

## <a name="syntax"></a>語法


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 這個方法會刪除 [**PrivateKey**](privatekey.md) 物件所參考的私密金鑰容器，以及容器中的所有私密金鑰。 使用對應至已刪除私密金鑰的公開金鑰加密的任何事物，將無法再解密。

 

\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
