---
description: 深入瞭解： JetEscrowUpdate 方法
title: JetEscrowUpdate 方法
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985404"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="82799-103">JetEscrowUpdate 方法</span><span class="sxs-lookup"><span data-stu-id="82799-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="82799-104">在一個資料行上執行不可部分完成的加法運算。</span><span class="sxs-lookup"><span data-stu-id="82799-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="82799-105">此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="82799-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="82799-106">另請參閱 [EscrowUpdate (JET_SESID、JET_TABLEID、JET_COLUMNID、Int32) ](./api.escrowupdate-method.md)。</span><span class="sxs-lookup"><span data-stu-id="82799-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="82799-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82799-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82799-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="82799-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82799-109">語法</span><span class="sxs-lookup"><span data-stu-id="82799-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="82799-110">參數</span><span class="sxs-lookup"><span data-stu-id="82799-110">Parameters</span></span>

  - <span data-ttu-id="82799-111">sesid</span><span class="sxs-lookup"><span data-stu-id="82799-111">sesid</span></span>  
    <span data-ttu-id="82799-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82799-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="82799-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="82799-113">The session to use.</span></span> <span data-ttu-id="82799-114">會話必須在交易中。</span><span class="sxs-lookup"><span data-stu-id="82799-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-115">tableid</span><span class="sxs-lookup"><span data-stu-id="82799-115">tableid</span></span>  
    <span data-ttu-id="82799-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82799-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="82799-117">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="82799-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-118">columnid</span><span class="sxs-lookup"><span data-stu-id="82799-118">columnid</span></span>  
    <span data-ttu-id="82799-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="82799-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="82799-120">要更新的資料行。</span><span class="sxs-lookup"><span data-stu-id="82799-120">The column to update.</span></span> <span data-ttu-id="82799-121">這必須是可更新的可更新資料行。</span><span class="sxs-lookup"><span data-stu-id="82799-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-122">delta</span><span class="sxs-lookup"><span data-stu-id="82799-122">delta</span></span>  
    <span data-ttu-id="82799-123">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="82799-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="82799-124">包含加數的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82799-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-125">deltaSize</span><span class="sxs-lookup"><span data-stu-id="82799-125">deltaSize</span></span>  
    <span data-ttu-id="82799-126">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82799-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="82799-127">加數的大小。</span><span class="sxs-lookup"><span data-stu-id="82799-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-128">previousValue</span><span class="sxs-lookup"><span data-stu-id="82799-128">previousValue</span></span>  
    <span data-ttu-id="82799-129">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="82799-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="82799-130">將接收資料行目前值的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82799-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="82799-131">這個緩衝區可以是 null。</span><span class="sxs-lookup"><span data-stu-id="82799-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-132">previousValueLength</span><span class="sxs-lookup"><span data-stu-id="82799-132">previousValueLength</span></span>  
    <span data-ttu-id="82799-133">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82799-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="82799-134">PreviousValue 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="82799-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-135">actualPreviousValueLength</span><span class="sxs-lookup"><span data-stu-id="82799-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="82799-136">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82799-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="82799-137">傳回 previousValue 的實際大小。</span><span class="sxs-lookup"><span data-stu-id="82799-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="82799-138">grbit</span><span class="sxs-lookup"><span data-stu-id="82799-138">grbit</span></span>  
    <span data-ttu-id="82799-139">型別： [EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="82799-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="82799-140">託管更新選項。</span><span class="sxs-lookup"><span data-stu-id="82799-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="82799-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82799-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82799-142">參考</span><span class="sxs-lookup"><span data-stu-id="82799-142">Reference</span></span>

[<span data-ttu-id="82799-143">Api 類別</span><span class="sxs-lookup"><span data-stu-id="82799-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="82799-144">Api 成員</span><span class="sxs-lookup"><span data-stu-id="82799-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="82799-145">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="82799-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
