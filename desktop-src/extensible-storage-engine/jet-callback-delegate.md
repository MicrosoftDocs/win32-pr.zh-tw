---
description: 深入瞭解： JET_CALLBACK 委派
title: JET_CALLBACK 委派
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989983"
---
# <a name="jet_callback-delegate"></a><span data-ttu-id="7b29f-103">JET_CALLBACK 委派</span><span class="sxs-lookup"><span data-stu-id="7b29f-103">JET_CALLBACK delegate</span></span>

<span data-ttu-id="7b29f-104">資料庫引擎使用的多用途回呼函式，用來通知應用程式涉及線上磁碟重組和資料指標狀態通知。</span><span class="sxs-lookup"><span data-stu-id="7b29f-104">A multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="7b29f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7b29f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7b29f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b29f-107">語法</span><span class="sxs-lookup"><span data-stu-id="7b29f-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a><span data-ttu-id="7b29f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7b29f-108">Parameters</span></span>

  - <span data-ttu-id="7b29f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7b29f-109">sesid</span></span>  
    <span data-ttu-id="7b29f-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7b29f-111">正在進行回呼的會話。</span><span class="sxs-lookup"><span data-stu-id="7b29f-111">The session for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="7b29f-112">dbid</span></span>  
    <span data-ttu-id="7b29f-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="7b29f-114">正在進行回呼的資料庫。</span><span class="sxs-lookup"><span data-stu-id="7b29f-114">The database for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-115">tableid</span><span class="sxs-lookup"><span data-stu-id="7b29f-115">tableid</span></span>  
    <span data-ttu-id="7b29f-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7b29f-117">正在進行回呼的資料指標。</span><span class="sxs-lookup"><span data-stu-id="7b29f-117">The cursor for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-118">cbtyp</span><span class="sxs-lookup"><span data-stu-id="7b29f-118">cbtyp</span></span>  
    <span data-ttu-id="7b29f-119">類型： [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-119">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="7b29f-120">正在進行回呼的作業。</span><span class="sxs-lookup"><span data-stu-id="7b29f-120">The operation for which the callback is being made.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-121">arg1</span><span class="sxs-lookup"><span data-stu-id="7b29f-121">arg1</span></span>  
    <span data-ttu-id="7b29f-122">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="7b29f-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="7b29f-123">第一個回呼特定的引數。</span><span class="sxs-lookup"><span data-stu-id="7b29f-123">First callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-124">arg2</span><span class="sxs-lookup"><span data-stu-id="7b29f-124">arg2</span></span>  
    <span data-ttu-id="7b29f-125">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="7b29f-125">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="7b29f-126">第二個回呼特定的引數。</span><span class="sxs-lookup"><span data-stu-id="7b29f-126">Second callback-specific argument.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-127">內容</span><span class="sxs-lookup"><span data-stu-id="7b29f-127">context</span></span>  
    <span data-ttu-id="7b29f-128">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="7b29f-128">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="7b29f-129">回呼內容。</span><span class="sxs-lookup"><span data-stu-id="7b29f-129">Callback context.</span></span>

<!-- end list -->

  - <span data-ttu-id="7b29f-130">unused</span><span class="sxs-lookup"><span data-stu-id="7b29f-130">unused</span></span>  
    <span data-ttu-id="7b29f-131">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="7b29f-131">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="7b29f-132">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="7b29f-132">This parameter is not used.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7b29f-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b29f-133">Return value</span></span>

<span data-ttu-id="7b29f-134">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7b29f-134">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7b29f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b29f-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b29f-136">參考</span><span class="sxs-lookup"><span data-stu-id="7b29f-136">Reference</span></span>

[<span data-ttu-id="7b29f-137">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7b29f-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
