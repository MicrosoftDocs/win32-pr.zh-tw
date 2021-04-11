---
description: 深入瞭解： JET_SETINFO itagSequence 屬性
title: JET_SETINFO itagSequence 屬性
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETINFO.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c409903f90633f15daa8d289c72530db943f1c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112525"
---
# <a name="jet_setinfoitagsequence-property"></a><span data-ttu-id="e044c-103">JET_SETINFO itagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="e044c-103">JET_SETINFO.itagSequence property</span></span>

<span data-ttu-id="e044c-104">取得或設定要設定之多重值資料行中的值順序。</span><span class="sxs-lookup"><span data-stu-id="e044c-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="e044c-105">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="e044c-105">The array of values is one-based.</span></span> <span data-ttu-id="e044c-106">第一個值是 sequence 1，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="e044c-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="e044c-107">如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。</span><span class="sxs-lookup"><span data-stu-id="e044c-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="e044c-108">值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="e044c-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="e044c-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e044c-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e044c-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e044c-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e044c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e044c-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e044c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e044c-112">Property value</span></span>

<span data-ttu-id="e044c-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e044c-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e044c-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e044c-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e044c-115">參考</span><span class="sxs-lookup"><span data-stu-id="e044c-115">Reference</span></span>

[<span data-ttu-id="e044c-116">JET_SETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="e044c-116">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="e044c-117">JET_SETINFO 成員</span><span class="sxs-lookup"><span data-stu-id="e044c-117">JET_SETINFO members</span></span>](./jet-setinfo-members.md)

[<span data-ttu-id="e044c-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e044c-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
