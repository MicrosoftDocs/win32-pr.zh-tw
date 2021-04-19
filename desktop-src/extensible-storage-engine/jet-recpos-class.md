---
description: 深入瞭解： JET_RECPOS 類別
title: JET_RECPOS 類別
TOCTitle: JET_RECPOS class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_RECPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos(v=EXCHG.10)
ms:contentKeyID: 55103839
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09fce4bf1d73ad1b9767e39ae5c90b25eccdea73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975556"
---
# <a name="jet_recpos-class"></a><span data-ttu-id="e28d9-103">JET_RECPOS 類別</span><span class="sxs-lookup"><span data-stu-id="e28d9-103">JET_RECPOS class</span></span>

<span data-ttu-id="e28d9-104">表示索引內的小數位置。</span><span class="sxs-lookup"><span data-stu-id="e28d9-104">Represents a fractional position within an index.</span></span> <span data-ttu-id="e28d9-105">這是由 JetGotoPosition 和 JetGetRecordPosition 所使用。</span><span class="sxs-lookup"><span data-stu-id="e28d9-105">This is used by JetGotoPosition and JetGetRecordPosition.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e28d9-106">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e28d9-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="e28d9-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="e28d9-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="e28d9-108">Microsoft.Isam.Esent.Interop.JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="e28d9-108">Microsoft.Isam.Esent.Interop.JET_RECPOS</span></span>  

<span data-ttu-id="e28d9-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e28d9-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e28d9-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e28d9-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e28d9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e28d9-111">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_RECPOS _
    Implements IContentEquatable(Of JET_RECPOS), IDeepCloneable(Of JET_RECPOS)
'Usage
Dim instance As JET_RECPOS
```

``` csharp
[SerializableAttribute]
public sealed class JET_RECPOS : IContentEquatable<JET_RECPOS>, 
    IDeepCloneable<JET_RECPOS>
```

## <a name="thread-safety"></a><span data-ttu-id="e28d9-112">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e28d9-112">Thread safety</span></span>

<span data-ttu-id="e28d9-113">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e28d9-113">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e28d9-114">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e28d9-114">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e28d9-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e28d9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e28d9-116">參考</span><span class="sxs-lookup"><span data-stu-id="e28d9-116">Reference</span></span>

[<span data-ttu-id="e28d9-117">JET_RECPOS 成員</span><span class="sxs-lookup"><span data-stu-id="e28d9-117">JET_RECPOS members</span></span>](./jet-recpos-members.md)

[<span data-ttu-id="e28d9-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e28d9-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
