---
description: 深入瞭解： VistaApi. JetOSSnapshotTruncateLog 方法
title: 'VistaApi. JetOSSnapshotTruncateLog 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973797"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="28d49-103">VistaApi. JetOSSnapshotTruncateLog 方法</span><span class="sxs-lookup"><span data-stu-id="28d49-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="28d49-104">針對屬於快照會話一部分的所有實例啟用記錄截斷。</span><span class="sxs-lookup"><span data-stu-id="28d49-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="28d49-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="28d49-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="28d49-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="28d49-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28d49-107">語法</span><span class="sxs-lookup"><span data-stu-id="28d49-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="28d49-108">參數</span><span class="sxs-lookup"><span data-stu-id="28d49-108">Parameters</span></span>

  - <span data-ttu-id="28d49-109">快照集</span><span class="sxs-lookup"><span data-stu-id="28d49-109">snapshot</span></span>  
    <span data-ttu-id="28d49-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="28d49-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="28d49-111">快照集識別碼。</span><span class="sxs-lookup"><span data-stu-id="28d49-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="28d49-112">grbit</span><span class="sxs-lookup"><span data-stu-id="28d49-112">grbit</span></span>  
    <span data-ttu-id="28d49-113">類型： [SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="28d49-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="28d49-114">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="28d49-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="28d49-115">備註</span><span class="sxs-lookup"><span data-stu-id="28d49-115">Remarks</span></span>

<span data-ttu-id="28d49-116">只有在使用 [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) 選項建立快照集時，才應該呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="28d49-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="28d49-117">否則，在呼叫 [JetOSSnapshotThaw (JET_OSSNAPID，SnapshotThawGrbit) ](./api.jetossnapshotthaw-method.md)之後，快照集會話就會結束。</span><span class="sxs-lookup"><span data-stu-id="28d49-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="28d49-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28d49-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28d49-119">參考</span><span class="sxs-lookup"><span data-stu-id="28d49-119">Reference</span></span>

[<span data-ttu-id="28d49-120">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="28d49-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="28d49-121">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="28d49-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="28d49-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="28d49-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
