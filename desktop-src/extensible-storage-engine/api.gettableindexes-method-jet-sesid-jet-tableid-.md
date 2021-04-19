---
description: '深入瞭解： GetTableIndexes 方法 (JET_SESID、JET_TABLEID) '
title: 'GetTableIndexes 方法 (JET_SESID，JET_TABLEID) '
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
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
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970149"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a><span data-ttu-id="af522-103">GetTableIndexes 方法 (JET_SESID，JET_TABLEID) </span><span class="sxs-lookup"><span data-stu-id="af522-103">Api.GetTableIndexes method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="af522-104">逐一查看資料表中的所有索引，傳回每個索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="af522-104">Iterates over all the indexes in the table, returning information about each one.</span></span>

<span data-ttu-id="af522-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af522-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af522-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="af522-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af522-107">語法</span><span class="sxs-lookup"><span data-stu-id="af522-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="af522-108">參數</span><span class="sxs-lookup"><span data-stu-id="af522-108">Parameters</span></span>

  - <span data-ttu-id="af522-109">sesid</span><span class="sxs-lookup"><span data-stu-id="af522-109">sesid</span></span>  
    <span data-ttu-id="af522-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af522-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="af522-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="af522-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="af522-112">tableid</span><span class="sxs-lookup"><span data-stu-id="af522-112">tableid</span></span>  
    <span data-ttu-id="af522-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af522-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="af522-114">要取出索引資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="af522-114">The table to retrieve index information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="af522-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="af522-115">Return value</span></span>

<span data-ttu-id="af522-116">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="af522-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="af522-117">資料表中每個索引的 IndexInfo 上的反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="af522-117">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af522-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af522-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af522-119">參考</span><span class="sxs-lookup"><span data-stu-id="af522-119">Reference</span></span>

[<span data-ttu-id="af522-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="af522-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="af522-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="af522-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="af522-122">GetTableIndexes 多載</span><span class="sxs-lookup"><span data-stu-id="af522-122">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="af522-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="af522-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
