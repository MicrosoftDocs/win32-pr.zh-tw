---
description: 深入瞭解： EsentResource 類別
title: EsentResource 類別
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971442"
---
# <a name="esentresource-class"></a><span data-ttu-id="8c892-103">EsentResource 類別</span><span class="sxs-lookup"><span data-stu-id="8c892-103">EsentResource class</span></span>

<span data-ttu-id="8c892-104">這是所有 esent 資源物件的基類。</span><span class="sxs-lookup"><span data-stu-id="8c892-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="8c892-105">此類別的子類別可以配置及釋放非受控資源。</span><span class="sxs-lookup"><span data-stu-id="8c892-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8c892-106">繼承階層</span><span class="sxs-lookup"><span data-stu-id="8c892-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="8c892-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="8c892-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="8c892-108">EsentResource （.）</span><span class="sxs-lookup"><span data-stu-id="8c892-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="8c892-109">Microsoft. Esent。</span><span class="sxs-lookup"><span data-stu-id="8c892-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="8c892-110">Microsoft. Esent. Interop. 資料表</span><span class="sxs-lookup"><span data-stu-id="8c892-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="8c892-111">Microsoft. Esent。</span><span class="sxs-lookup"><span data-stu-id="8c892-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="8c892-112">Microsoft. Esent。</span><span class="sxs-lookup"><span data-stu-id="8c892-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="8c892-113">Windows8. DurableCommitCallback （Microsoft）</span><span class="sxs-lookup"><span data-stu-id="8c892-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="8c892-114">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c892-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c892-115">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8c892-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c892-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c892-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="8c892-117">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="8c892-117">Thread safety</span></span>

<span data-ttu-id="8c892-118">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c892-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8c892-119">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="8c892-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c892-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c892-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c892-121">參考</span><span class="sxs-lookup"><span data-stu-id="8c892-121">Reference</span></span>

[<span data-ttu-id="8c892-122">EsentResource 成員</span><span class="sxs-lookup"><span data-stu-id="8c892-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="8c892-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8c892-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
