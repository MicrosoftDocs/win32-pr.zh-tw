---
description: 深入瞭解： JetCreateIndex 方法
title: JetCreateIndex 方法
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972826"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="35f91-103">JetCreateIndex 方法</span><span class="sxs-lookup"><span data-stu-id="35f91-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="35f91-104">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="35f91-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="35f91-105">索引可以用來快速找出特定資料。</span><span class="sxs-lookup"><span data-stu-id="35f91-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="35f91-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35f91-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35f91-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="35f91-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35f91-108">語法</span><span class="sxs-lookup"><span data-stu-id="35f91-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="35f91-109">參數</span><span class="sxs-lookup"><span data-stu-id="35f91-109">Parameters</span></span>

  - <span data-ttu-id="35f91-110">sesid</span><span class="sxs-lookup"><span data-stu-id="35f91-110">sesid</span></span>  
    <span data-ttu-id="35f91-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35f91-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="35f91-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="35f91-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-113">tableid</span><span class="sxs-lookup"><span data-stu-id="35f91-113">tableid</span></span>  
    <span data-ttu-id="35f91-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="35f91-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="35f91-115">要在其上建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="35f91-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-116">IndexName</span><span class="sxs-lookup"><span data-stu-id="35f91-116">indexName</span></span>  
    <span data-ttu-id="35f91-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="35f91-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="35f91-118">指標，指向以 null 終止的字串，指定要建立之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="35f91-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-119">grbit</span><span class="sxs-lookup"><span data-stu-id="35f91-119">grbit</span></span>  
    <span data-ttu-id="35f91-120">型別： [CreateIndexGrbit](./createindexgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="35f91-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="35f91-121">索引建立選項。</span><span class="sxs-lookup"><span data-stu-id="35f91-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-122">keyDescription</span><span class="sxs-lookup"><span data-stu-id="35f91-122">keyDescription</span></span>  
    <span data-ttu-id="35f91-123">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="35f91-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="35f91-124">Null 分隔標記的雙 null 結束字串指標。</span><span class="sxs-lookup"><span data-stu-id="35f91-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-125">keyDescriptionLength</span><span class="sxs-lookup"><span data-stu-id="35f91-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="35f91-126">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="35f91-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="35f91-127">SzKey 的長度（以字元為單位），包括兩個終止的 null。</span><span class="sxs-lookup"><span data-stu-id="35f91-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="35f91-128">密度 (density)</span><span class="sxs-lookup"><span data-stu-id="35f91-128">density</span></span>  
    <span data-ttu-id="35f91-129">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="35f91-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="35f91-130">初始 B + 樹狀結構密度。</span><span class="sxs-lookup"><span data-stu-id="35f91-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="35f91-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f91-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35f91-132">參考</span><span class="sxs-lookup"><span data-stu-id="35f91-132">Reference</span></span>

[<span data-ttu-id="35f91-133">Api 類別</span><span class="sxs-lookup"><span data-stu-id="35f91-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="35f91-134">Api 成員</span><span class="sxs-lookup"><span data-stu-id="35f91-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="35f91-135">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="35f91-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
