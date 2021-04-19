---
description: 深入瞭解： JetGotoSecondaryIndexBookmark 方法
title: JetGotoSecondaryIndexBookmark 方法
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980058"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="61d02-103">JetGotoSecondaryIndexBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="61d02-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="61d02-104">將游標放置在與指定次要索引書簽相關聯的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="61d02-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="61d02-105">次要索引書簽必須與原始抓取的相同資料表上的相同索引一起使用。</span><span class="sxs-lookup"><span data-stu-id="61d02-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="61d02-106">您可以使用 JetGotoSecondaryIndexBookmark (JET_SESID、JET_TABLEID、 \[ \] 、int32、 \[ \] 、int32、GotoSecondaryIndexBookmarkGrbit) ，來抓取索引項目的次要索引書簽。</span><span class="sxs-lookup"><span data-stu-id="61d02-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="61d02-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61d02-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61d02-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="61d02-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61d02-109">語法</span><span class="sxs-lookup"><span data-stu-id="61d02-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="61d02-110">參數</span><span class="sxs-lookup"><span data-stu-id="61d02-110">Parameters</span></span>

  - <span data-ttu-id="61d02-111">sesid</span><span class="sxs-lookup"><span data-stu-id="61d02-111">sesid</span></span>  
    <span data-ttu-id="61d02-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61d02-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="61d02-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="61d02-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-114">tableid</span><span class="sxs-lookup"><span data-stu-id="61d02-114">tableid</span></span>  
    <span data-ttu-id="61d02-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61d02-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="61d02-116">要放置的資料表資料指標。</span><span class="sxs-lookup"><span data-stu-id="61d02-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="61d02-117">secondaryKey</span></span>  
    <span data-ttu-id="61d02-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="61d02-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="61d02-119">包含次要索引鍵的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="61d02-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="61d02-120">secondaryKeySize</span></span>  
    <span data-ttu-id="61d02-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61d02-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61d02-122">次要索引鍵的大小。</span><span class="sxs-lookup"><span data-stu-id="61d02-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="61d02-123">primaryKey</span></span>  
    <span data-ttu-id="61d02-124">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="61d02-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="61d02-125">包含主要索引鍵的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="61d02-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-126">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="61d02-126">primaryKeySize</span></span>  
    <span data-ttu-id="61d02-127">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61d02-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61d02-128">主要索引鍵的大小。</span><span class="sxs-lookup"><span data-stu-id="61d02-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="61d02-129">grbit</span><span class="sxs-lookup"><span data-stu-id="61d02-129">grbit</span></span>  
    <span data-ttu-id="61d02-130">型別： [GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="61d02-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="61d02-131">用於定位書簽的選項。</span><span class="sxs-lookup"><span data-stu-id="61d02-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="61d02-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61d02-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61d02-133">參考</span><span class="sxs-lookup"><span data-stu-id="61d02-133">Reference</span></span>

[<span data-ttu-id="61d02-134">Api 類別</span><span class="sxs-lookup"><span data-stu-id="61d02-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="61d02-135">Api 成員</span><span class="sxs-lookup"><span data-stu-id="61d02-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="61d02-136">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="61d02-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
