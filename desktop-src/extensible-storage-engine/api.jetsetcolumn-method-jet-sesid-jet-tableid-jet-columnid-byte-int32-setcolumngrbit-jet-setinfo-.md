---
description: '深入瞭解： JetSetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、SetColumnGrbit、JET_SETINFO) '
title: 'JetSetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、SetColumnGrbit、JET_SETINFO) '
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975943"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="845f6-103">JetSetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、Byte、Int32、SetColumnGrbit、JET_SETINFO) </span><span class="sxs-lookup"><span data-stu-id="845f6-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="845f6-104">JetSetColumn 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="845f6-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="845f6-105">它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新 [LongText](./jet-coltyp-enumeration.md) 或 [LongBinary](./jet-coltyp-enumeration.md)) 類型資料行的完整或部分 long (值。</span><span class="sxs-lookup"><span data-stu-id="845f6-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="845f6-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="845f6-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="845f6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="845f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="845f6-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="845f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="845f6-109">Parameters</span></span>

  - <span data-ttu-id="845f6-110">sesid</span><span class="sxs-lookup"><span data-stu-id="845f6-110">sesid</span></span>  
    <span data-ttu-id="845f6-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="845f6-112">正在執行更新的會話。</span><span class="sxs-lookup"><span data-stu-id="845f6-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-113">tableid</span><span class="sxs-lookup"><span data-stu-id="845f6-113">tableid</span></span>  
    <span data-ttu-id="845f6-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="845f6-115">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="845f6-115">The cursor to update.</span></span> <span data-ttu-id="845f6-116">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="845f6-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-117">columnid</span><span class="sxs-lookup"><span data-stu-id="845f6-117">columnid</span></span>  
    <span data-ttu-id="845f6-118">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="845f6-119">要設定的 columnid。</span><span class="sxs-lookup"><span data-stu-id="845f6-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-120">data</span><span class="sxs-lookup"><span data-stu-id="845f6-120">data</span></span>  
    <span data-ttu-id="845f6-121">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="845f6-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="845f6-122">要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="845f6-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="845f6-123">dataSize</span></span>  
    <span data-ttu-id="845f6-124">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="845f6-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="845f6-125">要設定的資料大小。</span><span class="sxs-lookup"><span data-stu-id="845f6-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-126">grbit</span><span class="sxs-lookup"><span data-stu-id="845f6-126">grbit</span></span>  
    <span data-ttu-id="845f6-127">型別： [SetColumnGrbit](./setcolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="845f6-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="845f6-128">SetColumn 選項。</span><span class="sxs-lookup"><span data-stu-id="845f6-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="845f6-129">setinfo</span><span class="sxs-lookup"><span data-stu-id="845f6-129">setinfo</span></span>  
    <span data-ttu-id="845f6-130">類型： [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="845f6-131">用來指定 itag 或 long 值位移。</span><span class="sxs-lookup"><span data-stu-id="845f6-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="845f6-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="845f6-132">Return value</span></span>

<span data-ttu-id="845f6-133">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="845f6-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="845f6-134">警告碼。</span><span class="sxs-lookup"><span data-stu-id="845f6-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="845f6-135">備註</span><span class="sxs-lookup"><span data-stu-id="845f6-135">Remarks</span></span>

<span data-ttu-id="845f6-136">SetColumn 方法提供資料類型特定的覆寫，這可能更有效率。</span><span class="sxs-lookup"><span data-stu-id="845f6-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="845f6-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="845f6-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="845f6-138">參考</span><span class="sxs-lookup"><span data-stu-id="845f6-138">Reference</span></span>

[<span data-ttu-id="845f6-139">Api 類別</span><span class="sxs-lookup"><span data-stu-id="845f6-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="845f6-140">Api 成員</span><span class="sxs-lookup"><span data-stu-id="845f6-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="845f6-141">JetSetColumn 多載</span><span class="sxs-lookup"><span data-stu-id="845f6-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="845f6-142">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="845f6-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
