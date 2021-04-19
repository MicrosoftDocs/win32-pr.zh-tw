---
description: 抓取路徑長度條件約束的值。
ms.assetid: 77a12fdf-e9ed-4c79-aa2c-bd476ab3ff90
title: BasicConstraints. PathLenConstraint 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.PathLenConstraint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39656cf4f3cbe768589ba704a0a65c158da000fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985761"
---
# <a name="basicconstraintspathlenconstraint-property"></a>BasicConstraints. PathLenConstraint 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]

**PathLenConstraint** 屬性會捕獲 path length 條件約束的值。

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.PathLenConstraint As Long
```



## <a name="property-value"></a>屬性值

路徑長度條件約束的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
