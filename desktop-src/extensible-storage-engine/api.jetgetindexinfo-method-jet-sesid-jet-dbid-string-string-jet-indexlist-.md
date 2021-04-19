---
description: '深入瞭解： JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST) '
title: 'JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST) '
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
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
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972392"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a><span data-ttu-id="4afa5-103">JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、JET_INDEXLIST) </span><span class="sxs-lookup"><span data-stu-id="4afa5-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="4afa5-104">**注意：此 API 現已淘汰。**</span><span class="sxs-lookup"><span data-stu-id="4afa5-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="4afa5-105">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4afa5-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="4afa5-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4afa5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4afa5-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4afa5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4afa5-108">語法</span><span class="sxs-lookup"><span data-stu-id="4afa5-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="4afa5-109">參數</span><span class="sxs-lookup"><span data-stu-id="4afa5-109">Parameters</span></span>

  - <span data-ttu-id="4afa5-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4afa5-110">sesid</span></span>  
    <span data-ttu-id="4afa5-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4afa5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4afa5-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="4afa5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4afa5-113">dbid</span><span class="sxs-lookup"><span data-stu-id="4afa5-113">dbid</span></span>  
    <span data-ttu-id="4afa5-114">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4afa5-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="4afa5-115">要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4afa5-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4afa5-116">tablename</span><span class="sxs-lookup"><span data-stu-id="4afa5-116">tablename</span></span>  
    <span data-ttu-id="4afa5-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4afa5-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4afa5-118">要取得其索引資訊的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="4afa5-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="4afa5-119">忽略</span><span class="sxs-lookup"><span data-stu-id="4afa5-119">ignored</span></span>  
    <span data-ttu-id="4afa5-120">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4afa5-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4afa5-121">這個參數已忽略。</span><span class="sxs-lookup"><span data-stu-id="4afa5-121">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="4afa5-122">indexlist</span><span class="sxs-lookup"><span data-stu-id="4afa5-122">indexlist</span></span>  
    <span data-ttu-id="4afa5-123">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="4afa5-123">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="4afa5-124">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4afa5-124">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="4afa5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4afa5-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4afa5-126">參考</span><span class="sxs-lookup"><span data-stu-id="4afa5-126">Reference</span></span>

[<span data-ttu-id="4afa5-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="4afa5-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4afa5-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="4afa5-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4afa5-129">JetGetIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="4afa5-129">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="4afa5-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4afa5-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
