---
description: '深入瞭解： CimMofDeserializer. DeserializeClasses 方法 (Byte []，UInt32) '
title: 'CimMofDeserializer. DeserializeClasses 方法 (Byte []、UInt32)  (。序列化) '
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 983fa9e8fe36b872d05c3140c74f572b7d1ebf50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510867"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a>CimMofDeserializer. DeserializeClasses 方法 (Byte \[ \] ，UInt32) 

根據序列化資料將 CIM 類別還原序列化。

**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>參數

  - serializedData  
    類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    包含序列化資料的緩衝區。

<!-- end list -->

  - Offset  
    類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)
    
    開始讀取資料之位置的位元組位移。 當方法傳回時，位移會指向還原序列化類別之後的下一個位元組。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。

## <a name="see-also"></a>另請參閱

[CimClass 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
