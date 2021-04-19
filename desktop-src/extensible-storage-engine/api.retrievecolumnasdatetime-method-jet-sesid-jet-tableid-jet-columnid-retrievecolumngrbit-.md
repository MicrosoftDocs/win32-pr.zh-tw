---
description: '深入瞭解： RetrieveColumnAsDateTime 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) '
title: 'RetrieveColumnAsDateTime 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) '
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: befd4e7256c9d1ca52d6f0239f5e56c21842a85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977103"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="3521f-103">RetrieveColumnAsDateTime 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </span><span class="sxs-lookup"><span data-stu-id="3521f-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="3521f-104">從目前的記錄抓取 datetime 資料行值。</span><span class="sxs-lookup"><span data-stu-id="3521f-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="3521f-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="3521f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="3521f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3521f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3521f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3521f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3521f-108">語法</span><span class="sxs-lookup"><span data-stu-id="3521f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3521f-109">參數</span><span class="sxs-lookup"><span data-stu-id="3521f-109">Parameters</span></span>

  - <span data-ttu-id="3521f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3521f-110">sesid</span></span>  
    <span data-ttu-id="3521f-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3521f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3521f-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="3521f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3521f-113">tableid</span><span class="sxs-lookup"><span data-stu-id="3521f-113">tableid</span></span>  
    <span data-ttu-id="3521f-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3521f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3521f-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="3521f-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3521f-116">columnid</span><span class="sxs-lookup"><span data-stu-id="3521f-116">columnid</span></span>  
    <span data-ttu-id="3521f-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3521f-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3521f-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="3521f-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="3521f-119">grbit</span><span class="sxs-lookup"><span data-stu-id="3521f-119">grbit</span></span>  
    <span data-ttu-id="3521f-120">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="3521f-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3521f-121">抓取選項。</span><span class="sxs-lookup"><span data-stu-id="3521f-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3521f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="3521f-122">Return value</span></span>

<span data-ttu-id="3521f-123">類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="3521f-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="3521f-124">以日期時間從資料行中取出的資料。</span><span class="sxs-lookup"><span data-stu-id="3521f-124">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="3521f-125">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="3521f-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3521f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3521f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3521f-127">參考</span><span class="sxs-lookup"><span data-stu-id="3521f-127">Reference</span></span>

[<span data-ttu-id="3521f-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="3521f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3521f-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="3521f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3521f-130">RetrieveColumnAsDateTime 多載</span><span class="sxs-lookup"><span data-stu-id="3521f-130">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="3521f-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3521f-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
