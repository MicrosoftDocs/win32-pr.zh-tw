---
description: 深入瞭解： VistaApi. JetOSSnapshotEnd 方法
title: 'VistaApi. JetOSSnapshotEnd 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 291d83929940a9f66f4e16c5088e6ec08187f908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690804"
---
# <a name="vistaapijetossnapshotend-method"></a><span data-ttu-id="2fd12-103">VistaApi. JetOSSnapshotEnd 方法</span><span class="sxs-lookup"><span data-stu-id="2fd12-103">VistaApi.JetOSSnapshotEnd method</span></span>

<span data-ttu-id="2fd12-104">通知引擎快照會話已完成。</span><span class="sxs-lookup"><span data-stu-id="2fd12-104">Notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="2fd12-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="2fd12-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2fd12-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2fd12-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd12-107">語法</span><span class="sxs-lookup"><span data-stu-id="2fd12-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2fd12-108">參數</span><span class="sxs-lookup"><span data-stu-id="2fd12-108">Parameters</span></span>

  - <span data-ttu-id="2fd12-109">快照集</span><span class="sxs-lookup"><span data-stu-id="2fd12-109">snapshot</span></span>  
    <span data-ttu-id="2fd12-110">類型： [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2fd12-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="2fd12-111">快照集會話的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fd12-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="2fd12-112">grbit</span><span class="sxs-lookup"><span data-stu-id="2fd12-112">grbit</span></span>  
    <span data-ttu-id="2fd12-113">類型： [SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)的類型。</span><span class="sxs-lookup"><span data-stu-id="2fd12-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2fd12-114">快照集結束選項。</span><span class="sxs-lookup"><span data-stu-id="2fd12-114">Snapshot end options.</span></span>

## <a name="see-also"></a><span data-ttu-id="2fd12-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fd12-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2fd12-116">參考</span><span class="sxs-lookup"><span data-stu-id="2fd12-116">Reference</span></span>

[<span data-ttu-id="2fd12-117">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="2fd12-117">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="2fd12-118">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="2fd12-118">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="2fd12-119">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="2fd12-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
