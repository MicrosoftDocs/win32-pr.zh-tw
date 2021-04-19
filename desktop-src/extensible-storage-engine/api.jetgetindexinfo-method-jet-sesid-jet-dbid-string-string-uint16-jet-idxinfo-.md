---
description: '深入瞭解： JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、UInt16、JET_IdxInfo) '
title: 'JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、UInt16、JET_IdxInfo) '
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100771
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
ms.openlocfilehash: 762437dba9e502de5c0650e4ae6df53d4629d791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980937"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-uint16-jet_idxinfo"></a><span data-ttu-id="16115-103">JetGetIndexInfo 方法 (JET_SESID、JET_DBID、字串、字串、UInt16、JET_IdxInfo) </span><span class="sxs-lookup"><span data-stu-id="16115-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="16115-104">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16115-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="16115-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="16115-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="16115-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16115-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16115-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="16115-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16115-108">語法</span><span class="sxs-lookup"><span data-stu-id="16115-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="16115-109">參數</span><span class="sxs-lookup"><span data-stu-id="16115-109">Parameters</span></span>

  - <span data-ttu-id="16115-110">sesid</span><span class="sxs-lookup"><span data-stu-id="16115-110">sesid</span></span>  
    <span data-ttu-id="16115-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="16115-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="16115-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="16115-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="16115-113">dbid</span><span class="sxs-lookup"><span data-stu-id="16115-113">dbid</span></span>  
    <span data-ttu-id="16115-114">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="16115-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="16115-115">要使用的資料庫。</span><span class="sxs-lookup"><span data-stu-id="16115-115">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="16115-116">tablename</span><span class="sxs-lookup"><span data-stu-id="16115-116">tablename</span></span>  
    <span data-ttu-id="16115-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="16115-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="16115-118">要取得其索引資訊的資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="16115-118">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="16115-119">indexname</span><span class="sxs-lookup"><span data-stu-id="16115-119">indexname</span></span>  
    <span data-ttu-id="16115-120">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="16115-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="16115-121">要取得相關資訊的索引名稱。</span><span class="sxs-lookup"><span data-stu-id="16115-121">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="16115-122">result</span><span class="sxs-lookup"><span data-stu-id="16115-122">result</span></span>  
    <span data-ttu-id="16115-123">類型： [system.object](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="16115-123">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="16115-124">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16115-124">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="16115-125">infoLevel</span><span class="sxs-lookup"><span data-stu-id="16115-125">infoLevel</span></span>  
    <span data-ttu-id="16115-126">類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="16115-126">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="16115-127">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="16115-127">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="16115-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16115-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16115-129">參考</span><span class="sxs-lookup"><span data-stu-id="16115-129">Reference</span></span>

[<span data-ttu-id="16115-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="16115-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="16115-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="16115-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="16115-132">JetGetIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="16115-132">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="16115-133">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="16115-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
