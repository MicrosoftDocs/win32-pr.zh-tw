---
description: 深入瞭解： JetAddColumn 方法
title: JetAddColumn 方法
TOCTitle: 'JetAddColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAddColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.JET_COLUMNID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetaddcolumn(v=EXCHG.10)
ms:contentKeyID: 55100651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAddColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a864bab9c3b888622640e6226c3e7ee542a096d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986319"
---
# <a name="apijetaddcolumn-method"></a><span data-ttu-id="767d6-103">JetAddColumn 方法</span><span class="sxs-lookup"><span data-stu-id="767d6-103">Api.JetAddColumn method</span></span>

<span data-ttu-id="767d6-104">將新的資料行加入至現有的資料表。</span><span class="sxs-lookup"><span data-stu-id="767d6-104">Add a new column to an existing table.</span></span>

<span data-ttu-id="767d6-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="767d6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="767d6-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="767d6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="767d6-107">語法</span><span class="sxs-lookup"><span data-stu-id="767d6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetAddColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    columndef As JET_COLUMNDEF, _
    defaultValue As Byte(), _
    defaultValueSize As Integer, _
    <OutAttribute> ByRef columnid As JET_COLUMNID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim columndef As JET_COLUMNDEF
Dim defaultValue As Byte()
Dim defaultValueSize As Integer
Dim columnid As JET_COLUMNIDApi.JetAddColumn(sesid, tableid, _
    column, columndef, defaultValue, _
    defaultValueSize, columnid)
```

``` csharp
public static void JetAddColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    JET_COLUMNDEF columndef,
    byte[] defaultValue,
    int defaultValueSize,
    out JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="767d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="767d6-108">Parameters</span></span>

  - <span data-ttu-id="767d6-109">sesid</span><span class="sxs-lookup"><span data-stu-id="767d6-109">sesid</span></span>  
    <span data-ttu-id="767d6-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="767d6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="767d6-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="767d6-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-112">tableid</span><span class="sxs-lookup"><span data-stu-id="767d6-112">tableid</span></span>  
    <span data-ttu-id="767d6-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="767d6-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="767d6-114">要加入資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="767d6-114">The table to add the column to.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-115">直條圖</span><span class="sxs-lookup"><span data-stu-id="767d6-115">column</span></span>  
    <span data-ttu-id="767d6-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="767d6-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="767d6-117">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="767d6-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-118">columndef</span><span class="sxs-lookup"><span data-stu-id="767d6-118">columndef</span></span>  
    <span data-ttu-id="767d6-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="767d6-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="767d6-120">資料行的定義。</span><span class="sxs-lookup"><span data-stu-id="767d6-120">The definition of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-121">defaultValue</span><span class="sxs-lookup"><span data-stu-id="767d6-121">defaultValue</span></span>  
    <span data-ttu-id="767d6-122">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="767d6-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="767d6-123">資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="767d6-123">The default value of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-124">defaultValueSize</span><span class="sxs-lookup"><span data-stu-id="767d6-124">defaultValueSize</span></span>  
    <span data-ttu-id="767d6-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="767d6-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="767d6-126">預設值的大小。</span><span class="sxs-lookup"><span data-stu-id="767d6-126">The size of the default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="767d6-127">columnid</span><span class="sxs-lookup"><span data-stu-id="767d6-127">columnid</span></span>  
    <span data-ttu-id="767d6-128">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="767d6-128">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="767d6-129">傳回新資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="767d6-129">Returns the columnid of the new column.</span></span>

## <a name="see-also"></a><span data-ttu-id="767d6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="767d6-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="767d6-131">參考</span><span class="sxs-lookup"><span data-stu-id="767d6-131">Reference</span></span>

[<span data-ttu-id="767d6-132">Api 類別</span><span class="sxs-lookup"><span data-stu-id="767d6-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="767d6-133">Api 成員</span><span class="sxs-lookup"><span data-stu-id="767d6-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="767d6-134">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="767d6-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
