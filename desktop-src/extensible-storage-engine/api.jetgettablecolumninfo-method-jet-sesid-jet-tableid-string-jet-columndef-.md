---
description: '深入瞭解： JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串 JET_COLUMNDEF) '
title: 'JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNDEF) '
TOCTitle: JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettablecolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100724
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
ms.openlocfilehash: 60e984fdb1577dc69a352c327c1af605e0d441d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318676"
---
# <a name="apijetgettablecolumninfo-method-jet_sesid-jet_tableid-string-jet_columndef"></a><span data-ttu-id="f8c58-103">JetGetTableColumnInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_COLUMNDEF) </span><span class="sxs-lookup"><span data-stu-id="f8c58-103">Api.JetGetTableColumnInfo method (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</span></span>

<span data-ttu-id="f8c58-104">抓取資料表資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f8c58-104">Retrieves information about a table column.</span></span>

<span data-ttu-id="f8c58-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8c58-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8c58-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f8c58-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8c58-107">語法</span><span class="sxs-lookup"><span data-stu-id="f8c58-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableColumnInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetTableColumnInfo(sesid, _
    tableid, columnName, columndef)
```

``` csharp
public static void JetGetTableColumnInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a><span data-ttu-id="f8c58-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8c58-108">Parameters</span></span>

  - <span data-ttu-id="f8c58-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f8c58-109">sesid</span></span>  
    <span data-ttu-id="f8c58-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8c58-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8c58-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f8c58-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c58-112">tableid</span><span class="sxs-lookup"><span data-stu-id="f8c58-112">tableid</span></span>  
    <span data-ttu-id="f8c58-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8c58-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f8c58-114">包含資料行的資料表。</span><span class="sxs-lookup"><span data-stu-id="f8c58-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c58-115">columnName</span><span class="sxs-lookup"><span data-stu-id="f8c58-115">columnName</span></span>  
    <span data-ttu-id="f8c58-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f8c58-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f8c58-117">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="f8c58-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8c58-118">columndef</span><span class="sxs-lookup"><span data-stu-id="f8c58-118">columndef</span></span>  
    <span data-ttu-id="f8c58-119">類型： [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="f8c58-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="f8c58-120">填入資料行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f8c58-120">Filled in with information about the column.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8c58-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8c58-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8c58-122">參考</span><span class="sxs-lookup"><span data-stu-id="f8c58-122">Reference</span></span>

[<span data-ttu-id="f8c58-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f8c58-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8c58-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f8c58-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8c58-125">JetGetTableColumnInfo 多載</span><span class="sxs-lookup"><span data-stu-id="f8c58-125">JetGetTableColumnInfo overload</span></span>](./api.jetgettablecolumninfo-method.md)

[<span data-ttu-id="f8c58-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f8c58-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
