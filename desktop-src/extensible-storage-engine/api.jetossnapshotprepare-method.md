---
description: 深入瞭解： JetOSSnapshotPrepare 方法
title: JetOSSnapshotPrepare 方法
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195022"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="0a435-103">JetOSSnapshotPrepare 方法</span><span class="sxs-lookup"><span data-stu-id="0a435-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="0a435-104">開始快照集會話的準備工作。</span><span class="sxs-lookup"><span data-stu-id="0a435-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="0a435-105">快照集會話是一個短暫的時間間隔，在此時間間隔中，引擎不會將任何寫入 Io 發出至磁片，因此引擎可以在由快照寫入器驅動) 時，參與磁片區快照集會話 (。</span><span class="sxs-lookup"><span data-stu-id="0a435-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="0a435-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a435-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a435-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0a435-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a435-108">語法</span><span class="sxs-lookup"><span data-stu-id="0a435-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0a435-109">參數</span><span class="sxs-lookup"><span data-stu-id="0a435-109">Parameters</span></span>

  - <span data-ttu-id="0a435-110">快照集</span><span class="sxs-lookup"><span data-stu-id="0a435-110">snapshot</span></span>  
    <span data-ttu-id="0a435-111">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0a435-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="0a435-112">傳回快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a435-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="0a435-113">grbit</span><span class="sxs-lookup"><span data-stu-id="0a435-113">grbit</span></span>  
    <span data-ttu-id="0a435-114">型別： [SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="0a435-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0a435-115">快照集選項。</span><span class="sxs-lookup"><span data-stu-id="0a435-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a435-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a435-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a435-117">參考</span><span class="sxs-lookup"><span data-stu-id="0a435-117">Reference</span></span>

[<span data-ttu-id="0a435-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="0a435-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0a435-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="0a435-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0a435-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0a435-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
