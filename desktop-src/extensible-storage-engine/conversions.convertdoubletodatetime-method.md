---
description: 深入瞭解： ConvertDoubleToDateTime 方法
title: ConvertDoubleToDateTime 方法
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 208cd27ea6e3779923e1d5d99fffff44cd4c374117a0fb40471e13068e2c2541
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117716620"
---
# <a name="conversionsconvertdoubletodatetime-method"></a>ConvertDoubleToDateTime 方法

將雙 (的 OA 日期時間格式) 轉換為日期時間。 不同于 DateTime. Date.fromoadate，這不會擲回例外狀況。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a>參數

  - d  
    類型： [Double](/dotnet/api/system.double)  
    
    雙精度浮點數。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.datetime)  
日期時間。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[轉換類別](./conversions-class.md)

[轉換成員](./conversions-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
