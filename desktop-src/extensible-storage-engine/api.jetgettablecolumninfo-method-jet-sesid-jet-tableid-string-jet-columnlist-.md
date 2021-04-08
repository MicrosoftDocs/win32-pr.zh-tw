---
description: '深入瞭解： JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串 JET_COLUMNLIST) '
title: 'JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) '
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100723
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 516dad3bbc93a12ec216c5c3caa35617ea989bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694631"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columnlist"></a><span data-ttu-id="85dc3-103">JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNLIST) </span><span class="sxs-lookup"><span data-stu-id="85dc3-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</span></span>

<span data-ttu-id="85dc3-104">抓取資料表中所有資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="85dc3-104">Retrieves information about all columns in the table.</span></span>

<span data-ttu-id="85dc3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85dc3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85dc3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="85dc3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85dc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="85dc3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columnlist)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a><span data-ttu-id="85dc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="85dc3-108">Parameters</span></span>

  - <span data-ttu-id="85dc3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="85dc3-109">sesid</span></span>  
    <span data-ttu-id="85dc3-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85dc3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="85dc3-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="85dc3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="85dc3-112">tableid</span><span class="sxs-lookup"><span data-stu-id="85dc3-112">tableid</span></span>  
    <span data-ttu-id="85dc3-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85dc3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="85dc3-114">包含資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="85dc3-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="85dc3-115">columnName</span><span class="sxs-lookup"><span data-stu-id="85dc3-115">columnName</span></span>  
    <span data-ttu-id="85dc3-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="85dc3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="85dc3-117">參數已忽略。</span><span class="sxs-lookup"><span data-stu-id="85dc3-117">The parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="85dc3-118">columnlist</span><span class="sxs-lookup"><span data-stu-id="85dc3-118">columnlist</span></span>  
    <span data-ttu-id="85dc3-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="85dc3-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)</span></span>  
    
    <span data-ttu-id="85dc3-120">填入資料表中資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="85dc3-120">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="85dc3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85dc3-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85dc3-122">參考</span><span class="sxs-lookup"><span data-stu-id="85dc3-122">Reference</span></span>

[<span data-ttu-id="85dc3-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="85dc3-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="85dc3-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="85dc3-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="85dc3-125">JetGetTableColumnInfo 多載</span><span class="sxs-lookup"><span data-stu-id="85dc3-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="85dc3-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="85dc3-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
