---
description: 深入瞭解： JetGetSecondaryIndexBookmark 方法
title: JetGetSecondaryIndexBookmark 方法
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026144"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="5bdf7-103">JetGetSecondaryIndexBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="5bdf7-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="5bdf7-104">在資料指標的目前位置，抓取次要索引項目的特殊書簽。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="5bdf7-105">然後，您可以使用這個書簽，利用 JetGotoSecondaryIndexBookmark 將該資料指標有效率地重新放置到相同的索引項目。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="5bdf7-106">當在包含重複索引鍵或包含相同記錄之多個索引項目的次要索引上重新置放時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="5bdf7-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5bdf7-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bdf7-109">語法</span><span class="sxs-lookup"><span data-stu-id="5bdf7-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5bdf7-110">參數</span><span class="sxs-lookup"><span data-stu-id="5bdf7-110">Parameters</span></span>

  - <span data-ttu-id="5bdf7-111">sesid</span><span class="sxs-lookup"><span data-stu-id="5bdf7-111">sesid</span></span>  
    <span data-ttu-id="5bdf7-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5bdf7-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-114">tableid</span><span class="sxs-lookup"><span data-stu-id="5bdf7-114">tableid</span></span>  
    <span data-ttu-id="5bdf7-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5bdf7-116">要從中取出書簽的資料指標。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="5bdf7-117">secondaryKey</span></span>  
    <span data-ttu-id="5bdf7-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="5bdf7-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="5bdf7-119">次要索引鍵的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="5bdf7-120">secondaryKeySize</span></span>  
    <span data-ttu-id="5bdf7-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bdf7-122">次要金鑰緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-123">actualSecondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="5bdf7-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="5bdf7-124">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bdf7-125">傳回次要索引鍵的大小。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="5bdf7-126">primaryKey</span></span>  
    <span data-ttu-id="5bdf7-127">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="5bdf7-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="5bdf7-128">主要索引鍵的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-129">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="5bdf7-129">primaryKeySize</span></span>  
    <span data-ttu-id="5bdf7-130">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bdf7-131">主要金鑰緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-132">actualPrimaryKeySize</span><span class="sxs-lookup"><span data-stu-id="5bdf7-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="5bdf7-133">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bdf7-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bdf7-134">傳回主要索引鍵的大小。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bdf7-135">grbit</span><span class="sxs-lookup"><span data-stu-id="5bdf7-135">grbit</span></span>  
    <span data-ttu-id="5bdf7-136">型別： [GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5bdf7-137">呼叫的選項。</span><span class="sxs-lookup"><span data-stu-id="5bdf7-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bdf7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bdf7-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bdf7-139">參考</span><span class="sxs-lookup"><span data-stu-id="5bdf7-139">Reference</span></span>

[<span data-ttu-id="5bdf7-140">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5bdf7-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5bdf7-141">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5bdf7-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5bdf7-142">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5bdf7-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
