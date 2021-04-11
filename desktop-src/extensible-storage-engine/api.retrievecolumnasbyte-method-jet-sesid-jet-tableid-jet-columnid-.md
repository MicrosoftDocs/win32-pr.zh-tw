---
description: '深入瞭解： RetrieveColumnAsByte 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'RetrieveColumnAsByte 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100838
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3bc5db8aa14f3cabf05f15f8e1ecb41256496b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945283"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="3be70-103">RetrieveColumnAsByte 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="3be70-103">Api.RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="3be70-104">從目前的記錄抓取位元組資料行值。</span><span class="sxs-lookup"><span data-stu-id="3be70-104">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="3be70-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="3be70-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="3be70-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3be70-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3be70-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3be70-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3be70-108">語法</span><span class="sxs-lookup"><span data-stu-id="3be70-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="3be70-109">參數</span><span class="sxs-lookup"><span data-stu-id="3be70-109">Parameters</span></span>

  - <span data-ttu-id="3be70-110">sesid</span><span class="sxs-lookup"><span data-stu-id="3be70-110">sesid</span></span>  
    <span data-ttu-id="3be70-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3be70-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3be70-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="3be70-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3be70-113">tableid</span><span class="sxs-lookup"><span data-stu-id="3be70-113">tableid</span></span>  
    <span data-ttu-id="3be70-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3be70-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3be70-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="3be70-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3be70-116">columnid</span><span class="sxs-lookup"><span data-stu-id="3be70-116">columnid</span></span>  
    <span data-ttu-id="3be70-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3be70-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="3be70-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="3be70-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3be70-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="3be70-119">Return value</span></span>

<span data-ttu-id="3be70-120">類型： [可為 null](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span><span class="sxs-lookup"><span data-stu-id="3be70-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span></span>  
<span data-ttu-id="3be70-121">從資料行中取出的資料（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3be70-121">The data retrieved from the column as a byte.</span></span> <span data-ttu-id="3be70-122">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="3be70-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3be70-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3be70-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3be70-124">參考</span><span class="sxs-lookup"><span data-stu-id="3be70-124">Reference</span></span>

[<span data-ttu-id="3be70-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="3be70-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3be70-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="3be70-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3be70-127">RetrieveColumnAsByte 多載</span><span class="sxs-lookup"><span data-stu-id="3be70-127">RetrieveColumnAsByte overload</span></span>](./api.retrievecolumnasbyte-method.md)

[<span data-ttu-id="3be70-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3be70-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
