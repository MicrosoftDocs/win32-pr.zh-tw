---
description: '深入瞭解： RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100860
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
ms.openlocfilehash: 64500e9827d55fab4771963b95dbfd0efffdc5c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988399"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="220ba-103">RetrieveColumnAsString 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="220ba-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="220ba-104">從目前的記錄抓取單一資料行值。</span><span class="sxs-lookup"><span data-stu-id="220ba-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="220ba-105">記錄是與索引項目相關聯的記錄，位於資料指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="220ba-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="220ba-106">使用 Unicode 編碼。</span><span class="sxs-lookup"><span data-stu-id="220ba-106">The Unicode encoding is used.</span></span>

<span data-ttu-id="220ba-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="220ba-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="220ba-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="220ba-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="220ba-109">語法</span><span class="sxs-lookup"><span data-stu-id="220ba-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="220ba-110">參數</span><span class="sxs-lookup"><span data-stu-id="220ba-110">Parameters</span></span>

  - <span data-ttu-id="220ba-111">sesid</span><span class="sxs-lookup"><span data-stu-id="220ba-111">sesid</span></span>  
    <span data-ttu-id="220ba-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="220ba-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="220ba-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="220ba-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="220ba-114">tableid</span><span class="sxs-lookup"><span data-stu-id="220ba-114">tableid</span></span>  
    <span data-ttu-id="220ba-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="220ba-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="220ba-116">從中取出資料行的資料指標。</span><span class="sxs-lookup"><span data-stu-id="220ba-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="220ba-117">columnid</span><span class="sxs-lookup"><span data-stu-id="220ba-117">columnid</span></span>  
    <span data-ttu-id="220ba-118">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="220ba-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="220ba-119">要取出的 columnid。</span><span class="sxs-lookup"><span data-stu-id="220ba-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="220ba-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="220ba-120">Return value</span></span>

<span data-ttu-id="220ba-121">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="220ba-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="220ba-122">從資料行以字串形式取出的資料。</span><span class="sxs-lookup"><span data-stu-id="220ba-122">The data retrieved from the column as a string.</span></span> <span data-ttu-id="220ba-123">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="220ba-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="220ba-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="220ba-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="220ba-125">參考</span><span class="sxs-lookup"><span data-stu-id="220ba-125">Reference</span></span>

[<span data-ttu-id="220ba-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="220ba-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="220ba-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="220ba-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="220ba-128">RetrieveColumnAsString 多載</span><span class="sxs-lookup"><span data-stu-id="220ba-128">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="220ba-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="220ba-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
