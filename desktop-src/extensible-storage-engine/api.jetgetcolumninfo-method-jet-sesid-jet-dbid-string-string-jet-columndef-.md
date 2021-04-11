---
description: '深入瞭解： JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNDEF) '
title: 'JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNDEF) '
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4af99e7cfdc9f2f1fe83095ad92797ce0b34bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112588"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a><span data-ttu-id="6cea3-103">JetGetColumnInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_COLUMNDEF) </span><span class="sxs-lookup"><span data-stu-id="6cea3-103">Api.JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="6cea3-104">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6cea3-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="6cea3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6cea3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6cea3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6cea3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6cea3-107">語法</span><span class="sxs-lookup"><span data-stu-id="6cea3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="6cea3-108">參數</span><span class="sxs-lookup"><span data-stu-id="6cea3-108">Parameters</span></span>

  - <span data-ttu-id="6cea3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6cea3-109">sesid</span></span>  
    <span data-ttu-id="6cea3-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6cea3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6cea3-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="6cea3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cea3-112">dbid</span><span class="sxs-lookup"><span data-stu-id="6cea3-112">dbid</span></span>  
    <span data-ttu-id="6cea3-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6cea3-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6cea3-114">包含資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="6cea3-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cea3-115">tablename</span><span class="sxs-lookup"><span data-stu-id="6cea3-115">tablename</span></span>  
    <span data-ttu-id="6cea3-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6cea3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6cea3-117">包含資料行的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="6cea3-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cea3-118">columnName</span><span class="sxs-lookup"><span data-stu-id="6cea3-118">columnName</span></span>  
    <span data-ttu-id="6cea3-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6cea3-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6cea3-120">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="6cea3-120">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cea3-121">columndef</span><span class="sxs-lookup"><span data-stu-id="6cea3-121">columndef</span></span>  
    <span data-ttu-id="6cea3-122">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="6cea3-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="6cea3-123">填入資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6cea3-123">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cea3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cea3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6cea3-125">參考</span><span class="sxs-lookup"><span data-stu-id="6cea3-125">Reference</span></span>

[<span data-ttu-id="6cea3-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6cea3-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6cea3-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6cea3-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6cea3-128">JetGetColumnInfo 多載</span><span class="sxs-lookup"><span data-stu-id="6cea3-128">JetGetColumnInfo overload</span></span>](./api.jetgetcolumninfo-method.md)

[<span data-ttu-id="6cea3-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6cea3-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
