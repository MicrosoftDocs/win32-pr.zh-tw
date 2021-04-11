---
description: '深入瞭解： DeserializeObjectFromColumn 方法 (JET_SESID、JET_TABLEID JET_COLUMNID) '
title: 'DeserializeObjectFromColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) '
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100688
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9ec3ca1f505c9d768e54b284caf05b335934451
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847655"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="1db3b-103">DeserializeObjectFromColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID) </span><span class="sxs-lookup"><span data-stu-id="1db3b-103">Api.DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="1db3b-104">從資料行還原序列化物件。</span><span class="sxs-lookup"><span data-stu-id="1db3b-104">Deserialize an object from a column.</span></span>

<span data-ttu-id="1db3b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1db3b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1db3b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1db3b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1db3b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1db3b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="1db3b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1db3b-108">Parameters</span></span>

  - <span data-ttu-id="1db3b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1db3b-109">sesid</span></span>  
    <span data-ttu-id="1db3b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1db3b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1db3b-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1db3b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1db3b-112">tableid</span><span class="sxs-lookup"><span data-stu-id="1db3b-112">tableid</span></span>  
    <span data-ttu-id="1db3b-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1db3b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1db3b-114">要從中讀取的資料表。</span><span class="sxs-lookup"><span data-stu-id="1db3b-114">The table to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1db3b-115">columnid</span><span class="sxs-lookup"><span data-stu-id="1db3b-115">columnid</span></span>  
    <span data-ttu-id="1db3b-116">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1db3b-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1db3b-117">要從中讀取的資料行。</span><span class="sxs-lookup"><span data-stu-id="1db3b-117">The column to read from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1db3b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1db3b-118">Return value</span></span>

<span data-ttu-id="1db3b-119">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="1db3b-119">Type: [System.Object](/dotnet/api/system.object)</span></span>  
<span data-ttu-id="1db3b-120">已還原序列化的物件。</span><span class="sxs-lookup"><span data-stu-id="1db3b-120">The deserialized object.</span></span> <span data-ttu-id="1db3b-121">如果資料行是 null，則為 null。</span><span class="sxs-lookup"><span data-stu-id="1db3b-121">Null if the column was null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1db3b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1db3b-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1db3b-123">參考</span><span class="sxs-lookup"><span data-stu-id="1db3b-123">Reference</span></span>

[<span data-ttu-id="1db3b-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1db3b-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1db3b-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1db3b-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1db3b-126">DeserializeObjectFromColumn 多載</span><span class="sxs-lookup"><span data-stu-id="1db3b-126">DeserializeObjectFromColumn overload</span></span>](./api.deserializeobjectfromcolumn-method.md)

[<span data-ttu-id="1db3b-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1db3b-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
