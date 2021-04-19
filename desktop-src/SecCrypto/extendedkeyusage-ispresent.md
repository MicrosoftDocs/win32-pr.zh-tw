---
description: 傳回布林值，指出 EKU 延伸是否存在。 這是預設屬性。
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 785fa3c973e7f90eeab20bd76826b9e5bf612891
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984137"
---
# <a name="extendedkeyusageispresent-property"></a>ExtendedKeyUsage. IsPresent 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**IsPresent** 屬性會傳回布林值，指出 EKU 延伸是否存在。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則表示 EKU 延伸模組存在。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
