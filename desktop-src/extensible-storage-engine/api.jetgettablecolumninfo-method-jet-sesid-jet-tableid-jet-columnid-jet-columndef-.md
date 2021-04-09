---
description: '深入瞭解： JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID JET_COLUMNDEF) '
title: 'JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID JET_COLUMNDEF) '
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100730
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa120cf78001ed608a2385e07f388ae91bc9b425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694632"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-jet_columnid-jet_columndef"></a><span data-ttu-id="4dfe3-103">JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、JET_COLUMNID JET_COLUMNDEF) </span><span class="sxs-lookup"><span data-stu-id="4dfe3-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</span></span>

<span data-ttu-id="4dfe3-104">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="4dfe3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4dfe3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4dfe3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4dfe3-107">語法</span><span class="sxs-lookup"><span data-stu-id="4dfe3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnid, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="4dfe3-108">參數</span><span class="sxs-lookup"><span data-stu-id="4dfe3-108">Parameters</span></span>

  - <span data-ttu-id="4dfe3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="4dfe3-109">sesid</span></span>  
    <span data-ttu-id="4dfe3-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dfe3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4dfe3-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dfe3-112">tableid</span><span class="sxs-lookup"><span data-stu-id="4dfe3-112">tableid</span></span>  
    <span data-ttu-id="4dfe3-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dfe3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4dfe3-114">包含資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dfe3-115">columnid</span><span class="sxs-lookup"><span data-stu-id="4dfe3-115">columnid</span></span>  
    <span data-ttu-id="4dfe3-116">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dfe3-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4dfe3-117">資料行的 columnid。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-117">The columnid of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dfe3-118">columndef</span><span class="sxs-lookup"><span data-stu-id="4dfe3-118">columndef</span></span>  
    <span data-ttu-id="4dfe3-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="4dfe3-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="4dfe3-120">填入資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4dfe3-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dfe3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4dfe3-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4dfe3-122">參考</span><span class="sxs-lookup"><span data-stu-id="4dfe3-122">Reference</span></span>

[<span data-ttu-id="4dfe3-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4dfe3-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4dfe3-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4dfe3-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4dfe3-125">JetGetTableColumnInfo 多載</span><span class="sxs-lookup"><span data-stu-id="4dfe3-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="4dfe3-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4dfe3-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
