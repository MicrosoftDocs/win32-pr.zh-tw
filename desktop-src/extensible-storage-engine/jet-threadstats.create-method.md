---
description: 深入瞭解： JET_THREADSTATS。Create 方法
title: 'JET_THREADSTATS。建立方法 (的 < a0/&gt; < a1/&gt;) '
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694303"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="10c44-103">JET_THREADSTATS。Create 方法</span><span class="sxs-lookup"><span data-stu-id="10c44-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="10c44-104">使用指定的值建立新的 [JET_THREADSTATS](./jet-threadstats-structure2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="10c44-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="10c44-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="10c44-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="10c44-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="10c44-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10c44-107">語法</span><span class="sxs-lookup"><span data-stu-id="10c44-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="10c44-108">參數</span><span class="sxs-lookup"><span data-stu-id="10c44-108">Parameters</span></span>

  - <span data-ttu-id="10c44-109">cPageReferenced</span><span class="sxs-lookup"><span data-stu-id="10c44-109">cPageReferenced</span></span>  
    <span data-ttu-id="10c44-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-111">造訪的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="10c44-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-112">cPageRead</span><span class="sxs-lookup"><span data-stu-id="10c44-112">cPageRead</span></span>  
    <span data-ttu-id="10c44-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-114">讀取的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="10c44-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-115">cPagePreread</span><span class="sxs-lookup"><span data-stu-id="10c44-115">cPagePreread</span></span>  
    <span data-ttu-id="10c44-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-117">Preread 的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="10c44-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-118">cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="10c44-118">cPageDirtied</span></span>  
    <span data-ttu-id="10c44-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-120">TNumber 的頁面變動總數。</span><span class="sxs-lookup"><span data-stu-id="10c44-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="10c44-121">cPageRedirtied</span></span>  
    <span data-ttu-id="10c44-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-123">Redirtied 的頁面數目。</span><span class="sxs-lookup"><span data-stu-id="10c44-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-124">cLogRecord</span><span class="sxs-lookup"><span data-stu-id="10c44-124">cLogRecord</span></span>  
    <span data-ttu-id="10c44-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-126">產生的記錄檔記錄數目。</span><span class="sxs-lookup"><span data-stu-id="10c44-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="10c44-127">cbLogRecord</span><span class="sxs-lookup"><span data-stu-id="10c44-127">cbLogRecord</span></span>  
    <span data-ttu-id="10c44-128">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10c44-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10c44-129">寫入的記錄檔記錄位元組數。</span><span class="sxs-lookup"><span data-stu-id="10c44-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="10c44-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="10c44-130">Return value</span></span>

<span data-ttu-id="10c44-131">類型： [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="10c44-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="10c44-132">具有指定值的新 [JET_THREADSTATS](./jet-threadstats-structure2.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="10c44-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="10c44-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c44-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10c44-134">參考</span><span class="sxs-lookup"><span data-stu-id="10c44-134">Reference</span></span>

[<span data-ttu-id="10c44-135">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="10c44-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="10c44-136">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="10c44-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="10c44-137">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="10c44-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
