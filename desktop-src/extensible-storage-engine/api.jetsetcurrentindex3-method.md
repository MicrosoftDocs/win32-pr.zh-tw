---
description: 深入瞭解： JetSetCurrentIndex3 方法
title: JetSetCurrentIndex3 方法
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997545"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="53932-103">JetSetCurrentIndex3 方法</span><span class="sxs-lookup"><span data-stu-id="53932-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="53932-104">設定資料指標的目前索引。</span><span class="sxs-lookup"><span data-stu-id="53932-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="53932-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53932-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53932-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="53932-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53932-107">語法</span><span class="sxs-lookup"><span data-stu-id="53932-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="53932-108">參數</span><span class="sxs-lookup"><span data-stu-id="53932-108">Parameters</span></span>

  - <span data-ttu-id="53932-109">sesid</span><span class="sxs-lookup"><span data-stu-id="53932-109">sesid</span></span>  
    <span data-ttu-id="53932-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53932-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="53932-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="53932-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="53932-112">tableid</span><span class="sxs-lookup"><span data-stu-id="53932-112">tableid</span></span>  
    <span data-ttu-id="53932-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="53932-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="53932-114">要在其上設定索引的資料指標。</span><span class="sxs-lookup"><span data-stu-id="53932-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="53932-115">索引</span><span class="sxs-lookup"><span data-stu-id="53932-115">index</span></span>  
    <span data-ttu-id="53932-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="53932-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="53932-117">要選取之索引的名稱。</span><span class="sxs-lookup"><span data-stu-id="53932-117">The name of the index to be selected.</span></span> <span data-ttu-id="53932-118">如果這是 null 或空白，則會選取主要索引。</span><span class="sxs-lookup"><span data-stu-id="53932-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="53932-119">grbit</span><span class="sxs-lookup"><span data-stu-id="53932-119">grbit</span></span>  
    <span data-ttu-id="53932-120">型別： [SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="53932-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="53932-121">設定索引選項。</span><span class="sxs-lookup"><span data-stu-id="53932-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="53932-122">itagSequence</span><span class="sxs-lookup"><span data-stu-id="53932-122">itagSequence</span></span>  
    <span data-ttu-id="53932-123">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="53932-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="53932-124">多值資料行值的序號，此值會用來將資料指標放置在新的索引上。</span><span class="sxs-lookup"><span data-stu-id="53932-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="53932-125">此參數只會與 [NoMove](./setcurrentindexgrbit-enumeration.md)搭配使用。</span><span class="sxs-lookup"><span data-stu-id="53932-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="53932-126">當這個參數不存在或設為零時，其值會假設為1。</span><span class="sxs-lookup"><span data-stu-id="53932-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="53932-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53932-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53932-128">參考</span><span class="sxs-lookup"><span data-stu-id="53932-128">Reference</span></span>

[<span data-ttu-id="53932-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="53932-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="53932-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="53932-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="53932-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="53932-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
