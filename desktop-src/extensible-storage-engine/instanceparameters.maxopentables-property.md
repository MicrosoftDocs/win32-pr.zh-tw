---
description: 深入瞭解： InstanceParameters. MaxOpenTables 屬性
title: InstanceParameters. MaxOpenTables 屬性
TOCTitle: 'MaxOpenTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxopentables(v=EXCHG.10)
ms:contentKeyID: 55107442
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxOpenTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxOpenTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 623d2f1fe536fb2b5916c96e97de8904fa5a7c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975796"
---
# <a name="instanceparametersmaxopentables-property"></a><span data-ttu-id="05801-103">InstanceParameters. MaxOpenTables 屬性</span><span class="sxs-lookup"><span data-stu-id="05801-103">InstanceParameters.MaxOpenTables property</span></span>

<span data-ttu-id="05801-104">取得或設定保留給此實例的 B + 樹系資源數目。</span><span class="sxs-lookup"><span data-stu-id="05801-104">Gets or sets the number of B+ Tree resources reserved for this instance.</span></span>

<span data-ttu-id="05801-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05801-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05801-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="05801-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05801-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05801-107">Syntax</span></span>

``` vb
'Declaration
Public Property MaxOpenTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxOpenTables

instance.MaxOpenTables = value
```

``` csharp
public int MaxOpenTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="05801-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="05801-108">Property value</span></span>

<span data-ttu-id="05801-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="05801-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="05801-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05801-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05801-111">參考</span><span class="sxs-lookup"><span data-stu-id="05801-111">Reference</span></span>

[<span data-ttu-id="05801-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="05801-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="05801-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="05801-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="05801-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="05801-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
