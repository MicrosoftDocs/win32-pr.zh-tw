---
description: 深入瞭解： JetOSSnapshotFreeze 方法
title: JetOSSnapshotFreeze 方法
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195023"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="052ba-103">JetOSSnapshotFreeze 方法</span><span class="sxs-lookup"><span data-stu-id="052ba-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="052ba-104">啟動快照集。</span><span class="sxs-lookup"><span data-stu-id="052ba-104">Starts a snapshot.</span></span> <span data-ttu-id="052ba-105">當快照集進行中時，引擎無法進行寫入磁片的活動。</span><span class="sxs-lookup"><span data-stu-id="052ba-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="052ba-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="052ba-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="052ba-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="052ba-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="052ba-108">語法</span><span class="sxs-lookup"><span data-stu-id="052ba-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="052ba-109">參數</span><span class="sxs-lookup"><span data-stu-id="052ba-109">Parameters</span></span>

  - <span data-ttu-id="052ba-110">快照集</span><span class="sxs-lookup"><span data-stu-id="052ba-110">snapshot</span></span>  
    <span data-ttu-id="052ba-111">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="052ba-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="052ba-112">快照會話。</span><span class="sxs-lookup"><span data-stu-id="052ba-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="052ba-113">numInstances</span><span class="sxs-lookup"><span data-stu-id="052ba-113">numInstances</span></span>  
    <span data-ttu-id="052ba-114">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="052ba-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="052ba-115">傳回屬於快照會話一部分的實例數目。</span><span class="sxs-lookup"><span data-stu-id="052ba-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="052ba-116">執行個體</span><span class="sxs-lookup"><span data-stu-id="052ba-116">instances</span></span>  
    <span data-ttu-id="052ba-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="052ba-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="052ba-118">傳回屬於快照集會話一部分之實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="052ba-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="052ba-119">grbit</span><span class="sxs-lookup"><span data-stu-id="052ba-119">grbit</span></span>  
    <span data-ttu-id="052ba-120">型別： [SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="052ba-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="052ba-121">快照集凍結選項。</span><span class="sxs-lookup"><span data-stu-id="052ba-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="052ba-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="052ba-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="052ba-123">參考</span><span class="sxs-lookup"><span data-stu-id="052ba-123">Reference</span></span>

[<span data-ttu-id="052ba-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="052ba-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="052ba-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="052ba-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="052ba-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="052ba-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
