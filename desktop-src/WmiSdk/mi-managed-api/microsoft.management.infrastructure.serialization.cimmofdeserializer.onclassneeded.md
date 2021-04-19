---
description: '深入瞭解： CimMofDeserializer. OnClassNeeded 委派 (字串、字串、字串) '
title: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 50e107c09eccde03446278516a1f125f4ad86022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973904"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a>CimMofDeserializer。 OnClassNeeded 委派 (字串、字串、字串) 

表示用來抓取指定伺服器、命名空間和類別名稱之 CIM 類別的回呼。

**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a>參數

  - serverName  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    CIM 類別的伺服器名稱。

<!-- end list -->

  - namespaceName  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    CIM 類別的命名空間名稱。

<!-- end list -->

  - className  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    CIM 類別的類別名稱。

#### <a name="return-value"></a>傳回值

Type： [CimClass 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))

傳回對應至指定引數的 CIM 類別，如果找不到類別，則 **為 null** 。

## <a name="see-also"></a>另請參閱

[管理基礎結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
