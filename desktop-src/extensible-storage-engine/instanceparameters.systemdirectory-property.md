---
description: 深入瞭解： InstanceParameters.SystemDirectory 屬性
title: InstanceParameters.SystemDirectory 屬性
TOCTitle: 'SystemDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.systemdirectory(v=EXCHG.10)
ms:contentKeyID: 55103561
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_SystemDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c0478b4b9d626610549240d58f3289fc24d10aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981048"
---
# <a name="instanceparameterssystemdirectory-property"></a><span data-ttu-id="855a9-103">InstanceParameters.SystemDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="855a9-103">InstanceParameters.SystemDirectory property</span></span>

<span data-ttu-id="855a9-104">取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的檢查點檔案。</span><span class="sxs-lookup"><span data-stu-id="855a9-104">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span>

<span data-ttu-id="855a9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="855a9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="855a9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="855a9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="855a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="855a9-107">Syntax</span></span>

``` vb
'Declaration
Public Property SystemDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.SystemDirectory

instance.SystemDirectory = value
```

``` csharp
public string SystemDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="855a9-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="855a9-108">Property value</span></span>

<span data-ttu-id="855a9-109">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="855a9-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="855a9-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="855a9-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="855a9-111">參考</span><span class="sxs-lookup"><span data-stu-id="855a9-111">Reference</span></span>

[<span data-ttu-id="855a9-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="855a9-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="855a9-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="855a9-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="855a9-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="855a9-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
