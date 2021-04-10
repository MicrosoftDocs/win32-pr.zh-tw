---
description: 深入瞭解： CompareOptionsFromLCMapFlags 方法
title: CompareOptionsFromLCMapFlags 方法
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191664"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>CompareOptionsFromLCMapFlags 方法

針對 LCMapFlags 指定旗標，將它們轉換成比較選項。 忽略未知的選項。

此 API 不符合 CLS 規範。 

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>參數

  - lcmapFlags  
    類型： [system.object](/dotnet/api/system.uint32)  
    
    LCMapString 旗標。

#### <a name="return-value"></a>傳回值

類型： [CompareOptions](/dotnet/api/system.globalization.compareoptions)  
描述 (已知) 旗標的 CompareOptions。  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[轉換類別](./conversions-class.md)

[轉換成員](./conversions-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
