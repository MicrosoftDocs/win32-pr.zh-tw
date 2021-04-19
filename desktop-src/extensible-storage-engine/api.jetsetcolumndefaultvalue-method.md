---
description: 深入瞭解： JetSetColumnDefaultValue 方法
title: JetSetColumnDefaultValue 方法
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992098"
---
# <a name="apijetsetcolumndefaultvalue-method"></a><span data-ttu-id="dbe8c-103">JetSetColumnDefaultValue 方法</span><span class="sxs-lookup"><span data-stu-id="dbe8c-103">Api.JetSetColumnDefaultValue method</span></span>

<span data-ttu-id="dbe8c-104">變更現有資料行的預設值。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-104">Changes the default value of an existing column.</span></span>

<span data-ttu-id="dbe8c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dbe8c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe8c-107">語法</span><span class="sxs-lookup"><span data-stu-id="dbe8c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="dbe8c-108">參數</span><span class="sxs-lookup"><span data-stu-id="dbe8c-108">Parameters</span></span>

  - <span data-ttu-id="dbe8c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="dbe8c-109">sesid</span></span>  
    <span data-ttu-id="dbe8c-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="dbe8c-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-112">dbid</span><span class="sxs-lookup"><span data-stu-id="dbe8c-112">dbid</span></span>  
    <span data-ttu-id="dbe8c-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="dbe8c-114">包含資料行的資料庫。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-114">The database containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-115">tableName</span><span class="sxs-lookup"><span data-stu-id="dbe8c-115">tableName</span></span>  
    <span data-ttu-id="dbe8c-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dbe8c-117">包含資料行的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-118">columnName</span><span class="sxs-lookup"><span data-stu-id="dbe8c-118">columnName</span></span>  
    <span data-ttu-id="dbe8c-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="dbe8c-120">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-121">data</span><span class="sxs-lookup"><span data-stu-id="dbe8c-121">data</span></span>  
    <span data-ttu-id="dbe8c-122">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="dbe8c-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="dbe8c-123">新的預設值。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-123">The new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-124">dataSize</span><span class="sxs-lookup"><span data-stu-id="dbe8c-124">dataSize</span></span>  
    <span data-ttu-id="dbe8c-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="dbe8c-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="dbe8c-126">新預設值的大小。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-126">Size of the new default value.</span></span>

<!-- end list -->

  - <span data-ttu-id="dbe8c-127">grbit</span><span class="sxs-lookup"><span data-stu-id="dbe8c-127">grbit</span></span>  
    <span data-ttu-id="dbe8c-128">型別： [SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-128">Type: [Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="dbe8c-129">資料行預設值選項。</span><span class="sxs-lookup"><span data-stu-id="dbe8c-129">Column default value options.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe8c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbe8c-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dbe8c-131">參考</span><span class="sxs-lookup"><span data-stu-id="dbe8c-131">Reference</span></span>

[<span data-ttu-id="dbe8c-132">Api 類別</span><span class="sxs-lookup"><span data-stu-id="dbe8c-132">Api class</span></span>](./api-class.md)

[<span data-ttu-id="dbe8c-133">Api 成員</span><span class="sxs-lookup"><span data-stu-id="dbe8c-133">Api members</span></span>](./api-members.md)

[<span data-ttu-id="dbe8c-134">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="dbe8c-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
