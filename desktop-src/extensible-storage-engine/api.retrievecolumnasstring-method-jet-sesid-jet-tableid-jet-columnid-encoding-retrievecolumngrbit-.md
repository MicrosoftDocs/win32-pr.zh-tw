---
description: '深入瞭解： RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼、RetrieveColumnGrbit) '
title: 'RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼、RetrieveColumnGrbit) '
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989096"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="e4fd3-103">RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼、RetrieveColumnGrbit) </span><span class="sxs-lookup"><span data-stu-id="e4fd3-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="e4fd3-104">從目前的記錄抓取字串資料行值。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="e4fd3-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="e4fd3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4fd3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fd3-108">語法</span><span class="sxs-lookup"><span data-stu-id="e4fd3-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e4fd3-109">參數</span><span class="sxs-lookup"><span data-stu-id="e4fd3-109">Parameters</span></span>

  - <span data-ttu-id="e4fd3-110">sesid</span><span class="sxs-lookup"><span data-stu-id="e4fd3-110">sesid</span></span>  
    <span data-ttu-id="e4fd3-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e4fd3-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4fd3-113">tableid</span><span class="sxs-lookup"><span data-stu-id="e4fd3-113">tableid</span></span>  
    <span data-ttu-id="e4fd3-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e4fd3-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4fd3-116">columnid</span><span class="sxs-lookup"><span data-stu-id="e4fd3-116">columnid</span></span>  
    <span data-ttu-id="e4fd3-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="e4fd3-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4fd3-119">編碼</span><span class="sxs-lookup"><span data-stu-id="e4fd3-119">encoding</span></span>  
    <span data-ttu-id="e4fd3-120">類型： [system.object。編碼](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="e4fd3-121">轉換資料時要使用的字串編碼。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4fd3-122">grbit</span><span class="sxs-lookup"><span data-stu-id="e4fd3-122">grbit</span></span>  
    <span data-ttu-id="e4fd3-123">型別： [RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e4fd3-124">抓取選項。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e4fd3-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4fd3-125">Return value</span></span>

<span data-ttu-id="e4fd3-126">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e4fd3-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="e4fd3-127">從資料行以字串形式取出的資料。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="e4fd3-128">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="e4fd3-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e4fd3-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4fd3-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4fd3-130">參考</span><span class="sxs-lookup"><span data-stu-id="e4fd3-130">Reference</span></span>

[<span data-ttu-id="e4fd3-131">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e4fd3-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e4fd3-132">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e4fd3-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e4fd3-133">RetrieveColumnAsString 多載</span><span class="sxs-lookup"><span data-stu-id="e4fd3-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="e4fd3-134">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e4fd3-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
