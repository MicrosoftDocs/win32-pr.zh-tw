---
description: 深入瞭解： VistaApi. JetGetColumnInfo 方法
title: 'VistaApi. JetGetColumnInfo 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113585"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="8980b-103">VistaApi. JetGetColumnInfo 方法</span><span class="sxs-lookup"><span data-stu-id="8980b-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="8980b-104">抓取資料表中資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8980b-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="8980b-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="8980b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8980b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8980b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8980b-107">語法</span><span class="sxs-lookup"><span data-stu-id="8980b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="8980b-108">參數</span><span class="sxs-lookup"><span data-stu-id="8980b-108">Parameters</span></span>

  - <span data-ttu-id="8980b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8980b-109">sesid</span></span>  
    <span data-ttu-id="8980b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8980b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8980b-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="8980b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8980b-112">dbid</span><span class="sxs-lookup"><span data-stu-id="8980b-112">dbid</span></span>  
    <span data-ttu-id="8980b-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8980b-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="8980b-114">包含資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="8980b-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="8980b-115">tablename</span><span class="sxs-lookup"><span data-stu-id="8980b-115">tablename</span></span>  
    <span data-ttu-id="8980b-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8980b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8980b-117">包含資料行的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="8980b-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8980b-118">columnid</span><span class="sxs-lookup"><span data-stu-id="8980b-118">columnid</span></span>  
    <span data-ttu-id="8980b-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8980b-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8980b-120">資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8980b-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="8980b-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="8980b-121">columnbase</span></span>  
    <span data-ttu-id="8980b-122">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="8980b-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="8980b-123">填入資料表中資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8980b-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="8980b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8980b-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8980b-125">參考</span><span class="sxs-lookup"><span data-stu-id="8980b-125">Reference</span></span>

[<span data-ttu-id="8980b-126">VistaApi 類別</span><span class="sxs-lookup"><span data-stu-id="8980b-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="8980b-127">VistaApi 成員</span><span class="sxs-lookup"><span data-stu-id="8980b-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="8980b-128">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="8980b-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
