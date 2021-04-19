---
description: 深入瞭解： InstanceParameters. EnableIndexChecking 屬性
title: InstanceParameters. EnableIndexChecking 屬性
TOCTitle: 'EnableIndexChecking property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enableindexchecking(v=EXCHG.10)
ms:contentKeyID: 55103567
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableIndexChecking
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a3090c1e5c1e42aca3758496b1367f3932e123c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975238"
---
# <a name="instanceparametersenableindexchecking-property"></a><span data-ttu-id="6e0fb-103">InstanceParameters. EnableIndexChecking 屬性</span><span class="sxs-lookup"><span data-stu-id="6e0fb-103">InstanceParameters.EnableIndexChecking property</span></span>

<span data-ttu-id="6e0fb-104">取得或設定值，指出 [JetAttachDatabase (JET_SESID、String、AttachDatabaseGrbit) ](./api.jetattachdatabase-method.md) 是否將檢查在作業系統中使用舊版 NLS 程式庫所建立的索引。</span><span class="sxs-lookup"><span data-stu-id="6e0fb-104">Gets or sets a value indicating whether [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will check for indexes that were build using an older version of the NLS library in the operating system.</span></span>

<span data-ttu-id="6e0fb-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e0fb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e0fb-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6e0fb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0fb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e0fb-107">Syntax</span></span>

``` vb
'Declaration
Public Property EnableIndexChecking As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableIndexChecking

instance.EnableIndexChecking = value
```

``` csharp
public bool EnableIndexChecking { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6e0fb-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="6e0fb-108">Property value</span></span>

<span data-ttu-id="6e0fb-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6e0fb-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e0fb-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e0fb-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e0fb-111">參考</span><span class="sxs-lookup"><span data-stu-id="6e0fb-111">Reference</span></span>

[<span data-ttu-id="6e0fb-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="6e0fb-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6e0fb-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="6e0fb-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6e0fb-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6e0fb-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
