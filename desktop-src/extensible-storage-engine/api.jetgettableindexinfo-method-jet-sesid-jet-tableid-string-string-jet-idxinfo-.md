---
description: '深入瞭解： JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、字串、JET_IdxInfo) '
title: 'JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、字串、JET_IdxInfo) '
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100750
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 62291587ca1c07da74c2b646870751f3b8af981b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992422"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-string-jet_idxinfo"></a><span data-ttu-id="2721f-103">JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、字串、JET_IdxInfo) </span><span class="sxs-lookup"><span data-stu-id="2721f-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="2721f-104">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2721f-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="2721f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2721f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2721f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2721f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2721f-107">語法</span><span class="sxs-lookup"><span data-stu-id="2721f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="2721f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2721f-108">Parameters</span></span>

  - <span data-ttu-id="2721f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2721f-109">sesid</span></span>  
    <span data-ttu-id="2721f-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2721f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2721f-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="2721f-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2721f-112">tableid</span><span class="sxs-lookup"><span data-stu-id="2721f-112">tableid</span></span>  
    <span data-ttu-id="2721f-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2721f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2721f-114">要取出相關索引資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="2721f-114">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="2721f-115">indexname</span><span class="sxs-lookup"><span data-stu-id="2721f-115">indexname</span></span>  
    <span data-ttu-id="2721f-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2721f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2721f-117">索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="2721f-117">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="2721f-118">result</span><span class="sxs-lookup"><span data-stu-id="2721f-118">result</span></span>  
    <span data-ttu-id="2721f-119">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2721f-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2721f-120">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2721f-120">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="2721f-121">infoLevel</span><span class="sxs-lookup"><span data-stu-id="2721f-121">infoLevel</span></span>  
    <span data-ttu-id="2721f-122">類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2721f-122">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="2721f-123">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="2721f-123">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="2721f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2721f-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2721f-125">參考</span><span class="sxs-lookup"><span data-stu-id="2721f-125">Reference</span></span>

[<span data-ttu-id="2721f-126">Api 類別</span><span class="sxs-lookup"><span data-stu-id="2721f-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2721f-127">Api 成員</span><span class="sxs-lookup"><span data-stu-id="2721f-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2721f-128">JetGetTableIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="2721f-128">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="2721f-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2721f-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
