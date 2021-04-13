---
description: 深入瞭解： TryOpenTable 方法
title: TryOpenTable 方法
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386135"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="b6fb0-103">TryOpenTable 方法</span><span class="sxs-lookup"><span data-stu-id="b6fb0-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="b6fb0-104">嘗試開啟資料表。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-104">Try to open a table.</span></span>

<span data-ttu-id="b6fb0-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6fb0-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6fb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="b6fb0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b6fb0-108">參數</span><span class="sxs-lookup"><span data-stu-id="b6fb0-108">Parameters</span></span>

  - <span data-ttu-id="b6fb0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b6fb0-109">sesid</span></span>  
    <span data-ttu-id="b6fb0-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b6fb0-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6fb0-112">dbid</span><span class="sxs-lookup"><span data-stu-id="b6fb0-112">dbid</span></span>  
    <span data-ttu-id="b6fb0-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="b6fb0-114">要在其中尋找資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6fb0-115">tablename</span><span class="sxs-lookup"><span data-stu-id="b6fb0-115">tablename</span></span>  
    <span data-ttu-id="b6fb0-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b6fb0-117">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6fb0-118">grbit</span><span class="sxs-lookup"><span data-stu-id="b6fb0-118">grbit</span></span>  
    <span data-ttu-id="b6fb0-119">型別： [OpenTableGrbit](./opentablegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b6fb0-120">資料表開啟的選項。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6fb0-121">tableid</span><span class="sxs-lookup"><span data-stu-id="b6fb0-121">tableid</span></span>  
    <span data-ttu-id="b6fb0-122">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b6fb0-123">傳回開啟的 tableid。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6fb0-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b6fb0-124">Return value</span></span>

<span data-ttu-id="b6fb0-125">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b6fb0-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b6fb0-126">如果資料表已開啟，則為 True，如果資料表不存在，則為 false。</span><span class="sxs-lookup"><span data-stu-id="b6fb0-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6fb0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6fb0-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6fb0-128">參考</span><span class="sxs-lookup"><span data-stu-id="b6fb0-128">Reference</span></span>

[<span data-ttu-id="b6fb0-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b6fb0-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6fb0-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b6fb0-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6fb0-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b6fb0-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
