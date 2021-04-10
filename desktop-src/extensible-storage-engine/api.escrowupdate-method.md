---
description: 深入瞭解： EscrowUpdate 方法
title: EscrowUpdate 方法
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689431"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="54824-103">EscrowUpdate 方法</span><span class="sxs-lookup"><span data-stu-id="54824-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="54824-104">在一個資料行上執行不可部分完成的加法。</span><span class="sxs-lookup"><span data-stu-id="54824-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="54824-105">資料行的類型必須為 [Long](./jet-coltyp-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="54824-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="54824-106">此函數可讓多個會話同時更新相同的記錄，而不會發生衝突。</span><span class="sxs-lookup"><span data-stu-id="54824-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="54824-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54824-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54824-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="54824-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54824-109">語法</span><span class="sxs-lookup"><span data-stu-id="54824-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="54824-110">參數</span><span class="sxs-lookup"><span data-stu-id="54824-110">Parameters</span></span>

  - <span data-ttu-id="54824-111">sesid</span><span class="sxs-lookup"><span data-stu-id="54824-111">sesid</span></span>  
    <span data-ttu-id="54824-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54824-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="54824-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="54824-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="54824-114">tableid</span><span class="sxs-lookup"><span data-stu-id="54824-114">tableid</span></span>  
    <span data-ttu-id="54824-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54824-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="54824-116">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="54824-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="54824-117">columnid</span><span class="sxs-lookup"><span data-stu-id="54824-117">columnid</span></span>  
    <span data-ttu-id="54824-118">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="54824-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="54824-119">要更新的資料行。</span><span class="sxs-lookup"><span data-stu-id="54824-119">The column to update.</span></span> <span data-ttu-id="54824-120">這必須是可供使用的可更新資料行。</span><span class="sxs-lookup"><span data-stu-id="54824-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="54824-121">delta</span><span class="sxs-lookup"><span data-stu-id="54824-121">delta</span></span>  
    <span data-ttu-id="54824-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="54824-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="54824-123">要套用至資料行的差異。</span><span class="sxs-lookup"><span data-stu-id="54824-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="54824-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="54824-124">Return value</span></span>

<span data-ttu-id="54824-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="54824-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="54824-126">在資料庫中儲存之資料行的目前值 (版本設定會被忽略) 。</span><span class="sxs-lookup"><span data-stu-id="54824-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="54824-127">備註</span><span class="sxs-lookup"><span data-stu-id="54824-127">Remarks</span></span>

<span data-ttu-id="54824-128">這個方法會包裝[JetEscrowUpdate (JET_SESID、JET_TABLEID、JET_COLUMNID、 \[ \] 、int32、 \[ \] 、int32、int32、EscrowUpdateGrbit) ](./api.jetescrowupdate-method.md)。</span><span class="sxs-lookup"><span data-stu-id="54824-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="54824-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54824-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54824-130">參考</span><span class="sxs-lookup"><span data-stu-id="54824-130">Reference</span></span>

[<span data-ttu-id="54824-131">Api 類別</span><span class="sxs-lookup"><span data-stu-id="54824-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="54824-132">Api 成員</span><span class="sxs-lookup"><span data-stu-id="54824-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="54824-133">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="54824-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
