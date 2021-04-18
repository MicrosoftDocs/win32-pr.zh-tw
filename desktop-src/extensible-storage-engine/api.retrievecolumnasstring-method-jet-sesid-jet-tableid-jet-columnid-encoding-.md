---
description: '深入瞭解： RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼) '
title: 'RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼) '
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100899
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d7ec3bac73f5b82f82d2762a34084de25b63f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971339"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding"></a><span data-ttu-id="1d04f-103">RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、編碼) </span><span class="sxs-lookup"><span data-stu-id="1d04f-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding)</span></span>

<span data-ttu-id="1d04f-104">從目前的記錄抓取字串資料行值。</span><span class="sxs-lookup"><span data-stu-id="1d04f-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="1d04f-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="1d04f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="1d04f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d04f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1d04f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1d04f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d04f-108">語法</span><span class="sxs-lookup"><span data-stu-id="1d04f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="1d04f-109">參數</span><span class="sxs-lookup"><span data-stu-id="1d04f-109">Parameters</span></span>

  - <span data-ttu-id="1d04f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="1d04f-110">sesid</span></span>  
    <span data-ttu-id="1d04f-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d04f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1d04f-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1d04f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d04f-113">tableid</span><span class="sxs-lookup"><span data-stu-id="1d04f-113">tableid</span></span>  
    <span data-ttu-id="1d04f-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d04f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1d04f-115">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1d04f-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d04f-116">columnid</span><span class="sxs-lookup"><span data-stu-id="1d04f-116">columnid</span></span>  
    <span data-ttu-id="1d04f-117">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d04f-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1d04f-118">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="1d04f-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d04f-119">編碼</span><span class="sxs-lookup"><span data-stu-id="1d04f-119">encoding</span></span>  
    <span data-ttu-id="1d04f-120">類型： [system.object。編碼](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="1d04f-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="1d04f-121">轉換資料時要使用的字串編碼。</span><span class="sxs-lookup"><span data-stu-id="1d04f-121">The string encoding to use when converting data.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1d04f-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d04f-122">Return value</span></span>

<span data-ttu-id="1d04f-123">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1d04f-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="1d04f-124">從資料行以字串形式取出的資料。</span><span class="sxs-lookup"><span data-stu-id="1d04f-124">The data retrieved from the column as a string.</span></span> <span data-ttu-id="1d04f-125">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="1d04f-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d04f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d04f-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d04f-127">參考</span><span class="sxs-lookup"><span data-stu-id="1d04f-127">Reference</span></span>

[<span data-ttu-id="1d04f-128">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1d04f-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1d04f-129">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1d04f-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1d04f-130">RetrieveColumnAsString 多載</span><span class="sxs-lookup"><span data-stu-id="1d04f-130">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="1d04f-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1d04f-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
