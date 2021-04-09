---
description: 深入瞭解： InstanceParameters. TempDirectory 屬性
title: InstanceParameters. TempDirectory 屬性
TOCTitle: 'TempDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.tempdirectory(v=EXCHG.10)
ms:contentKeyID: 55103324
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_TempDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.TempDirectory
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0bbe31b7f437f045f601b18daf92877784d58512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945367"
---
# <a name="instanceparameterstempdirectory-property"></a><span data-ttu-id="3b8d9-103">InstanceParameters. TempDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="3b8d9-103">InstanceParameters.TempDirectory property</span></span>

<span data-ttu-id="3b8d9-104">取得或設定資料夾的相對或絕對檔案系統路徑，其中將包含實例的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="3b8d9-104">Gets or sets the relative or absolute file system path of the folder that will contain the temporary database for the instance.</span></span>

<span data-ttu-id="3b8d9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3b8d9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3b8d9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3b8d9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3b8d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b8d9-107">Syntax</span></span>

``` vb
'Declaration
Public Property TempDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.TempDirectory

instance.TempDirectory = value
```

``` csharp
public string TempDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3b8d9-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="3b8d9-108">Property value</span></span>

<span data-ttu-id="3b8d9-109">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3b8d9-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3b8d9-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b8d9-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3b8d9-111">參考</span><span class="sxs-lookup"><span data-stu-id="3b8d9-111">Reference</span></span>

[<span data-ttu-id="3b8d9-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="3b8d9-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="3b8d9-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="3b8d9-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="3b8d9-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3b8d9-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
