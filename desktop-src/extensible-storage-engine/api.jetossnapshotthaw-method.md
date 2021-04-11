---
description: 深入瞭解： JetOSSnapshotThaw 方法
title: JetOSSnapshotThaw 方法
TOCTitle: 'JetOSSnapshotThaw method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.SnapshotThawGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotthaw(v=EXCHG.10)
ms:contentKeyID: 55100780
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3fe0bc04586dddade7a9723720bbd3c994c516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852451"
---
# <a name="apijetossnapshotthaw-method"></a><span data-ttu-id="d5461-103">JetOSSnapshotThaw 方法</span><span class="sxs-lookup"><span data-stu-id="d5461-103">Api.JetOSSnapshotThaw method</span></span>

<span data-ttu-id="d5461-104">通知引擎可在凍結期間之後繼續正常 IO 作業，以及成功的快照集。</span><span class="sxs-lookup"><span data-stu-id="d5461-104">Notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="d5461-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d5461-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d5461-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d5461-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d5461-107">語法</span><span class="sxs-lookup"><span data-stu-id="d5461-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotThaw ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotThawGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotThawGrbitApi.JetOSSnapshotThaw(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotThaw(
    JET_OSSNAPID snapshot,
    SnapshotThawGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d5461-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5461-108">Parameters</span></span>

  - <span data-ttu-id="d5461-109">快照集</span><span class="sxs-lookup"><span data-stu-id="d5461-109">snapshot</span></span>  
    <span data-ttu-id="d5461-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d5461-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="d5461-111">快照集的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5461-111">The ID of the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="d5461-112">grbit</span><span class="sxs-lookup"><span data-stu-id="d5461-112">grbit</span></span>  
    <span data-ttu-id="d5461-113">型別： [SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="d5461-113">Type: [Microsoft.Isam.Esent.Interop.SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d5461-114">解除凍結選項。</span><span class="sxs-lookup"><span data-stu-id="d5461-114">Thaw options.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5461-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5461-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d5461-116">參考</span><span class="sxs-lookup"><span data-stu-id="d5461-116">Reference</span></span>

[<span data-ttu-id="d5461-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="d5461-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d5461-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="d5461-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d5461-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d5461-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
