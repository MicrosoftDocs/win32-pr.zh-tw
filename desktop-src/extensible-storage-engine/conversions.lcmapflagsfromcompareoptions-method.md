---
description: 深入瞭解： LCMapFlagsFromCompareOptions 方法
title: LCMapFlagsFromCompareOptions 方法
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976771"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>LCMapFlagsFromCompareOptions 方法

提供 CompareOptions，並將其轉換成 LCMapString 的旗標。 忽略未知的選項。

此 API 不符合 CLS 規範。 

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>參數

  - compareOptions  
    類型： [CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    要轉換的選項。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.uint32)  
符合比較選項的 LCMapString 旗標。 系統會忽略不支援的選項。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[轉換類別](./conversions-class.md)

[轉換成員](./conversions-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
