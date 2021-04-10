---
description: 深入瞭解： JetRenameTable 方法
title: JetRenameTable 方法
TOCTitle: 'JetRenameTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenametable(v=EXCHG.10)
ms:contentKeyID: 55100788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bb108498501df50a43964f5b069860d10c39258
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026142"
---
# <a name="apijetrenametable-method"></a><span data-ttu-id="b757b-103">JetRenameTable 方法</span><span class="sxs-lookup"><span data-stu-id="b757b-103">Api.JetRenameTable method</span></span>

<span data-ttu-id="b757b-104">變更現有資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b757b-104">Changes the name of an existing table.</span></span>

<span data-ttu-id="b757b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b757b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b757b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b757b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b757b-107">語法</span><span class="sxs-lookup"><span data-stu-id="b757b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    newTableName As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim newTableName As StringApi.JetRenameTable(sesid, dbid, _
    tableName, newTableName)
```

``` csharp
public static void JetRenameTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string newTableName
)
```

#### <a name="parameters"></a><span data-ttu-id="b757b-108">參數</span><span class="sxs-lookup"><span data-stu-id="b757b-108">Parameters</span></span>

  - <span data-ttu-id="b757b-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b757b-109">sesid</span></span>  
    <span data-ttu-id="b757b-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b757b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b757b-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="b757b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b757b-112">dbid</span><span class="sxs-lookup"><span data-stu-id="b757b-112">dbid</span></span>  
    <span data-ttu-id="b757b-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b757b-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="b757b-114">包含資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="b757b-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b757b-115">tableName</span><span class="sxs-lookup"><span data-stu-id="b757b-115">tableName</span></span>  
    <span data-ttu-id="b757b-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b757b-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b757b-117">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b757b-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="b757b-118">newTableName</span><span class="sxs-lookup"><span data-stu-id="b757b-118">newTableName</span></span>  
    <span data-ttu-id="b757b-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b757b-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b757b-120">資料表的新名稱。</span><span class="sxs-lookup"><span data-stu-id="b757b-120">The new name of the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="b757b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b757b-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b757b-122">參考</span><span class="sxs-lookup"><span data-stu-id="b757b-122">Reference</span></span>

[<span data-ttu-id="b757b-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="b757b-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b757b-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="b757b-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b757b-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b757b-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
