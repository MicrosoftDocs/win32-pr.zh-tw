---
description: 深入瞭解： JetDeleteTable 方法
title: JetDeleteTable 方法
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b4128ae81484343bec7fb4f52a736db149f0eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112600"
---
# <a name="apijetdeletetable-method"></a><span data-ttu-id="c6208-103">JetDeleteTable 方法</span><span class="sxs-lookup"><span data-stu-id="c6208-103">Api.JetDeleteTable method</span></span>

<span data-ttu-id="c6208-104">從資料庫刪除資料表。</span><span class="sxs-lookup"><span data-stu-id="c6208-104">Deletes a table from a database.</span></span>

<span data-ttu-id="c6208-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c6208-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c6208-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c6208-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c6208-107">語法</span><span class="sxs-lookup"><span data-stu-id="c6208-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a><span data-ttu-id="c6208-108">參數</span><span class="sxs-lookup"><span data-stu-id="c6208-108">Parameters</span></span>

  - <span data-ttu-id="c6208-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c6208-109">sesid</span></span>  
    <span data-ttu-id="c6208-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6208-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c6208-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c6208-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6208-112">dbid</span><span class="sxs-lookup"><span data-stu-id="c6208-112">dbid</span></span>  
    <span data-ttu-id="c6208-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c6208-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="c6208-114">要從中刪除資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c6208-114">The database to delete the table from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c6208-115">資料表</span><span class="sxs-lookup"><span data-stu-id="c6208-115">table</span></span>  
    <span data-ttu-id="c6208-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c6208-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c6208-117">要刪除的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="c6208-117">The name of the table to delete.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6208-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6208-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c6208-119">參考</span><span class="sxs-lookup"><span data-stu-id="c6208-119">Reference</span></span>

[<span data-ttu-id="c6208-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c6208-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c6208-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c6208-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c6208-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c6208-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
