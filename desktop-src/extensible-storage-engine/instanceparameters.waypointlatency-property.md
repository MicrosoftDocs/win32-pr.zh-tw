---
description: 深入瞭解： InstanceParameters. WaypointLatency 屬性
title: InstanceParameters. WaypointLatency 屬性
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976576"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="544b3-103">InstanceParameters. WaypointLatency 屬性</span><span class="sxs-lookup"><span data-stu-id="544b3-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="544b3-104">取得或設定 esent 將延遲資料庫排清之記錄檔的數目。</span><span class="sxs-lookup"><span data-stu-id="544b3-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="544b3-105">如果失敗導致記錄檔遺失，這可以用來提高資料庫復原能力。</span><span class="sxs-lookup"><span data-stu-id="544b3-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="544b3-106">Windows 7 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="544b3-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="544b3-107">在 Windows XP、Windows Server 2003、Windows Vista 和 Windows Server 2008 上略過。</span><span class="sxs-lookup"><span data-stu-id="544b3-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="544b3-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="544b3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="544b3-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="544b3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="544b3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="544b3-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="544b3-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="544b3-111">Property value</span></span>

<span data-ttu-id="544b3-112">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="544b3-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="544b3-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="544b3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="544b3-114">參考</span><span class="sxs-lookup"><span data-stu-id="544b3-114">Reference</span></span>

[<span data-ttu-id="544b3-115">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="544b3-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="544b3-116">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="544b3-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="544b3-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="544b3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
