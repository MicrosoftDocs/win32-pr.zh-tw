---
description: '深入瞭解： GetTableColumns 方法 (JET_SESID、JET_TABLEID) '
title: 'GetTableColumns 方法 (JET_SESID，JET_TABLEID) '
TOCTitle: GetTableColumns method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumns(v=EXCHG.10)
ms:contentKeyID: 55107218
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 393f730920ce7abb3ef24916c9e1c9e9591ba020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111953"
---
# <a name="apigettablecolumns-method-jet_sesid-jet_tableid"></a><span data-ttu-id="f371c-103">GetTableColumns 方法 (JET_SESID，JET_TABLEID) </span><span class="sxs-lookup"><span data-stu-id="f371c-103">Api.GetTableColumns method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="f371c-104">逐一查看資料表中的所有資料行，並傳回每個資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f371c-104">Iterates over all the columns in the table, returning information about each one.</span></span>

<span data-ttu-id="f371c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f371c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f371c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f371c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f371c-107">語法</span><span class="sxs-lookup"><span data-stu-id="f371c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of ColumnInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of ColumnInfo)

returnValue = Api.GetTableColumns(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<ColumnInfo> GetTableColumns(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="f371c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f371c-108">Parameters</span></span>

  - <span data-ttu-id="f371c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f371c-109">sesid</span></span>  
    <span data-ttu-id="f371c-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f371c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f371c-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f371c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f371c-112">tableid</span><span class="sxs-lookup"><span data-stu-id="f371c-112">tableid</span></span>  
    <span data-ttu-id="f371c-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f371c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f371c-114">要取得其資料行資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="f371c-114">The table to retrieve column information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f371c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f371c-115">Return value</span></span>

<span data-ttu-id="f371c-116">類型： [system.object](/dotnet/api/system.collections.generic.ienumerable-1) 。\<[ColumnInfo](./columninfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="f371c-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[ColumnInfo](./columninfo-class.md)\></span></span>  
<span data-ttu-id="f371c-117">資料表中每個資料行的 ColumnInfo 反覆運算器。</span><span class="sxs-lookup"><span data-stu-id="f371c-117">An iterator over ColumnInfo for each column in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f371c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f371c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f371c-119">參考</span><span class="sxs-lookup"><span data-stu-id="f371c-119">Reference</span></span>

[<span data-ttu-id="f371c-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f371c-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f371c-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f371c-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f371c-122">GetTableColumns 多載</span><span class="sxs-lookup"><span data-stu-id="f371c-122">GetTableColumns overload</span></span>](./api.gettablecolumns-method.md)

[<span data-ttu-id="f371c-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f371c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
