---
description: 深入瞭解： VistaApi. JetOSSnapshotPrepareInstance 方法
title: 'VistaApi. JetOSSnapshotPrepareInstance 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115640"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="b43de-103">VistaApi. JetOSSnapshotPrepareInstance 方法</span><span class="sxs-lookup"><span data-stu-id="b43de-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="b43de-104">選取要成為快照會話一部分的特定實例。</span><span class="sxs-lookup"><span data-stu-id="b43de-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="b43de-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="b43de-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b43de-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b43de-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b43de-107">語法</span><span class="sxs-lookup"><span data-stu-id="b43de-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b43de-108">參數</span><span class="sxs-lookup"><span data-stu-id="b43de-108">Parameters</span></span>

  - <span data-ttu-id="b43de-109">快照集</span><span class="sxs-lookup"><span data-stu-id="b43de-109">snapshot</span></span>  
    <span data-ttu-id="b43de-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b43de-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="b43de-111">快照集識別碼。</span><span class="sxs-lookup"><span data-stu-id="b43de-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="b43de-112">instance</span><span class="sxs-lookup"><span data-stu-id="b43de-112">instance</span></span>  
    <span data-ttu-id="b43de-113">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b43de-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b43de-114">要加入至快照集的實例。</span><span class="sxs-lookup"><span data-stu-id="b43de-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="b43de-115">grbit</span><span class="sxs-lookup"><span data-stu-id="b43de-115">grbit</span></span>  
    <span data-ttu-id="b43de-116">類型： [SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="b43de-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b43de-117">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="b43de-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="b43de-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b43de-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b43de-119">參考</span><span class="sxs-lookup"><span data-stu-id="b43de-119">Reference</span></span>

[<span data-ttu-id="b43de-120">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="b43de-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="b43de-121">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="b43de-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="b43de-122">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="b43de-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
