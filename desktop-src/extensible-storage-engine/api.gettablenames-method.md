---
description: 深入瞭解： GetTableNames 方法
title: GetTableNames 方法
TOCTitle: 'GetTableNames method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableNames(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablenames(v=EXCHG.10)
ms:contentKeyID: 55100650
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39a52d62ae5271353350df15c4c00833266094cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112609"
---
# <a name="apigettablenames-method"></a><span data-ttu-id="d6a7d-103">GetTableNames 方法</span><span class="sxs-lookup"><span data-stu-id="d6a7d-103">Api.GetTableNames method</span></span>

<span data-ttu-id="d6a7d-104">傳回資料庫中的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="d6a7d-104">Returns the names of the tables in the database.</span></span>

<span data-ttu-id="d6a7d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6a7d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d6a7d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="d6a7d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableNames ( _
    sesid As JET_SESID, _
    dbid As JET_DBID _
) As IEnumerable(Of String)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim returnValue As IEnumerable(Of String)

returnValue = Api.GetTableNames(sesid, _
    dbid)
```

``` csharp
public static IEnumerable<string> GetTableNames(
    JET_SESID sesid,
    JET_DBID dbid
)
```

#### <a name="parameters"></a><span data-ttu-id="d6a7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="d6a7d-108">Parameters</span></span>

  - <span data-ttu-id="d6a7d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d6a7d-109">sesid</span></span>  
    <span data-ttu-id="d6a7d-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d6a7d-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="d6a7d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6a7d-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d6a7d-112">dbid</span></span>  
    <span data-ttu-id="d6a7d-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6a7d-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d6a7d-114">包含資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="d6a7d-114">The database containing the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d6a7d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6a7d-115">Return value</span></span>

<span data-ttu-id="d6a7d-116">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="d6a7d-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[String](/dotnet/api/system.string)\></span></span>  
<span data-ttu-id="d6a7d-117">資料庫中資料表名稱的反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="d6a7d-117">An iterator over the names of the tables in the database.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6a7d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6a7d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6a7d-119">參考</span><span class="sxs-lookup"><span data-stu-id="d6a7d-119">Reference</span></span>

[<span data-ttu-id="d6a7d-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="d6a7d-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d6a7d-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="d6a7d-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d6a7d-122">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d6a7d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
