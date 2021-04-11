---
description: 深入瞭解： JetGetLock 方法
title: JetGetLock 方法
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847849"
---
# <a name="apijetgetlock-method"></a><span data-ttu-id="e3aed-103">JetGetLock 方法</span><span class="sxs-lookup"><span data-stu-id="e3aed-103">Api.JetGetLock method</span></span>

<span data-ttu-id="e3aed-104">明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。</span><span class="sxs-lookup"><span data-stu-id="e3aed-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="e3aed-105">一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。</span><span class="sxs-lookup"><span data-stu-id="e3aed-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="e3aed-106">由於記錄版本控制，通常不需要讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="e3aed-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="e3aed-107">不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</span><span class="sxs-lookup"><span data-stu-id="e3aed-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="e3aed-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3aed-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3aed-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e3aed-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3aed-110">語法</span><span class="sxs-lookup"><span data-stu-id="e3aed-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e3aed-111">參數</span><span class="sxs-lookup"><span data-stu-id="e3aed-111">Parameters</span></span>

  - <span data-ttu-id="e3aed-112">sesid</span><span class="sxs-lookup"><span data-stu-id="e3aed-112">sesid</span></span>  
    <span data-ttu-id="e3aed-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3aed-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e3aed-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e3aed-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3aed-115">tableid</span><span class="sxs-lookup"><span data-stu-id="e3aed-115">tableid</span></span>  
    <span data-ttu-id="e3aed-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3aed-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e3aed-117">要使用的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e3aed-117">The cursor to use.</span></span> <span data-ttu-id="e3aed-118">將會取得目前記錄的鎖定。</span><span class="sxs-lookup"><span data-stu-id="e3aed-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3aed-119">grbit</span><span class="sxs-lookup"><span data-stu-id="e3aed-119">grbit</span></span>  
    <span data-ttu-id="e3aed-120">型別： [GetLockGrbit](./getlockgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="e3aed-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e3aed-121">鎖定選項：使用此選項來指定要取得的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="e3aed-121">Lock options, use this to specify which type of lock to obtain.</span></span>

## <a name="see-also"></a><span data-ttu-id="e3aed-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3aed-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3aed-123">參考</span><span class="sxs-lookup"><span data-stu-id="e3aed-123">Reference</span></span>

[<span data-ttu-id="e3aed-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e3aed-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e3aed-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e3aed-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e3aed-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e3aed-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
