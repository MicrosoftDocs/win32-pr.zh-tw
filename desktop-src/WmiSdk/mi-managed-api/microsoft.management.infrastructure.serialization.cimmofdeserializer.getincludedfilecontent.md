---
description: '深入瞭解： CimMofDeserializer. GetIncludedFileContent 委派 (字串) '
title: CimMofDeserializer)  (的 GetIncludedFileContent 委派
TOCTitle: CimMofDeserializer.GetIncludedFileContent delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::GetIncludedFileContent
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: cb922d785da7d01de93adec56cefee29785210d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973699"
---
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a>CimMofDeserializer. GetIncludedFileContent 委派 (字串) 

表示以位元組陣列形式取出檔案內容的回呼。

**命名空間：**   [Microsoft. 管理結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構  

## <a name="syntax"></a>語法

``` csharp
public delegate byte[] GetIncludedFileContent(
    string fileName
)
```

``` c++
public delegate array<unsigned char>^ GetIncludedFileContent(
    String^ fileName
)
```

``` fsharp
type GetIncludedFileContent = 
    delegate of 
        fileName:string -> byte[]
```

``` vb
Public Delegate Function GetIncludedFileContent (
    fileName As String
) As Byte()
```

#### <a name="parameters"></a>參數

  - fileName  
    類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)
    
    檔案名，包括路徑。

#### <a name="return-value"></a>傳回值

類型： [system.string](/dotnet/api/system.byte?view=netframework-4.8)\[\]

以位元組陣列的形式傳回檔案的內容。

## <a name="see-also"></a>另請參閱

[管理基礎結構。序列化](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
