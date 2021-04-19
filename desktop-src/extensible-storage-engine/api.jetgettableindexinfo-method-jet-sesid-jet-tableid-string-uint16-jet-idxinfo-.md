---
description: '深入瞭解： JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、字串、UInt16、JET_IdxInfo) '
title: 'JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、String、UInt16、JET_IdxInfo) '
TOCTitle: JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.UInt16@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100747
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
ms.openlocfilehash: 5a5e1f5e6908f33d211c5a32a3b9d34e55098101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001422"
---
# <a name="apijetgettableindexinfo-method-jet_sesid-jet_tableid-string-uint16-jet_idxinfo"></a><span data-ttu-id="f3008-103">JetGetTableIndexInfo 方法 (JET_SESID、JET_TABLEID、String、UInt16、JET_IdxInfo) </span><span class="sxs-lookup"><span data-stu-id="f3008-103">Api.JetGetTableIndexInfo method (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</span></span>

<span data-ttu-id="f3008-104">抓取資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3008-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="f3008-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="f3008-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="f3008-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3008-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3008-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f3008-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3008-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3008-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetTableIndexInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexname As String, _
    <OutAttribute> ByRef result As UShort, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexname As String
Dim result As UShort
Dim infoLevel As JET_IdxInfoApi.JetGetTableIndexInfo(sesid, _
    tableid, indexname, result, infoLevel)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetTableIndexInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexname,
    out ushort result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="f3008-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3008-109">Parameters</span></span>

  - <span data-ttu-id="f3008-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f3008-110">sesid</span></span>  
    <span data-ttu-id="f3008-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f3008-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f3008-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="f3008-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f3008-113">tableid</span><span class="sxs-lookup"><span data-stu-id="f3008-113">tableid</span></span>  
    <span data-ttu-id="f3008-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f3008-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f3008-115">要取出相關索引資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="f3008-115">The table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="f3008-116">indexname</span><span class="sxs-lookup"><span data-stu-id="f3008-116">indexname</span></span>  
    <span data-ttu-id="f3008-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f3008-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f3008-118">索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3008-118">The name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="f3008-119">result</span><span class="sxs-lookup"><span data-stu-id="f3008-119">result</span></span>  
    <span data-ttu-id="f3008-120">類型： [system.object](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="f3008-120">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="f3008-121">填入資料表上索引的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3008-121">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f3008-122">infoLevel</span><span class="sxs-lookup"><span data-stu-id="f3008-122">infoLevel</span></span>  
    <span data-ttu-id="f3008-123">類型： [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f3008-123">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="f3008-124">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="f3008-124">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3008-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3008-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3008-126">參考</span><span class="sxs-lookup"><span data-stu-id="f3008-126">Reference</span></span>

[<span data-ttu-id="f3008-127">Api 類別</span><span class="sxs-lookup"><span data-stu-id="f3008-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f3008-128">Api 成員</span><span class="sxs-lookup"><span data-stu-id="f3008-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f3008-129">JetGetTableIndexInfo 多載</span><span class="sxs-lookup"><span data-stu-id="f3008-129">JetGetTableIndexInfo overload</span></span>](./api.jetgettableindexinfo-method.md)

[<span data-ttu-id="f3008-130">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f3008-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
