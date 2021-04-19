---
description: '深入瞭解： JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) '
title: 'JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) '
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3e276d118dcbb13fe7e67b33e8705581b16be67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979989"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-int32-jet_tblinfo"></a><span data-ttu-id="03b92-103">JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、Int32、JET_TblInfo) </span><span class="sxs-lookup"><span data-stu-id="03b92-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</span></span>

<span data-ttu-id="03b92-104">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="03b92-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="03b92-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="03b92-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="03b92-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="03b92-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="03b92-107">語法</span><span class="sxs-lookup"><span data-stu-id="03b92-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As Integer, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As Integer
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="03b92-108">參數</span><span class="sxs-lookup"><span data-stu-id="03b92-108">Parameters</span></span>

  - <span data-ttu-id="03b92-109">sesid</span><span class="sxs-lookup"><span data-stu-id="03b92-109">sesid</span></span>  
    <span data-ttu-id="03b92-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="03b92-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="03b92-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="03b92-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="03b92-112">tableid</span><span class="sxs-lookup"><span data-stu-id="03b92-112">tableid</span></span>  
    <span data-ttu-id="03b92-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="03b92-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="03b92-114">要取得相關資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="03b92-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="03b92-115">result</span><span class="sxs-lookup"><span data-stu-id="03b92-115">result</span></span>  
    <span data-ttu-id="03b92-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="03b92-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="03b92-117">取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="03b92-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="03b92-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="03b92-118">infoLevel</span></span>  
    <span data-ttu-id="03b92-119">類型： [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="03b92-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="03b92-120">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="03b92-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="03b92-121">備註</span><span class="sxs-lookup"><span data-stu-id="03b92-121">Remarks</span></span>

<span data-ttu-id="03b92-122">這個多載會搭配 [SpaceOwned](./jet-tblinfo-enumeration.md) 和 [SpaceAvailable](./jet-tblinfo-enumeration.md)使用。</span><span class="sxs-lookup"><span data-stu-id="03b92-122">This overload is used with [SpaceOwned](./jet-tblinfo-enumeration.md) and [SpaceAvailable](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="03b92-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03b92-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="03b92-124">參考</span><span class="sxs-lookup"><span data-stu-id="03b92-124">Reference</span></span>

[<span data-ttu-id="03b92-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="03b92-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="03b92-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="03b92-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="03b92-127">JetGetTableInfo 多載</span><span class="sxs-lookup"><span data-stu-id="03b92-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="03b92-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="03b92-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
