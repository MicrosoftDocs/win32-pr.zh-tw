---
description: 抓取延伸模組的編碼資料。
ms.assetid: 79811557-6d7e-4d19-bcbb-1f79455dd286
title: EncodedData 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension.EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2153c97d523693a0a1ea13f92135a17591ce68d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982569"
---
# <a name="extensionencodeddata-property"></a>EncodedData 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)。\]

**EncodedData** 屬性會抓取擴充功能的編碼資料。

## <a name="syntax"></a>Syntax


```VB
Extension.EncodedData As EncodedData
```



## <a name="property-value"></a>屬性值

代表憑證延伸之資料的 [**EncodedData**](encodeddata.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
