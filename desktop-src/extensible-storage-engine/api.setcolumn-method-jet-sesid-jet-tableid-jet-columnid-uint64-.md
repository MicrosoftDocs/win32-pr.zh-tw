---
description: '深入瞭解： SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt64) '
title: 'SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt64) '
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.UInt64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100931
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e43711f40c723e84476bd8d2aa79f3761f87b9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979019"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-uint64"></a><span data-ttu-id="6a0e1-103">SetColumn 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID、UInt64) </span><span class="sxs-lookup"><span data-stu-id="6a0e1-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</span></span>

<span data-ttu-id="6a0e1-104">修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="6a0e1-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="6a0e1-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a0e1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a0e1-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a0e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="6a0e1-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As ULong _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As ULongApi.SetColumn(sesid, tableid, columnid, _
    data)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    ulong data
)
```

#### <a name="parameters"></a><span data-ttu-id="6a0e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="6a0e1-109">Parameters</span></span>

  - <span data-ttu-id="6a0e1-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6a0e1-110">sesid</span></span>  
    <span data-ttu-id="6a0e1-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a0e1-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6a0e1-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a0e1-113">tableid</span><span class="sxs-lookup"><span data-stu-id="6a0e1-113">tableid</span></span>  
    <span data-ttu-id="6a0e1-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a0e1-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6a0e1-115">要更新的資料指標。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-115">The cursor to update.</span></span> <span data-ttu-id="6a0e1-116">應備妥更新。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a0e1-117">columnid</span><span class="sxs-lookup"><span data-stu-id="6a0e1-117">columnid</span></span>  
    <span data-ttu-id="6a0e1-118">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6a0e1-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6a0e1-119">要設定的 columnid。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a0e1-120">data</span><span class="sxs-lookup"><span data-stu-id="6a0e1-120">data</span></span>  
    <span data-ttu-id="6a0e1-121">類型： [system.object](/dotnet/api/system.uint64)</span><span class="sxs-lookup"><span data-stu-id="6a0e1-121">Type: [System.UInt64](/dotnet/api/system.uint64)</span></span>  
    
    <span data-ttu-id="6a0e1-122">要設定的資料。</span><span class="sxs-lookup"><span data-stu-id="6a0e1-122">The data to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a0e1-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a0e1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a0e1-124">參考</span><span class="sxs-lookup"><span data-stu-id="6a0e1-124">Reference</span></span>

[<span data-ttu-id="6a0e1-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6a0e1-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6a0e1-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6a0e1-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6a0e1-127">SetColumn 多載</span><span class="sxs-lookup"><span data-stu-id="6a0e1-127">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="6a0e1-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6a0e1-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
