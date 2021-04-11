---
description: 深入瞭解： JetCreateIndex2 方法
title: JetCreateIndex2 方法
TOCTitle: 'JetCreateIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex2(v=EXCHG.10)
ms:contentKeyID: 55100673
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fa690ed127c41b8a84f5d8aa012510f3a9c3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847855"
---
# <a name="apijetcreateindex2-method"></a><span data-ttu-id="63ce3-103">JetCreateIndex2 方法</span><span class="sxs-lookup"><span data-stu-id="63ce3-103">Api.JetCreateIndex2 method</span></span>

<span data-ttu-id="63ce3-104">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="63ce3-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="63ce3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="63ce3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="63ce3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="63ce3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="63ce3-107">語法</span><span class="sxs-lookup"><span data-stu-id="63ce3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerApi.JetCreateIndex2(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="63ce3-108">參數</span><span class="sxs-lookup"><span data-stu-id="63ce3-108">Parameters</span></span>

  - <span data-ttu-id="63ce3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="63ce3-109">sesid</span></span>  
    <span data-ttu-id="63ce3-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63ce3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="63ce3-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="63ce3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="63ce3-112">tableid</span><span class="sxs-lookup"><span data-stu-id="63ce3-112">tableid</span></span>  
    <span data-ttu-id="63ce3-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="63ce3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="63ce3-114">要在其上建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="63ce3-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="63ce3-115">indexcreates</span><span class="sxs-lookup"><span data-stu-id="63ce3-115">indexcreates</span></span>  
    <span data-ttu-id="63ce3-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="63ce3-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="63ce3-117">物件的陣列，描述要建立的索引。</span><span class="sxs-lookup"><span data-stu-id="63ce3-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="63ce3-118">numIndexCreates</span><span class="sxs-lookup"><span data-stu-id="63ce3-118">numIndexCreates</span></span>  
    <span data-ttu-id="63ce3-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="63ce3-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="63ce3-120">索引描述物件的數目。</span><span class="sxs-lookup"><span data-stu-id="63ce3-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="63ce3-121">備註</span><span class="sxs-lookup"><span data-stu-id="63ce3-121">Remarks</span></span>

<span data-ttu-id="63ce3-122">建立多個索引時 (也就是 numIndexCreates 大於 1) 此方法必須在任何交易之外呼叫，且具有資料表的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="63ce3-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="63ce3-123">"JetCreateTable" 所傳回的 JET_TABLEID 將擁有% 存取權，或是藉由將[DenyRead](./opentablegrbit-enumeration.md)傳遞至[JetOpenTable (JET_SESID、JET_DBID、字串、 \[ \] 、Int32、OpenTableGrbit、JET_TABLEID) ，](./api.jetopentable-method.md)來開啟資料表以進行獨佔存取。</span><span class="sxs-lookup"><span data-stu-id="63ce3-123">The JET_TABLEID returned by "JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="63ce3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63ce3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="63ce3-125">參考</span><span class="sxs-lookup"><span data-stu-id="63ce3-125">Reference</span></span>

[<span data-ttu-id="63ce3-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="63ce3-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="63ce3-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="63ce3-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="63ce3-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="63ce3-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
