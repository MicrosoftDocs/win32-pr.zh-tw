---
description: 深入瞭解： JetRetrieveKey 方法
title: JetRetrieveKey 方法
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984251"
---
# <a name="apijetretrievekey-method"></a><span data-ttu-id="901ae-103">JetRetrieveKey 方法</span><span class="sxs-lookup"><span data-stu-id="901ae-103">Api.JetRetrieveKey method</span></span>

<span data-ttu-id="901ae-104">在資料指標的目前位置，抓取索引項目的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="901ae-104">Retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="901ae-105">另請參閱 [RetrieveKey (JET_SESID、JET_TABLEID、RetrieveKeyGrbit) ](./api.retrievekey-method.md)。</span><span class="sxs-lookup"><span data-stu-id="901ae-105">Also see [RetrieveKey(JET_SESID, JET_TABLEID, RetrieveKeyGrbit)](./api.retrievekey-method.md).</span></span>

<span data-ttu-id="901ae-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="901ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="901ae-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="901ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="901ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="901ae-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="901ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="901ae-109">Parameters</span></span>

  - <span data-ttu-id="901ae-110">sesid</span><span class="sxs-lookup"><span data-stu-id="901ae-110">sesid</span></span>  
    <span data-ttu-id="901ae-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="901ae-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="901ae-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="901ae-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="901ae-113">tableid</span><span class="sxs-lookup"><span data-stu-id="901ae-113">tableid</span></span>  
    <span data-ttu-id="901ae-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="901ae-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="901ae-115">從中取出索引鍵的資料指標。</span><span class="sxs-lookup"><span data-stu-id="901ae-115">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="901ae-116">data</span><span class="sxs-lookup"><span data-stu-id="901ae-116">data</span></span>  
    <span data-ttu-id="901ae-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="901ae-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="901ae-118">要在其中取出索引鍵的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="901ae-118">The buffer to retrieve the key into.</span></span>

<!-- end list -->

  - <span data-ttu-id="901ae-119">dataSize</span><span class="sxs-lookup"><span data-stu-id="901ae-119">dataSize</span></span>  
    <span data-ttu-id="901ae-120">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="901ae-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="901ae-121">緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="901ae-121">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="901ae-122">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="901ae-122">actualDataSize</span></span>  
    <span data-ttu-id="901ae-123">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="901ae-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="901ae-124">傳回資料的實際大小。</span><span class="sxs-lookup"><span data-stu-id="901ae-124">Returns the actual size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="901ae-125">grbit</span><span class="sxs-lookup"><span data-stu-id="901ae-125">grbit</span></span>  
    <span data-ttu-id="901ae-126">型別： [RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="901ae-126">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="901ae-127">取得索引鍵選項。</span><span class="sxs-lookup"><span data-stu-id="901ae-127">Retrieve key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="901ae-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="901ae-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="901ae-129">參考</span><span class="sxs-lookup"><span data-stu-id="901ae-129">Reference</span></span>

[<span data-ttu-id="901ae-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="901ae-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="901ae-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="901ae-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="901ae-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="901ae-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
