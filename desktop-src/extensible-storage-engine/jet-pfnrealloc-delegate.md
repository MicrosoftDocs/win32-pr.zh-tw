---
description: 深入瞭解： JET_PFNREALLOC 委派
title: JET_PFNREALLOC 委派
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945361"
---
# <a name="jet_pfnrealloc-delegate"></a><span data-ttu-id="0eee7-103">JET_PFNREALLOC 委派</span><span class="sxs-lookup"><span data-stu-id="0eee7-103">JET_PFNREALLOC delegate</span></span>

<span data-ttu-id="0eee7-104">JetEnumerateColumns 用來為其輸出緩衝區配置記憶體的回呼。</span><span class="sxs-lookup"><span data-stu-id="0eee7-104">Callback used by JetEnumerateColumns to allocate memory for its output buffers.</span></span>

<span data-ttu-id="0eee7-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="0eee7-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="0eee7-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0eee7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0eee7-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0eee7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0eee7-108">語法</span><span class="sxs-lookup"><span data-stu-id="0eee7-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a><span data-ttu-id="0eee7-109">參數</span><span class="sxs-lookup"><span data-stu-id="0eee7-109">Parameters</span></span>

  - <span data-ttu-id="0eee7-110">內容</span><span class="sxs-lookup"><span data-stu-id="0eee7-110">context</span></span>  
    <span data-ttu-id="0eee7-111">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="0eee7-111">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="0eee7-112">提供給 JetEnumerateColumns 的內容。</span><span class="sxs-lookup"><span data-stu-id="0eee7-112">Context given to JetEnumerateColumns.</span></span>

<!-- end list -->

  - <span data-ttu-id="0eee7-113">記憶體</span><span class="sxs-lookup"><span data-stu-id="0eee7-113">memory</span></span>  
    <span data-ttu-id="0eee7-114">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="0eee7-114">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="0eee7-115">如果非零，則為此回呼先前配置之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="0eee7-115">If non-zero, a pointer to a memory block previously allocated by this callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="0eee7-116">requestedSize</span><span class="sxs-lookup"><span data-stu-id="0eee7-116">requestedSize</span></span>  
    <span data-ttu-id="0eee7-117">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="0eee7-117">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="0eee7-118">記憶體區塊的新大小 (以位元組為單位) 。</span><span class="sxs-lookup"><span data-stu-id="0eee7-118">The new size of the memory block (in bytes).</span></span> <span data-ttu-id="0eee7-119">如果這是0，而且指定了記憶體區塊，就會釋放該記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="0eee7-119">If this is 0 and a memory block is specified, that memory block will be freed.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0eee7-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0eee7-120">Return value</span></span>

<span data-ttu-id="0eee7-121">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="0eee7-121">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
<span data-ttu-id="0eee7-122">新配置之記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="0eee7-122">A pointer to newly allocated memory.</span></span> <span data-ttu-id="0eee7-123">如果無法配置記憶體，則應該傳回 [零](/dotnet/api/system.intptr.zero) 。</span><span class="sxs-lookup"><span data-stu-id="0eee7-123">If memory could not be allocated then [Zero](/dotnet/api/system.intptr.zero) should be returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0eee7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0eee7-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0eee7-125">參考</span><span class="sxs-lookup"><span data-stu-id="0eee7-125">Reference</span></span>

[<span data-ttu-id="0eee7-126">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0eee7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
