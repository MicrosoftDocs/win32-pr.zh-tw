---
description: '深入瞭解： RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983900"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="4d486-103">RetrieveColumnSize 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="4d486-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="4d486-104">從目前的記錄抓取單一資料行值的大小。</span><span class="sxs-lookup"><span data-stu-id="4d486-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="4d486-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="4d486-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="4d486-106">或者，此函式可以從資料指標複製緩衝區中所建立的記錄取得資料行。</span><span class="sxs-lookup"><span data-stu-id="4d486-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="4d486-107">此函數也可以從參考目前記錄的索引項目抓取資料行資料。</span><span class="sxs-lookup"><span data-stu-id="4d486-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="4d486-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d486-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d486-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4d486-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d486-110">語法</span><span class="sxs-lookup"><span data-stu-id="4d486-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="4d486-111">參數</span><span class="sxs-lookup"><span data-stu-id="4d486-111">Parameters</span></span>

  - <span data-ttu-id="4d486-112">sesid</span><span class="sxs-lookup"><span data-stu-id="4d486-112">sesid</span></span>  
    <span data-ttu-id="4d486-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d486-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4d486-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4d486-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d486-115">tableid</span><span class="sxs-lookup"><span data-stu-id="4d486-115">tableid</span></span>  
    <span data-ttu-id="4d486-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d486-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4d486-117">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="4d486-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d486-118">columnid</span><span class="sxs-lookup"><span data-stu-id="4d486-118">columnid</span></span>  
    <span data-ttu-id="4d486-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4d486-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4d486-120">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="4d486-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4d486-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d486-121">Return value</span></span>

<span data-ttu-id="4d486-122">類型： [可為 null](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="4d486-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="4d486-123">資料行的大小。</span><span class="sxs-lookup"><span data-stu-id="4d486-123">The size of the column.</span></span> <span data-ttu-id="4d486-124">如果資料行是 null，則為0。</span><span class="sxs-lookup"><span data-stu-id="4d486-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d486-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d486-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d486-126">參考</span><span class="sxs-lookup"><span data-stu-id="4d486-126">Reference</span></span>

[<span data-ttu-id="4d486-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4d486-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4d486-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4d486-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4d486-129">RetrieveColumnSize 多載</span><span class="sxs-lookup"><span data-stu-id="4d486-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="4d486-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4d486-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
