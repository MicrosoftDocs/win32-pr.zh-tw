---
description: 深入瞭解： JetCreateTable 方法
title: JetCreateTable 方法
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468856"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="a9607-103">JetCreateTable 方法</span><span class="sxs-lookup"><span data-stu-id="a9607-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="a9607-104">建立空的資料表。</span><span class="sxs-lookup"><span data-stu-id="a9607-104">Create an empty table.</span></span> <span data-ttu-id="a9607-105">新建立的資料表會以獨佔方式開啟。</span><span class="sxs-lookup"><span data-stu-id="a9607-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="a9607-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a9607-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a9607-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a9607-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a9607-108">語法</span><span class="sxs-lookup"><span data-stu-id="a9607-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a9607-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9607-109">Parameters</span></span>

  - <span data-ttu-id="a9607-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a9607-110">sesid</span></span>  
    <span data-ttu-id="a9607-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9607-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a9607-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a9607-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9607-113">dbid</span><span class="sxs-lookup"><span data-stu-id="a9607-113">dbid</span></span>  
    <span data-ttu-id="a9607-114">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9607-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a9607-115">要在其中建立資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a9607-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9607-116">資料表</span><span class="sxs-lookup"><span data-stu-id="a9607-116">table</span></span>  
    <span data-ttu-id="a9607-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a9607-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a9607-118">要建立之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9607-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9607-119">頁面</span><span class="sxs-lookup"><span data-stu-id="a9607-119">pages</span></span>  
    <span data-ttu-id="a9607-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a9607-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a9607-121">資料表中的初始頁面數目。</span><span class="sxs-lookup"><span data-stu-id="a9607-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9607-122">密度 (density)</span><span class="sxs-lookup"><span data-stu-id="a9607-122">density</span></span>  
    <span data-ttu-id="a9607-123">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a9607-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a9607-124">資料表的預設密度。</span><span class="sxs-lookup"><span data-stu-id="a9607-124">The default density of the table.</span></span> <span data-ttu-id="a9607-125">這是在執行連續插入時使用。</span><span class="sxs-lookup"><span data-stu-id="a9607-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="a9607-126">tableid</span><span class="sxs-lookup"><span data-stu-id="a9607-126">tableid</span></span>  
    <span data-ttu-id="a9607-127">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a9607-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a9607-128">傳回新資料表的 tableid。</span><span class="sxs-lookup"><span data-stu-id="a9607-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="a9607-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9607-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a9607-130">參考</span><span class="sxs-lookup"><span data-stu-id="a9607-130">Reference</span></span>

[<span data-ttu-id="a9607-131">Api 類別</span><span class="sxs-lookup"><span data-stu-id="a9607-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a9607-132">Api 成員</span><span class="sxs-lookup"><span data-stu-id="a9607-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a9607-133">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a9607-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
