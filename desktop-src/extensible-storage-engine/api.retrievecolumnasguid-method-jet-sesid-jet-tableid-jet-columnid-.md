---
description: '深入瞭解： RetrieveColumnAsGuid 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'RetrieveColumnAsGuid 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasguid(v=EXCHG.10)
ms:contentKeyID: 55100876
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a496d5f0ce45a1f2f8d43072ac5d311e7e7a9c29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983864"
---
# <a name="apiretrievecolumnasguid-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="d3947-103">RetrieveColumnAsGuid 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="d3947-103">Api.RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="d3947-104">從目前的記錄抓取 guid 資料行值。</span><span class="sxs-lookup"><span data-stu-id="d3947-104">Retrieves a guid column value from the current record.</span></span> <span data-ttu-id="d3947-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="d3947-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="d3947-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3947-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3947-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d3947-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3947-108">語法</span><span class="sxs-lookup"><span data-stu-id="d3947-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsGuid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Guid)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Guid)

returnValue = Api.RetrieveColumnAsGuid(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<Guid> RetrieveColumnAsGuid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="d3947-109">參數</span><span class="sxs-lookup"><span data-stu-id="d3947-109">Parameters</span></span>

  - <span data-ttu-id="d3947-110">sesid</span><span class="sxs-lookup"><span data-stu-id="d3947-110">sesid</span></span>  
    <span data-ttu-id="d3947-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3947-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d3947-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d3947-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3947-113">tableid</span><span class="sxs-lookup"><span data-stu-id="d3947-113">tableid</span></span>  
    <span data-ttu-id="d3947-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3947-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d3947-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="d3947-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3947-116">columnid</span><span class="sxs-lookup"><span data-stu-id="d3947-116">columnid</span></span>  
    <span data-ttu-id="d3947-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3947-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d3947-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="d3947-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d3947-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3947-119">Return value</span></span>

<span data-ttu-id="d3947-120">類型： [可為 null](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span><span class="sxs-lookup"><span data-stu-id="d3947-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span></span>  
<span data-ttu-id="d3947-121">從資料行取出為 guid 的資料。</span><span class="sxs-lookup"><span data-stu-id="d3947-121">The data retrieved from the column as a guid.</span></span> <span data-ttu-id="d3947-122">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="d3947-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3947-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3947-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3947-124">參考</span><span class="sxs-lookup"><span data-stu-id="d3947-124">Reference</span></span>

[<span data-ttu-id="d3947-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="d3947-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d3947-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="d3947-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d3947-127">RetrieveColumnAsGuid 多載</span><span class="sxs-lookup"><span data-stu-id="d3947-127">RetrieveColumnAsGuid overload</span></span>](./api.retrievecolumnasguid-method.md)

[<span data-ttu-id="d3947-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d3947-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
