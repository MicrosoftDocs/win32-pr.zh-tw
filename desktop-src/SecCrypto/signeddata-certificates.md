---
description: 抓取與 SignedData 物件相關聯的憑證集合。 在抓取之後，可以列舉集合中的個別憑證物件。
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: SignedData 憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990055"
---
# <a name="signeddatacertificates-property"></a>SignedData 憑證屬性

\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

[**憑證**] 屬性會抓取與 [**SignedData**](signeddata.md)物件相關聯的 [**憑證**](certificates.md)集合。 在抓取之後，可以列舉集合中的個別 [**憑證**](certificate.md) 物件。

## <a name="syntax"></a>Syntax


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a>屬性值

與 [**SignedData**](signeddata.md)物件相關聯的 [**憑證**](certificates.md)集合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
