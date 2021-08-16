---
description: '深入瞭解： CimInstance. SetCimSessionComputerName 方法 (字串) '
title: CimInstance.SetCimSessionComputerName 方法 (Microsoft.Management.Infrastructure)
TOCTitle: CimInstance.SetCimSessionComputerName method (Microsoft.Management.Infrastructure)
ms:assetid: M:Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName(System.String)
ms.date: 11/12/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
- Microsoft::Management::Infrastructure::CimInstance::SetCimSessionComputerName
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c3f3c3cbe93710f5f9a796463539ad754c1f2e50ce5524c90a5f639021e716bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131110"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a>CimInstance. SetCimSessionComputerName 方法 (字串) 

設定用於 CIM 會話的電腦名稱稱。

**命名空間：**   [Microsoft. 管理. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public void SetCimSessionComputerName(
    string computerName
)
```

``` c++
public:
void SetCimSessionComputerName(
    String^ computerName
)
```

``` fsharp
member SetCimSessionComputerName : 
        computerName:string -> unit
```

``` vb
Public Sub SetCimSessionComputerName (
    computerName As String
)
```

#### <a name="parameters"></a>參數

  - computerName  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    用於 CIM 會話的電腦名稱稱。 如果目前的實例只是用戶端，或從 localhost 取出實例，則 **為 null** 。

## <a name="see-also"></a>另請參閱

[CimInstance 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))  
[Microsoft. 基礎結構命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))
