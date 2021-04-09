---
description: 深入瞭解： EsentStopwatch 類別
title: EsentStopwatch 類別
TOCTitle: EsentStopwatch class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStopwatch
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch(v=EXCHG.10)
ms:contentKeyID: 55102933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1250b10763aca6155ef7ac12bc64adbb95ac77a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851967"
---
# <a name="esentstopwatch-class"></a><span data-ttu-id="ec040-103">EsentStopwatch 類別</span><span class="sxs-lookup"><span data-stu-id="ec040-103">EsentStopwatch class</span></span>

<span data-ttu-id="ec040-104">提供一組方法和屬性，您可以使用這些方法和屬性來測量執行緒的 ESENT 工作統計資料。</span><span class="sxs-lookup"><span data-stu-id="ec040-104">Provides a set of methods and properties that you can use to measure ESENT work statistics for a thread.</span></span> <span data-ttu-id="ec040-105">如果最新版本的 ESENT 不支援 [JetGetThreadStats (JET_THREADSTATS) ](./vistaapi.jetgetthreadstats-method.md) 那麼所有 ESENT 統計資料都會是0。</span><span class="sxs-lookup"><span data-stu-id="ec040-105">If the current version of ESENT doesn't support [JetGetThreadStats(JET_THREADSTATS)](./vistaapi.jetgetthreadstats-method.md) then all ESENT statistics will be 0.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ec040-106">繼承階層</span><span class="sxs-lookup"><span data-stu-id="ec040-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="ec040-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="ec040-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="ec040-108">EsentStopwatch （.）</span><span class="sxs-lookup"><span data-stu-id="ec040-108">Microsoft.Isam.Esent.Interop.EsentStopwatch</span></span>  

<span data-ttu-id="ec040-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec040-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec040-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ec040-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec040-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec040-111">Syntax</span></span>

``` vb
'Declaration
Public Class EsentStopwatch
'Usage
Dim instance As EsentStopwatch
```

``` csharp
public class EsentStopwatch
```

## <a name="thread-safety"></a><span data-ttu-id="ec040-112">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="ec040-112">Thread safety</span></span>

<span data-ttu-id="ec040-113">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec040-113">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ec040-114">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="ec040-114">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec040-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec040-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec040-116">參考</span><span class="sxs-lookup"><span data-stu-id="ec040-116">Reference</span></span>

[<span data-ttu-id="ec040-117">EsentStopwatch 成員</span><span class="sxs-lookup"><span data-stu-id="ec040-117">EsentStopwatch members</span></span>](./esentstopwatch-members.md)

[<span data-ttu-id="ec040-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ec040-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
