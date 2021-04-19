---
description: '深入瞭解： CimMofDeserializer. DeserializeInstances 方法 (Byte []、UInt32、IEnumerable <CimClass> 、OnClassNeeded、GetIncludedFileContent) '
title: 'CimMofDeserializer. DeserializeInstances 方法 (Byte []、UInt32、IEnumerable (CimClass) 、OnClassNeeded、GetIncludedFileContent)  (Microsoft.) '
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 081c6d028abdb341d75ff57758c703458fd0b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998054"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a>CimMofDeserializer. DeserializeInstances 方法 (Byte \[ \] 、UInt32、IEnumerable \<CimClass\> 、OnClassNeeded、GetIncludedFileContent) 

根據序列化資料、父 CIM 類別的集合和回呼，將 CIM 實例還原序列化。

**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> cimClasses,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ cimClasses,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref *
        cimClasses:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger,
    cimClasses As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>參數

  - serializedData  
    類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    包含序列化資料的緩衝區。

<!-- end list -->

  - Offset  
    類型： [system.object](/dotnet/api/system.uint32?view=netframework-4.8)
    
    開始讀取資料之位置的位元組位移。 當方法傳回時，位移將指向已還原序列化之實例之後的下一個位元組。

<!-- end list -->

  - cimClasses  
    類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    父 CIM 類別的選擇性快取。

<!-- end list -->

  - onClassNeededCallback  
    類型： [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    回呼函數，用來在還原序列化期間提供要求的類別物件。

<!-- end list -->

  - getIncludedFileCallback  
    類型： [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    回呼函數，用來提供指定檔案的檔案緩衝區內容。

#### <a name="return-value"></a>傳回值

類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) 。\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

可以用來列舉 CIM 類別的[IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)介面。

## <a name="see-also"></a>另請參閱

[CimInstance 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[。序列化命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
