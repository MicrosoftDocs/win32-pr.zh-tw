---
description: '深入瞭解： GetTableIndexes 方法 (JET_SESID、JET_DBID、字串) '
title: 'GetTableIndexes 方法 (JET_SESID、JET_DBID、字串) '
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847653"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a><span data-ttu-id="36b36-103">GetTableIndexes 方法 (JET_SESID、JET_DBID、字串) </span><span class="sxs-lookup"><span data-stu-id="36b36-103">Api.GetTableIndexes method (JET_SESID, JET_DBID, String)</span></span>

<span data-ttu-id="36b36-104">逐一查看資料表中的所有索引，傳回每個資料表的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="36b36-104">Iterates over all the indexs in the table, returning information about each one.</span></span>

<span data-ttu-id="36b36-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36b36-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="36b36-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="36b36-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36b36-107">語法</span><span class="sxs-lookup"><span data-stu-id="36b36-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a><span data-ttu-id="36b36-108">參數</span><span class="sxs-lookup"><span data-stu-id="36b36-108">Parameters</span></span>

  - <span data-ttu-id="36b36-109">sesid</span><span class="sxs-lookup"><span data-stu-id="36b36-109">sesid</span></span>  
    <span data-ttu-id="36b36-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36b36-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="36b36-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="36b36-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="36b36-112">dbid</span><span class="sxs-lookup"><span data-stu-id="36b36-112">dbid</span></span>  
    <span data-ttu-id="36b36-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36b36-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="36b36-114">包含資料表的資料庫。</span><span class="sxs-lookup"><span data-stu-id="36b36-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="36b36-115">tablename</span><span class="sxs-lookup"><span data-stu-id="36b36-115">tablename</span></span>  
    <span data-ttu-id="36b36-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="36b36-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="36b36-117">資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="36b36-117">The name of the table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="36b36-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="36b36-118">Return value</span></span>

<span data-ttu-id="36b36-119">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="36b36-119">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="36b36-120">資料表中每個索引的 IndexInfo 上的反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="36b36-120">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="36b36-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36b36-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36b36-122">參考</span><span class="sxs-lookup"><span data-stu-id="36b36-122">Reference</span></span>

[<span data-ttu-id="36b36-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="36b36-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="36b36-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="36b36-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="36b36-125">GetTableIndexes 多載</span><span class="sxs-lookup"><span data-stu-id="36b36-125">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="36b36-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="36b36-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
