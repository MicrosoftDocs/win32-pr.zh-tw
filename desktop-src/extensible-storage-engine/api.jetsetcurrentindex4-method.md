---
description: 深入瞭解： JetSetCurrentIndex4 方法
title: JetSetCurrentIndex4 方法
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970780"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="2deb2-103">JetSetCurrentIndex4 方法</span><span class="sxs-lookup"><span data-stu-id="2deb2-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="2deb2-104">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="2deb2-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="2deb2-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2deb2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2deb2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2deb2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2deb2-107">語法</span><span class="sxs-lookup"><span data-stu-id="2deb2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="2deb2-108">參數</span><span class="sxs-lookup"><span data-stu-id="2deb2-108">Parameters</span></span>

  - <span data-ttu-id="2deb2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="2deb2-109">sesid</span></span>  
    <span data-ttu-id="2deb2-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2deb2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2deb2-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="2deb2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deb2-112">tableid</span><span class="sxs-lookup"><span data-stu-id="2deb2-112">tableid</span></span>  
    <span data-ttu-id="2deb2-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2deb2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="2deb2-114">要在其上設定索引的資料指標。</span><span class="sxs-lookup"><span data-stu-id="2deb2-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deb2-115">索引</span><span class="sxs-lookup"><span data-stu-id="2deb2-115">index</span></span>  
    <span data-ttu-id="2deb2-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2deb2-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2deb2-117">要選取之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="2deb2-117">The name of the index to be selected.</span></span> <span data-ttu-id="2deb2-118">如果這是 null 或空白，則會選取主要索引。</span><span class="sxs-lookup"><span data-stu-id="2deb2-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deb2-119">indexid</span><span class="sxs-lookup"><span data-stu-id="2deb2-119">indexid</span></span>  
    <span data-ttu-id="2deb2-120">類型： [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="2deb2-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="2deb2-121">要選取之索引的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2deb2-121">The id of the index to select.</span></span> <span data-ttu-id="2deb2-122">您可以使用 JetGetIndexInfo 或 JetGetTableIndexInfo 搭配 [IndexId](./jet-idxinfo-enumeration.md) 選項來取得此識別碼。</span><span class="sxs-lookup"><span data-stu-id="2deb2-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deb2-123">grbit</span><span class="sxs-lookup"><span data-stu-id="2deb2-123">grbit</span></span>  
    <span data-ttu-id="2deb2-124">型別： [SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="2deb2-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2deb2-125">設定索引選項。</span><span class="sxs-lookup"><span data-stu-id="2deb2-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="2deb2-126">itagSequence</span><span class="sxs-lookup"><span data-stu-id="2deb2-126">itagSequence</span></span>  
    <span data-ttu-id="2deb2-127">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2deb2-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2deb2-128">多值資料行值的序號，此值會用來將資料指標放置在新的索引上。</span><span class="sxs-lookup"><span data-stu-id="2deb2-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="2deb2-129">此參數只會與 [NoMove](./setcurrentindexgrbit-enumeration.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="2deb2-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="2deb2-130">當這個參數不存在或設為零時，其值會假設為1。</span><span class="sxs-lookup"><span data-stu-id="2deb2-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="2deb2-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2deb2-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2deb2-132">參考</span><span class="sxs-lookup"><span data-stu-id="2deb2-132">Reference</span></span>

[<span data-ttu-id="2deb2-133">Api 類別</span><span class="sxs-lookup"><span data-stu-id="2deb2-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2deb2-134">Api 成員</span><span class="sxs-lookup"><span data-stu-id="2deb2-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2deb2-135">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2deb2-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
