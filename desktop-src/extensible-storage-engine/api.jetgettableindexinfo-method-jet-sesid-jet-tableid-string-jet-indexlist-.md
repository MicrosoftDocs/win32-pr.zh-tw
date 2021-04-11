---
description: '深入瞭解： JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串 JET_INDEXLIST) '
title: 'JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST) '
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100752
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5a39fba54463f7a55fd6a8521f5c905da4afb4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191680"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-jet_indexlist"></a><span data-ttu-id="68620-103">JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_INDEXLIST) </span><span class="sxs-lookup"><span data-stu-id="68620-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</span></span>

<span data-ttu-id="68620-104">**注意：此 API 現已淘汰。**</span><span class="sxs-lookup"><span data-stu-id="68620-104">**NOTE: This API is now obsolete.**</span></span>

<span data-ttu-id="68620-105">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68620-105">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="68620-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68620-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68620-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="68620-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68620-108">語法</span><span class="sxs-lookup"><span data-stu-id="68620-108">Syntax</span></span>

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim indexlist As JET_INDEXLISTApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a><span data-ttu-id="68620-109">參數</span><span class="sxs-lookup"><span data-stu-id="68620-109">Parameters</span></span>

  - <span data-ttu-id="68620-110">sesid</span><span class="sxs-lookup"><span data-stu-id="68620-110">sesid</span></span>  
    <span data-ttu-id="68620-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68620-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="68620-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="68620-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="68620-113">tableid</span><span class="sxs-lookup"><span data-stu-id="68620-113">tableid</span></span>  
    <span data-ttu-id="68620-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="68620-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="68620-115">要取出相關索引資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="68620-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="68620-116">indexname</span><span class="sxs-lookup"><span data-stu-id="68620-116">indexname</span></span>  
    <span data-ttu-id="68620-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="68620-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="68620-118">這個參數已忽略。</span><span class="sxs-lookup"><span data-stu-id="68620-118">This parameter is ignored.</span></span>

<!-- end list -->

  - <span data-ttu-id="68620-119">indexlist</span><span class="sxs-lookup"><span data-stu-id="68620-119">indexlist</span></span>  
    <span data-ttu-id="68620-120">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="68620-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="68620-121">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="68620-121">Filled in with information about indexes on the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="68620-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68620-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68620-123">參考</span><span class="sxs-lookup"><span data-stu-id="68620-123">Reference</span></span>

[<span data-ttu-id="68620-124">Api 類別</span><span class="sxs-lookup"><span data-stu-id="68620-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="68620-125">Api 成員</span><span class="sxs-lookup"><span data-stu-id="68620-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="68620-126">JetGetTableIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="68620-126">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="68620-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="68620-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
