---
description: '深入瞭解： RetrieveColumnAsUInt16 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) '
title: 'RetrieveColumnAsUInt16 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) '
TOCTitle: RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint16(v=EXCHG.10)
ms:contentKeyID: 55100902
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ca82b1c2f5a9a1be7fa0ddbd5082e55820263a10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510842"
---
# <a name="apiretrievecolumnasuint16-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="672e9-103">RetrieveColumnAsUInt16 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、RetrieveColumnGrbit) </span><span class="sxs-lookup"><span data-stu-id="672e9-103">Api.RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="672e9-104">從目前的記錄抓取 uint16 資料行值。</span><span class="sxs-lookup"><span data-stu-id="672e9-104">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="672e9-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="672e9-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="672e9-106">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="672e9-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="672e9-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="672e9-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="672e9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="672e9-109">語法</span><span class="sxs-lookup"><span data-stu-id="672e9-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UShort)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UShort)

returnValue = Api.RetrieveColumnAsUInt16(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ushort> RetrieveColumnAsUInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="672e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="672e9-110">Parameters</span></span>

  - <span data-ttu-id="672e9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="672e9-111">sesid</span></span>  
    <span data-ttu-id="672e9-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="672e9-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="672e9-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="672e9-114">tableid</span><span class="sxs-lookup"><span data-stu-id="672e9-114">tableid</span></span>  
    <span data-ttu-id="672e9-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="672e9-116">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="672e9-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="672e9-117">columnid</span><span class="sxs-lookup"><span data-stu-id="672e9-117">columnid</span></span>  
    <span data-ttu-id="672e9-118">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="672e9-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="672e9-119">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="672e9-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="672e9-120">grbit</span><span class="sxs-lookup"><span data-stu-id="672e9-120">grbit</span></span>  
    <span data-ttu-id="672e9-121">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="672e9-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="672e9-122">抓取選項。</span><span class="sxs-lookup"><span data-stu-id="672e9-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="672e9-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="672e9-123">Return value</span></span>

<span data-ttu-id="672e9-124">類型： [可為 null](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span><span class="sxs-lookup"><span data-stu-id="672e9-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span></span>  
<span data-ttu-id="672e9-125">從資料行取出為 UInt16 的資料。</span><span class="sxs-lookup"><span data-stu-id="672e9-125">The data retrieved from the column as an UInt16.</span></span> <span data-ttu-id="672e9-126">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="672e9-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="672e9-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="672e9-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="672e9-128">參考</span><span class="sxs-lookup"><span data-stu-id="672e9-128">Reference</span></span>

[<span data-ttu-id="672e9-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="672e9-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="672e9-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="672e9-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="672e9-131">RetrieveColumnAsUInt16 多載</span><span class="sxs-lookup"><span data-stu-id="672e9-131">RetrieveColumnAsUInt16 overload</span></span>](./api.retrievecolumnasuint16-method.md)

[<span data-ttu-id="672e9-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="672e9-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
