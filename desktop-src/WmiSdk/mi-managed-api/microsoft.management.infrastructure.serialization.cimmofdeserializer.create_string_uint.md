---
description: 深入瞭解： CimMofDeserializer (字串，UInt32) 的 Create 方法
title: CimMofDeserializer.Create 方法 (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.Create method (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create(System.String,System.UInt32)
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
- Microsoft::Management::Infrastructure::.Serialization::CimMofDeserializer::Create
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: e8a89c628abcc9fa9b8ac54d75493c8a385ef64bddd257bd3dc193b7e04c71aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050666"
---
# <a name="cimmofdeserializercreate-method-string-uint32"></a>CimMofDeserializer： Create 方法 (String，UInt32) 

根據指定的格式和旗標，建立並初始化自訂還原序列化。

**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public static CimMofDeserializer Create(
    string format,
    uint flags
)
```

``` c++
public:
static CimMofDeserializer^ Create(
    String^ format,
    unsigned int flags
)
```

``` fsharp
static member Create : 
        format:string *
        flags:uint32 -> CimMofDeserializer
```

``` vb
Public Shared Function Create (
    format As String,
    flags As UInteger
) As CimMofDeserializer
```

#### <a name="parameters"></a>參數

  - format  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    序列化格式。 僅支援 "MI_XML"。

<!-- end list -->

  - flags  
    類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)
    
    序列化旗標。 必須是 0。

#### <a name="return-value"></a>傳回值

型別： [CimMofDeserializer。](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)

新建立的還原序列化物件。

## <a name="see-also"></a>另請參閱

[CimMofDeserializer 類別](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
。[序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
