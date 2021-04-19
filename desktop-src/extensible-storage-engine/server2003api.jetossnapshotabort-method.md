---
description: 深入瞭解： Server2003Api. JetOSSnapshotAbort 方法
title: 'Server2003Api. JetOSSnapshotAbort 方法 (Server2003 的) '
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971056"
---
# <a name="server2003apijetossnapshotabort-method"></a><span data-ttu-id="1f0fa-103">Server2003Api. JetOSSnapshotAbort 方法</span><span class="sxs-lookup"><span data-stu-id="1f0fa-103">Server2003Api.JetOSSnapshotAbort method</span></span>

<span data-ttu-id="1f0fa-104">通知引擎在凍結期間結束時，它可以繼續正常 IO 作業，並以失敗的快照集結束。</span><span class="sxs-lookup"><span data-stu-id="1f0fa-104">Notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="1f0fa-105">**命名空間：**  [Microsoft Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f0fa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="1f0fa-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1f0fa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0fa-107">語法</span><span class="sxs-lookup"><span data-stu-id="1f0fa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1f0fa-108">參數</span><span class="sxs-lookup"><span data-stu-id="1f0fa-108">Parameters</span></span>

  - <span data-ttu-id="1f0fa-109">snapid</span><span class="sxs-lookup"><span data-stu-id="1f0fa-109">snapid</span></span>  
    <span data-ttu-id="1f0fa-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f0fa-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="1f0fa-111">快照會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f0fa-111">Identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f0fa-112">grbit</span><span class="sxs-lookup"><span data-stu-id="1f0fa-112">grbit</span></span>  
    <span data-ttu-id="1f0fa-113">型別： [Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1f0fa-113">Type: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1f0fa-114">此呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="1f0fa-114">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f0fa-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f0fa-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f0fa-116">參考</span><span class="sxs-lookup"><span data-stu-id="1f0fa-116">Reference</span></span>

[<span data-ttu-id="1f0fa-117">Server2003Api 類別</span><span class="sxs-lookup"><span data-stu-id="1f0fa-117">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="1f0fa-118">Server2003Api 成員</span><span class="sxs-lookup"><span data-stu-id="1f0fa-118">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="1f0fa-119">Server2003 命名空間。</span><span class="sxs-lookup"><span data-stu-id="1f0fa-119">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
