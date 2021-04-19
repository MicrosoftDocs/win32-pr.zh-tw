---
description: 深入瞭解： VistaApi. JetOSSnapshotGetFreezeInfo 方法
title: 'VistaApi. JetOSSnapshotGetFreezeInfo 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84b8f33f1fcac280e8fee65c1092c8fccdec3b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974373"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a><span data-ttu-id="1280a-103">VistaApi. JetOSSnapshotGetFreezeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="1280a-103">VistaApi.JetOSSnapshotGetFreezeInfo method</span></span>

<span data-ttu-id="1280a-104">在任何指定的時間，取得屬於快照會話一部分的實例和資料庫清單。</span><span class="sxs-lookup"><span data-stu-id="1280a-104">Retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="1280a-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="1280a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1280a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1280a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1280a-107">語法</span><span class="sxs-lookup"><span data-stu-id="1280a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1280a-108">參數</span><span class="sxs-lookup"><span data-stu-id="1280a-108">Parameters</span></span>

  - <span data-ttu-id="1280a-109">快照集</span><span class="sxs-lookup"><span data-stu-id="1280a-109">snapshot</span></span>  
    <span data-ttu-id="1280a-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1280a-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="1280a-111">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1280a-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="1280a-112">numInstances</span><span class="sxs-lookup"><span data-stu-id="1280a-112">numInstances</span></span>  
    <span data-ttu-id="1280a-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1280a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1280a-114">傳回實例的數目。</span><span class="sxs-lookup"><span data-stu-id="1280a-114">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="1280a-115">執行個體</span><span class="sxs-lookup"><span data-stu-id="1280a-115">instances</span></span>  
    <span data-ttu-id="1280a-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="1280a-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="1280a-117">傳回實例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1280a-117">Returns information about the instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="1280a-118">grbit</span><span class="sxs-lookup"><span data-stu-id="1280a-118">grbit</span></span>  
    <span data-ttu-id="1280a-119">類型： [SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="1280a-119">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1280a-120">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="1280a-120">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="1280a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1280a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1280a-122">參考</span><span class="sxs-lookup"><span data-stu-id="1280a-122">Reference</span></span>

[<span data-ttu-id="1280a-123">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="1280a-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="1280a-124">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="1280a-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="1280a-125">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="1280a-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
