---
description: 深入瞭解： InstanceParameters. MaxSessions 屬性
title: InstanceParameters. MaxSessions 屬性
TOCTitle: 'MaxSessions property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxsessions(v=EXCHG.10)
ms:contentKeyID: 55103557
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxSessions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2294a8de2e3603a638607efad5baaa6af6c1ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978308"
---
# <a name="instanceparametersmaxsessions-property"></a><span data-ttu-id="43ec1-103">InstanceParameters. MaxSessions 屬性</span><span class="sxs-lookup"><span data-stu-id="43ec1-103">InstanceParameters.MaxSessions property</span></span>

<span data-ttu-id="43ec1-104">取得或設定保留給此實例的會話資源數目。</span><span class="sxs-lookup"><span data-stu-id="43ec1-104">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="43ec1-105">會話資源直接對應至 JET_SESID。</span><span class="sxs-lookup"><span data-stu-id="43ec1-105">A session resource directly corresponds to a JET_SESID.</span></span>

<span data-ttu-id="43ec1-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43ec1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43ec1-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="43ec1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43ec1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="43ec1-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxSessions As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxSessions

instance.MaxSessions = value
```

``` csharp
public int MaxSessions { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="43ec1-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="43ec1-109">Property value</span></span>

<span data-ttu-id="43ec1-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="43ec1-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="43ec1-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43ec1-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43ec1-112">參考</span><span class="sxs-lookup"><span data-stu-id="43ec1-112">Reference</span></span>

[<span data-ttu-id="43ec1-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="43ec1-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="43ec1-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="43ec1-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="43ec1-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="43ec1-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
