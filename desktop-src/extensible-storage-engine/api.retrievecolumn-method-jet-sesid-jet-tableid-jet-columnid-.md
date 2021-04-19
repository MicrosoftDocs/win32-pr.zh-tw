---
description: '深入瞭解： RetrieveColumn 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'RetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100833
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c29a591064c573e168903aaf83dcdd15f5b9a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980079"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="1a426-103">RetrieveColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="1a426-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="1a426-104">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="1a426-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="1a426-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="1a426-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="1a426-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a426-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a426-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1a426-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a426-108">語法</span><span class="sxs-lookup"><span data-stu-id="1a426-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="1a426-109">參數</span><span class="sxs-lookup"><span data-stu-id="1a426-109">Parameters</span></span>

  - <span data-ttu-id="1a426-110">sesid</span><span class="sxs-lookup"><span data-stu-id="1a426-110">sesid</span></span>  
    <span data-ttu-id="1a426-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a426-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a426-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1a426-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a426-113">tableid</span><span class="sxs-lookup"><span data-stu-id="1a426-113">tableid</span></span>  
    <span data-ttu-id="1a426-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a426-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1a426-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1a426-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a426-116">columnid</span><span class="sxs-lookup"><span data-stu-id="1a426-116">columnid</span></span>  
    <span data-ttu-id="1a426-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a426-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1a426-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="1a426-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1a426-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a426-119">Return value</span></span>

<span data-ttu-id="1a426-120">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="1a426-120">Type: \[\]</span></span>  
<span data-ttu-id="1a426-121">從資料行中取出的資料。</span><span class="sxs-lookup"><span data-stu-id="1a426-121">The data retrieved from the column.</span></span> <span data-ttu-id="1a426-122">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="1a426-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a426-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a426-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a426-124">參考</span><span class="sxs-lookup"><span data-stu-id="1a426-124">Reference</span></span>

[<span data-ttu-id="1a426-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1a426-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a426-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1a426-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a426-127">RetrieveColumn 多載</span><span class="sxs-lookup"><span data-stu-id="1a426-127">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="1a426-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1a426-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
