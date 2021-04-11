---
description: 深入瞭解： VistaApi. JetOSSnapshotTruncateLogInstance 方法
title: 'VistaApi. JetOSSnapshotTruncateLogInstance 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853012"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a><span data-ttu-id="893ad-103">VistaApi. JetOSSnapshotTruncateLogInstance 方法</span><span class="sxs-lookup"><span data-stu-id="893ad-103">VistaApi.JetOSSnapshotTruncateLogInstance method</span></span>

<span data-ttu-id="893ad-104">在快照會話期間截斷指定之實例的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="893ad-104">Truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="893ad-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="893ad-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="893ad-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="893ad-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="893ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="893ad-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="893ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="893ad-108">Parameters</span></span>

  - <span data-ttu-id="893ad-109">快照集</span><span class="sxs-lookup"><span data-stu-id="893ad-109">snapshot</span></span>  
    <span data-ttu-id="893ad-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="893ad-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="893ad-111">快照集識別碼。</span><span class="sxs-lookup"><span data-stu-id="893ad-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="893ad-112">instance</span><span class="sxs-lookup"><span data-stu-id="893ad-112">instance</span></span>  
    <span data-ttu-id="893ad-113">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="893ad-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="893ad-114">要 truncat 記錄檔的實例。</span><span class="sxs-lookup"><span data-stu-id="893ad-114">The instance to truncat the log for.</span></span>

<!-- end list -->

  - <span data-ttu-id="893ad-115">grbit</span><span class="sxs-lookup"><span data-stu-id="893ad-115">grbit</span></span>  
    <span data-ttu-id="893ad-116">類型： [SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="893ad-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="893ad-117">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="893ad-117">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="893ad-118">備註</span><span class="sxs-lookup"><span data-stu-id="893ad-118">Remarks</span></span>

<span data-ttu-id="893ad-119">只有在使用 [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) 選項建立快照集時，才應該呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="893ad-119">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="893ad-120">否則，在呼叫 [JetOSSnapshotThaw (JET_OSSNAPID，SnapshotThawGrbit) ](./api.jetossnapshotthaw-method.md)之後，快照集會話就會結束。</span><span class="sxs-lookup"><span data-stu-id="893ad-120">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="893ad-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="893ad-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="893ad-122">參考</span><span class="sxs-lookup"><span data-stu-id="893ad-122">Reference</span></span>

[<span data-ttu-id="893ad-123">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="893ad-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="893ad-124">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="893ad-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="893ad-125">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="893ad-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
