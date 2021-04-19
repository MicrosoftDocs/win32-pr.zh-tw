---
description: '深入瞭解： JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST JET_IdxInfo) '
title: 'JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST JET_IdxInfo) '
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55107227
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cc7c110c139c66fdd5d8baee4ebb102922adf7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970387"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist-jet_idxinfo"></a><span data-ttu-id="cb39e-103">JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST JET_IdxInfo) </span><span class="sxs-lookup"><span data-stu-id="cb39e-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</span></span>

<span data-ttu-id="cb39e-104">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb39e-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="cb39e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb39e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb39e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cb39e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb39e-107">語法</span><span class="sxs-lookup"><span data-stu-id="cb39e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXLIST, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXLIST
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXLIST result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="cb39e-108">參數</span><span class="sxs-lookup"><span data-stu-id="cb39e-108">Parameters</span></span>

  - <span data-ttu-id="cb39e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="cb39e-109">sesid</span></span>  
    <span data-ttu-id="cb39e-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb39e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cb39e-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="cb39e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb39e-112">dbid</span><span class="sxs-lookup"><span data-stu-id="cb39e-112">dbid</span></span>  
    <span data-ttu-id="cb39e-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb39e-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="cb39e-114">要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="cb39e-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb39e-115">tablename</span><span class="sxs-lookup"><span data-stu-id="cb39e-115">tablename</span></span>  
    <span data-ttu-id="cb39e-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cb39e-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cb39e-117">要取得其索引資訊的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="cb39e-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb39e-118">indexname</span><span class="sxs-lookup"><span data-stu-id="cb39e-118">indexname</span></span>  
    <span data-ttu-id="cb39e-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cb39e-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="cb39e-120">要取得相關資訊的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="cb39e-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb39e-121">result</span><span class="sxs-lookup"><span data-stu-id="cb39e-121">result</span></span>  
    <span data-ttu-id="cb39e-122">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="cb39e-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="cb39e-123">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb39e-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb39e-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="cb39e-124">infoLevel</span></span>  
    <span data-ttu-id="cb39e-125">類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="cb39e-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="cb39e-126">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="cb39e-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb39e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cb39e-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb39e-128">參考</span><span class="sxs-lookup"><span data-stu-id="cb39e-128">Reference</span></span>

[<span data-ttu-id="cb39e-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="cb39e-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cb39e-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="cb39e-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cb39e-131">JetGetIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="cb39e-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="cb39e-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cb39e-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
