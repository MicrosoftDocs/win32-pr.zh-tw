---
description: '深入瞭解： JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、字串、JET_IdxInfo) '
title: 'JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、字串、JET_IdxInfo) '
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100769
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eed2ba4a3f578dda966b2b4530f26de25089681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970386"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-string-jet_idxinfo"></a><span data-ttu-id="49153-103">JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、字串、JET_IdxInfo) </span><span class="sxs-lookup"><span data-stu-id="49153-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="49153-104">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49153-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="49153-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="49153-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="49153-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="49153-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="49153-107">語法</span><span class="sxs-lookup"><span data-stu-id="49153-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="49153-108">參數</span><span class="sxs-lookup"><span data-stu-id="49153-108">Parameters</span></span>

  - <span data-ttu-id="49153-109">sesid</span><span class="sxs-lookup"><span data-stu-id="49153-109">sesid</span></span>  
    <span data-ttu-id="49153-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49153-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="49153-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="49153-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="49153-112">dbid</span><span class="sxs-lookup"><span data-stu-id="49153-112">dbid</span></span>  
    <span data-ttu-id="49153-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="49153-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="49153-114">要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="49153-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="49153-115">tablename</span><span class="sxs-lookup"><span data-stu-id="49153-115">tablename</span></span>  
    <span data-ttu-id="49153-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="49153-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="49153-117">要取得其索引資訊的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="49153-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="49153-118">indexname</span><span class="sxs-lookup"><span data-stu-id="49153-118">indexname</span></span>  
    <span data-ttu-id="49153-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="49153-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="49153-120">要取得相關資訊的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="49153-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="49153-121">result</span><span class="sxs-lookup"><span data-stu-id="49153-121">result</span></span>  
    <span data-ttu-id="49153-122">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="49153-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="49153-123">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="49153-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="49153-124">infoLevel</span><span class="sxs-lookup"><span data-stu-id="49153-124">infoLevel</span></span>  
    <span data-ttu-id="49153-125">類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="49153-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="49153-126">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="49153-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="49153-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49153-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="49153-128">參考</span><span class="sxs-lookup"><span data-stu-id="49153-128">Reference</span></span>

[<span data-ttu-id="49153-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="49153-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="49153-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="49153-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="49153-131">JetGetIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="49153-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="49153-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="49153-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
