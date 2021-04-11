---
description: 深入瞭解： JET_CONDITIONALCOLUMN 類別
title: JET_CONDITIONALCOLUMN 類別
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944703"
---
# <a name="jet_conditionalcolumn-class"></a><span data-ttu-id="e2625-103">JET_CONDITIONALCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="e2625-103">JET_CONDITIONALCOLUMN class</span></span>

<span data-ttu-id="e2625-104">定義如何針對指定的索引執行條件式索引編制。</span><span class="sxs-lookup"><span data-stu-id="e2625-104">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="e2625-105">條件式索引僅包含符合指定條件之資料列的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="e2625-105">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="e2625-106">不過，條件資料行不是索引索引鍵的一部分，而只會控制索引項目是否存在。</span><span class="sxs-lookup"><span data-stu-id="e2625-106">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e2625-107">繼承階層</span><span class="sxs-lookup"><span data-stu-id="e2625-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="e2625-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="e2625-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="e2625-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e2625-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span></span>  

<span data-ttu-id="e2625-110">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2625-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2625-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e2625-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2625-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2625-112">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a><span data-ttu-id="e2625-113">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="e2625-113">Thread safety</span></span>

<span data-ttu-id="e2625-114">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e2625-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e2625-115">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="e2625-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2625-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2625-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2625-117">參考</span><span class="sxs-lookup"><span data-stu-id="e2625-117">Reference</span></span>

[<span data-ttu-id="e2625-118">JET_CONDITIONALCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="e2625-118">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="e2625-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e2625-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
