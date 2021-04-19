---
description: PublicKey 物件代表憑證物件中的公開金鑰。
title: PublicKey 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978507"
---
# <a name="publickey-object"></a>PublicKey 物件

\[**PublicKey** 物件可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PublicKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1)。\]

**PublicKey** 物件代表 [**憑證**](certificate.md)物件中的公開金鑰。

## <a name="when-to-use"></a>使用時機

**PublicKey** 物件是用來取得公開金鑰的相關資料。

## <a name="members"></a>成員

**PublicKey** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**PublicKey** 物件具有這些屬性。



| 屬性                                                            | 存取類型          | Description                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**演算法**](publickey-algorithm.md)<br/>                 | 唯讀<br/> | 抓取標識公開金鑰所使用之演算法的 [**OID**](oid.md) 物件。 這是預設屬性。<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | 唯讀<br/> | 抓取可存取公開金鑰值的 [**EncodedData**](encodeddata.md) 物件。<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | 唯讀<br/> | 抓取可存取公開金鑰演算法之參數的 [**EncodedData**](encodeddata.md) 物件。<br/>  |
| [**長度**](publickey-length.md)<br/>                       | 唯讀<br/> | 抓取公開金鑰的長度（以位為單位）。<br/>                                                                             |



 

## <a name="remarks"></a>備註

無法建立 **PublicKey** 物件。

**PublicKey** 物件是由 [**PublicKey**](certificate-publickey.md)方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
