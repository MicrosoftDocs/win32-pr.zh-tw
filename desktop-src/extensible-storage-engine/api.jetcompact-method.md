---
description: 深入瞭解： JetCompact 方法
title: JetCompact 方法
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943306"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="5d884-103">JetCompact 方法</span><span class="sxs-lookup"><span data-stu-id="5d884-103">Api.JetCompact method</span></span>

<span data-ttu-id="5d884-104">建立現有資料庫的複本。</span><span class="sxs-lookup"><span data-stu-id="5d884-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="5d884-105">複本會壓縮為使用狀態的最佳狀態。</span><span class="sxs-lookup"><span data-stu-id="5d884-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="5d884-106">複製的資料中的資料將會根據在索引建立時為索引選擇的量值進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="5d884-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="5d884-107">如此一來，壓縮的資料可能會盡可能儲存為密集。</span><span class="sxs-lookup"><span data-stu-id="5d884-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="5d884-108">或者，壓縮的資料可能會保留空間，以便後續記錄成長或插入索引。</span><span class="sxs-lookup"><span data-stu-id="5d884-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="5d884-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d884-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d884-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5d884-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d884-111">語法</span><span class="sxs-lookup"><span data-stu-id="5d884-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5d884-112">參數</span><span class="sxs-lookup"><span data-stu-id="5d884-112">Parameters</span></span>

  - <span data-ttu-id="5d884-113">sesid</span><span class="sxs-lookup"><span data-stu-id="5d884-113">sesid</span></span>  
    <span data-ttu-id="5d884-114">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5d884-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5d884-115">要用於呼叫的會話。</span><span class="sxs-lookup"><span data-stu-id="5d884-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d884-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="5d884-116">sourceDatabase</span></span>  
    <span data-ttu-id="5d884-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5d884-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5d884-118">將壓縮的源資料庫。</span><span class="sxs-lookup"><span data-stu-id="5d884-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d884-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="5d884-119">destinationDatabase</span></span>  
    <span data-ttu-id="5d884-120">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5d884-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5d884-121">要用於壓縮資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d884-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d884-122">statusCallback</span><span class="sxs-lookup"><span data-stu-id="5d884-122">statusCallback</span></span>  
    <span data-ttu-id="5d884-123">類型： [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="5d884-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="5d884-124">可透過資料庫 compact 作業定期呼叫以報告進度的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="5d884-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d884-125">忽略</span><span class="sxs-lookup"><span data-stu-id="5d884-125">ignored</span></span>  
    <span data-ttu-id="5d884-126">類型： [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="5d884-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="5d884-127">此參數會被忽略，而且應該是 null。</span><span class="sxs-lookup"><span data-stu-id="5d884-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="5d884-128">grbit</span><span class="sxs-lookup"><span data-stu-id="5d884-128">grbit</span></span>  
    <span data-ttu-id="5d884-129">型別： [CompactGrbit](./compactgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d884-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5d884-130">壓縮選項。</span><span class="sxs-lookup"><span data-stu-id="5d884-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d884-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d884-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d884-132">參考</span><span class="sxs-lookup"><span data-stu-id="5d884-132">Reference</span></span>

[<span data-ttu-id="5d884-133">Api 類別</span><span class="sxs-lookup"><span data-stu-id="5d884-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5d884-134">Api 成員</span><span class="sxs-lookup"><span data-stu-id="5d884-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5d884-135">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5d884-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
