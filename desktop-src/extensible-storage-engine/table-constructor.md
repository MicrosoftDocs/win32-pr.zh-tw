---
description: 深入瞭解：資料表函數
title: 資料表建構函式
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972073"
---
# <a name="table-constructor"></a><span data-ttu-id="f0bef-103">資料表建構函式</span><span class="sxs-lookup"><span data-stu-id="f0bef-103">Table constructor</span></span>

<span data-ttu-id="f0bef-104">初始化 Table 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="f0bef-104">Initializes a new instance of the Table class.</span></span> <span data-ttu-id="f0bef-105">資料表會從指定的資料庫開啟。</span><span class="sxs-lookup"><span data-stu-id="f0bef-105">The table is opened from the given database.</span></span>

<span data-ttu-id="f0bef-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0bef-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0bef-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f0bef-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0bef-108">語法</span><span class="sxs-lookup"><span data-stu-id="f0bef-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f0bef-109">參數</span><span class="sxs-lookup"><span data-stu-id="f0bef-109">Parameters</span></span>

  - <span data-ttu-id="f0bef-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f0bef-110">sesid</span></span>  
    <span data-ttu-id="f0bef-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f0bef-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f0bef-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f0bef-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f0bef-113">dbid</span><span class="sxs-lookup"><span data-stu-id="f0bef-113">dbid</span></span>  
    <span data-ttu-id="f0bef-114">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f0bef-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="f0bef-115">要在其中開啟資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="f0bef-115">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="f0bef-116">NAME</span><span class="sxs-lookup"><span data-stu-id="f0bef-116">name</span></span>  
    <span data-ttu-id="f0bef-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f0bef-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f0bef-118">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0bef-118">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f0bef-119">grbit</span><span class="sxs-lookup"><span data-stu-id="f0bef-119">grbit</span></span>  
    <span data-ttu-id="f0bef-120">型別： [OpenTableGrbit](./opentablegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="f0bef-120">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f0bef-121">JetOpenTable 選項。</span><span class="sxs-lookup"><span data-stu-id="f0bef-121">JetOpenTable options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0bef-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0bef-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0bef-123">參考</span><span class="sxs-lookup"><span data-stu-id="f0bef-123">Reference</span></span>

[<span data-ttu-id="f0bef-124">Table 類別</span><span class="sxs-lookup"><span data-stu-id="f0bef-124">Table class</span></span>](./table-class.md)

[<span data-ttu-id="f0bef-125">資料表成員</span><span class="sxs-lookup"><span data-stu-id="f0bef-125">Table members</span></span>](./table-members.md)

[<span data-ttu-id="f0bef-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f0bef-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
