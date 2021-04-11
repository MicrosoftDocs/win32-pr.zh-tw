---
description: 深入瞭解： Windows8Api. JetCreateIndex4 方法
title: 'Windows8Api. JetCreateIndex4 方法 (Windows8 的) '
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114257"
---
# <a name="windows8apijetcreateindex4-method"></a><span data-ttu-id="69c05-103">Windows8Api. JetCreateIndex4 方法</span><span class="sxs-lookup"><span data-stu-id="69c05-103">Windows8Api.JetCreateIndex4 method</span></span>

<span data-ttu-id="69c05-104">對 ESE 資料庫中的資料建立索引。</span><span class="sxs-lookup"><span data-stu-id="69c05-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="69c05-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69c05-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="69c05-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="69c05-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69c05-107">語法</span><span class="sxs-lookup"><span data-stu-id="69c05-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="69c05-108">參數</span><span class="sxs-lookup"><span data-stu-id="69c05-108">Parameters</span></span>

  - <span data-ttu-id="69c05-109">sesid</span><span class="sxs-lookup"><span data-stu-id="69c05-109">sesid</span></span>  
    <span data-ttu-id="69c05-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69c05-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69c05-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="69c05-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="69c05-112">tableid</span><span class="sxs-lookup"><span data-stu-id="69c05-112">tableid</span></span>  
    <span data-ttu-id="69c05-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69c05-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="69c05-114">要在其上建立索引的資料表。</span><span class="sxs-lookup"><span data-stu-id="69c05-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="69c05-115">indexcreates</span><span class="sxs-lookup"><span data-stu-id="69c05-115">indexcreates</span></span>  
    <span data-ttu-id="69c05-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="69c05-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="69c05-117">物件的陣列，描述要建立的索引。</span><span class="sxs-lookup"><span data-stu-id="69c05-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="69c05-118">numIndexCreates</span><span class="sxs-lookup"><span data-stu-id="69c05-118">numIndexCreates</span></span>  
    <span data-ttu-id="69c05-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="69c05-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="69c05-120">索引描述物件的數目。</span><span class="sxs-lookup"><span data-stu-id="69c05-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="69c05-121">備註</span><span class="sxs-lookup"><span data-stu-id="69c05-121">Remarks</span></span>

<span data-ttu-id="69c05-122">建立多個索引時 (也就是 numIndexCreates 大於 1) 此方法必須在任何交易之外呼叫，且具有資料表的獨佔存取權。</span><span class="sxs-lookup"><span data-stu-id="69c05-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="69c05-123">JetCreateTable 所傳回的 JET_TABLEID 將擁有% 存取權，或者，您可以藉由將[DenyRead](./opentablegrbit-enumeration.md)傳遞至[JetOpenTable (JET_SESID、JET_DBID、字串、 \[ \] 、Int32、OpenTableGrbit、JET_TABLEID) ，](./api.jetopentable-method.md)來開啟該資料表以進行獨佔存取。</span><span class="sxs-lookup"><span data-stu-id="69c05-123">The JET_TABLEID returned by "Api.JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="69c05-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69c05-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69c05-125">參考</span><span class="sxs-lookup"><span data-stu-id="69c05-125">Reference</span></span>

[<span data-ttu-id="69c05-126">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="69c05-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="69c05-127">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="69c05-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="69c05-128">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="69c05-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
