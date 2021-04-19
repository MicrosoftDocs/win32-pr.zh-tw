---
description: 抓取布林值，這個值會指出基本條件約束延伸是否存在。 這是預設屬性。
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992905"
---
# <a name="basicconstraintsispresent-property"></a>BasicConstraints. IsPresent 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]

**IsPresent** 屬性會抓取布林值，指出基本條件約束延伸是否存在。 這是預設屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>屬性值

若 **為 true**，則會出現基本限制延伸。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicConstraints**](basicconstraints.md)
</dt> </dl>

 

 
