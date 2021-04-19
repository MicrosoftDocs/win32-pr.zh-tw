---
description: 深入瞭解： JET_THREADSTATS 結構
title: 'JET_THREADSTATS 結構 (的結構) '
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972809"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="823c1-103">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="823c1-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="823c1-104">包含目前線程上資料庫引擎所執行之工作的累計統計資料。</span><span class="sxs-lookup"><span data-stu-id="823c1-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="823c1-105">這項資訊會透過 JetGetThreadStats 傳回。</span><span class="sxs-lookup"><span data-stu-id="823c1-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="823c1-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="823c1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="823c1-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="823c1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="823c1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="823c1-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="823c1-109">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="823c1-109">Thread safety</span></span>

<span data-ttu-id="823c1-110">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="823c1-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="823c1-111">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="823c1-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="823c1-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="823c1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="823c1-113">參考</span><span class="sxs-lookup"><span data-stu-id="823c1-113">Reference</span></span>

[<span data-ttu-id="823c1-114">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="823c1-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="823c1-115">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="823c1-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
