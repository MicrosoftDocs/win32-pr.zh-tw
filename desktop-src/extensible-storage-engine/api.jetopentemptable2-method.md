---
description: 深入瞭解： JetOpenTempTable2 方法
title: JetOpenTempTable2 方法
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195024"
---
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="0d8f5-103">JetOpenTempTable2 方法</span><span class="sxs-lookup"><span data-stu-id="0d8f5-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="0d8f5-104">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="0d8f5-105">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="0d8f5-106">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="0d8f5-107">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="0d8f5-108">另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、Int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、 [JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable3-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="0d8f5-109">[JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) ](./vistaapi.jetopentemporarytable-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="0d8f5-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d8f5-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d8f5-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8f5-112">語法</span><span class="sxs-lookup"><span data-stu-id="0d8f5-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="0d8f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d8f5-113">Parameters</span></span>

  - <span data-ttu-id="0d8f5-114">sesid</span><span class="sxs-lookup"><span data-stu-id="0d8f5-114">sesid</span></span>  
    <span data-ttu-id="0d8f5-115">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d8f5-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0d8f5-116">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-117">資料行</span><span class="sxs-lookup"><span data-stu-id="0d8f5-117">columns</span></span>  
    <span data-ttu-id="0d8f5-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="0d8f5-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="0d8f5-119">在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="0d8f5-120">numColumns</span></span>  
    <span data-ttu-id="0d8f5-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0d8f5-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0d8f5-122">資料行定義的數目。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-123">lcid</span><span class="sxs-lookup"><span data-stu-id="0d8f5-123">lcid</span></span>  
    <span data-ttu-id="0d8f5-124">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0d8f5-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0d8f5-125">用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="0d8f5-126">只要電腦上已安裝適當的語言套件，即可使用任何地區設定。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-127">grbit</span><span class="sxs-lookup"><span data-stu-id="0d8f5-127">grbit</span></span>  
    <span data-ttu-id="0d8f5-128">型別： [TempTableGrbit](./temptablegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0d8f5-129">資料表建立選項。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-130">tableid</span><span class="sxs-lookup"><span data-stu-id="0d8f5-130">tableid</span></span>  
    <span data-ttu-id="0d8f5-131">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0d8f5-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0d8f5-132">傳回臨時表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="0d8f5-133">使用 [JetCloseTable (JET_SESID 關閉此 tableid，JET_TABLEID) ](./api.jetclosetable-method.md) 會釋出與臨時表相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d8f5-134">columnids</span><span class="sxs-lookup"><span data-stu-id="0d8f5-134">columnids</span></span>  
    <span data-ttu-id="0d8f5-135">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="0d8f5-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="0d8f5-136">輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="0d8f5-137">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="0d8f5-138">因此，這個緩衝區的大小必須對應到輸入陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="0d8f5-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d8f5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d8f5-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d8f5-140">參考</span><span class="sxs-lookup"><span data-stu-id="0d8f5-140">Reference</span></span>

[<span data-ttu-id="0d8f5-141">Api 類別</span><span class="sxs-lookup"><span data-stu-id="0d8f5-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0d8f5-142">Api 成員</span><span class="sxs-lookup"><span data-stu-id="0d8f5-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0d8f5-143">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0d8f5-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
