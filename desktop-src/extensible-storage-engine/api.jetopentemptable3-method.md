---
description: 深入瞭解： JetOpenTempTable3 方法
title: Api.JetOpenTempTable3 方法
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978160"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="c886c-103">Api.JetOpenTempTable3 方法</span><span class="sxs-lookup"><span data-stu-id="c886c-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="c886c-104">使用單一索引建立臨時表。</span><span class="sxs-lookup"><span data-stu-id="c886c-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="c886c-105">臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。</span><span class="sxs-lookup"><span data-stu-id="c886c-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="c886c-106">不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。</span><span class="sxs-lookup"><span data-stu-id="c886c-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="c886c-107">它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。</span><span class="sxs-lookup"><span data-stu-id="c886c-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="c886c-108">另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、Int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、 [JetOpenTemporaryTable (JET_SESID JET_OPENTEMPORARYTABLE) ](./vistaapi.jetopentemporarytable-method.md)。</span><span class="sxs-lookup"><span data-stu-id="c886c-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="c886c-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c886c-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c886c-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c886c-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c886c-111">語法</span><span class="sxs-lookup"><span data-stu-id="c886c-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="c886c-112">參數</span><span class="sxs-lookup"><span data-stu-id="c886c-112">Parameters</span></span>

  - <span data-ttu-id="c886c-113">sesid</span><span class="sxs-lookup"><span data-stu-id="c886c-113">sesid</span></span>  
    <span data-ttu-id="c886c-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c886c-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c886c-115">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c886c-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-116">資料行</span><span class="sxs-lookup"><span data-stu-id="c886c-116">columns</span></span>  
    <span data-ttu-id="c886c-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="c886c-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="c886c-118">在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="c886c-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="c886c-119">numColumns</span></span>  
    <span data-ttu-id="c886c-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c886c-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c886c-121">資料行定義的數目。</span><span class="sxs-lookup"><span data-stu-id="c886c-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="c886c-122">unicodeindex</span></span>  
    <span data-ttu-id="c886c-123">類型： [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="c886c-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="c886c-124">地區設定識別碼和正規化旗標，將用來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="c886c-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="c886c-125">如果不存在，則會使用預設選項。</span><span class="sxs-lookup"><span data-stu-id="c886c-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-126">grbit</span><span class="sxs-lookup"><span data-stu-id="c886c-126">grbit</span></span>  
    <span data-ttu-id="c886c-127">型別： [TempTableGrbit](./temptablegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c886c-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c886c-128">資料表建立選項。</span><span class="sxs-lookup"><span data-stu-id="c886c-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-129">tableid</span><span class="sxs-lookup"><span data-stu-id="c886c-129">tableid</span></span>  
    <span data-ttu-id="c886c-130">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c886c-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c886c-131">傳回臨時表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="c886c-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="c886c-132">使用 [JetCloseTable (JET_SESID 關閉此 tableid，JET_TABLEID) ](./api.jetclosetable-method.md) 會釋出與臨時表相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="c886c-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="c886c-133">columnids</span><span class="sxs-lookup"><span data-stu-id="c886c-133">columnids</span></span>  
    <span data-ttu-id="c886c-134">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="c886c-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="c886c-135">輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。</span><span class="sxs-lookup"><span data-stu-id="c886c-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="c886c-136">此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。</span><span class="sxs-lookup"><span data-stu-id="c886c-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="c886c-137">因此，這個緩衝區的大小必須對應到輸入陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="c886c-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="c886c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c886c-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c886c-139">參考</span><span class="sxs-lookup"><span data-stu-id="c886c-139">Reference</span></span>

[<span data-ttu-id="c886c-140">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c886c-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c886c-141">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c886c-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c886c-142">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c886c-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
