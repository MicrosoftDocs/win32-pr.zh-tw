---
description: 深入瞭解： TryGetLock 方法
title: TryGetLock 方法
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ecd4e0e66226d438b4e5a78b2397f5637154096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195017"
---
# <a name="apitrygetlock-method"></a><span data-ttu-id="f84d9-103">TryGetLock 方法</span><span class="sxs-lookup"><span data-stu-id="f84d9-103">Api.TryGetLock method</span></span>

<span data-ttu-id="f84d9-104">明確保留更新資料列、寫入鎖定，或明確防止任何其他會話、讀取鎖定的資料列更新的能力。</span><span class="sxs-lookup"><span data-stu-id="f84d9-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="f84d9-105">一般來說，資料列寫入鎖定是以隱含方式取得，因為更新資料列的結果。</span><span class="sxs-lookup"><span data-stu-id="f84d9-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="f84d9-106">由於記錄版本控制，通常不需要讀取鎖定。</span><span class="sxs-lookup"><span data-stu-id="f84d9-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="f84d9-107">不過，在某些情況下，交易可能會想要明確地鎖定資料列以強制執行序列化，或確定後續作業將會成功。</span><span class="sxs-lookup"><span data-stu-id="f84d9-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="f84d9-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f84d9-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f84d9-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f84d9-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f84d9-110">語法</span><span class="sxs-lookup"><span data-stu-id="f84d9-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f84d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="f84d9-111">Parameters</span></span>

  - <span data-ttu-id="f84d9-112">sesid</span><span class="sxs-lookup"><span data-stu-id="f84d9-112">sesid</span></span>  
    <span data-ttu-id="f84d9-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f84d9-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f84d9-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f84d9-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f84d9-115">tableid</span><span class="sxs-lookup"><span data-stu-id="f84d9-115">tableid</span></span>  
    <span data-ttu-id="f84d9-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f84d9-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f84d9-117">要使用的資料指標。</span><span class="sxs-lookup"><span data-stu-id="f84d9-117">The cursor to use.</span></span> <span data-ttu-id="f84d9-118">將會取得目前記錄的鎖定。</span><span class="sxs-lookup"><span data-stu-id="f84d9-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="f84d9-119">grbit</span><span class="sxs-lookup"><span data-stu-id="f84d9-119">grbit</span></span>  
    <span data-ttu-id="f84d9-120">型別： [GetLockGrbit](./getlockgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="f84d9-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f84d9-121">鎖定選項：使用此選項來指定要取得的鎖定類型。</span><span class="sxs-lookup"><span data-stu-id="f84d9-121">Lock options, use this to specify which type of lock to obtain.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f84d9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f84d9-122">Return value</span></span>

<span data-ttu-id="f84d9-123">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f84d9-123">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f84d9-124">如果已取得鎖定，則為 True，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="f84d9-124">True if the lock was obtained, false otherwise.</span></span> <span data-ttu-id="f84d9-125">如果遇到未預期的錯誤，則會擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="f84d9-125">An exception is thrown if an unexpected error is encountered.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f84d9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f84d9-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f84d9-127">參考</span><span class="sxs-lookup"><span data-stu-id="f84d9-127">Reference</span></span>

[<span data-ttu-id="f84d9-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f84d9-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f84d9-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f84d9-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f84d9-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f84d9-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
