---
description: 深入瞭解： InstanceParameters. EnableDBScanSerialization 屬性
title: InstanceParameters. EnableDBScanSerialization 屬性
TOCTitle: 'EnableDBScanSerialization property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscanserialization(v=EXCHG.10)
ms:contentKeyID: 55103555
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c514218b43d1f291abc01d384cdb47f339163cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318748"
---
# <a name="instanceparametersenabledbscanserialization-property"></a><span data-ttu-id="b53e0-103">InstanceParameters. EnableDBScanSerialization 屬性</span><span class="sxs-lookup"><span data-stu-id="b53e0-103">InstanceParameters.EnableDBScanSerialization property</span></span>

<span data-ttu-id="b53e0-104">取得或設定值，指出是否為共用相同磁片的資料庫啟用資料庫維護序列化。</span><span class="sxs-lookup"><span data-stu-id="b53e0-104">Gets or sets a value indicating whether database Maintenance serialization is enabled for databases sharing the same disk.</span></span>

<span data-ttu-id="b53e0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b53e0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b53e0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b53e0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b53e0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b53e0-107">Syntax</span></span>

``` vb
'Declaration
Public Property EnableDBScanSerialization As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableDBScanSerialization

instance.EnableDBScanSerialization = value
```

``` csharp
public bool EnableDBScanSerialization { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b53e0-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="b53e0-108">Property value</span></span>

<span data-ttu-id="b53e0-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b53e0-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b53e0-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b53e0-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b53e0-111">參考</span><span class="sxs-lookup"><span data-stu-id="b53e0-111">Reference</span></span>

[<span data-ttu-id="b53e0-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="b53e0-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b53e0-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="b53e0-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="b53e0-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b53e0-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
