---
description: 深入瞭解： JET_SETCOLUMN itagSequence 屬性
title: JET_SETCOLUMN itagSequence 屬性
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7870f6e29cf8f6810c6aa41049868fbceb370dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997484"
---
# <a name="jet_setcolumnitagsequence-property"></a><span data-ttu-id="7ba1e-103">JET_SETCOLUMN itagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="7ba1e-103">JET_SETCOLUMN.itagSequence property</span></span>

<span data-ttu-id="7ba1e-104">取得或設定要設定之多重值資料行中的值順序。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-104">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="7ba1e-105">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-105">The array of values is one-based.</span></span> <span data-ttu-id="7ba1e-106">第一個值是 sequence 1，而不是 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-106">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="7ba1e-107">如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 itagSequence 傳遞。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-107">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="7ba1e-108">值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-108">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="7ba1e-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7ba1e-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7ba1e-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7ba1e-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba1e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba1e-111">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7ba1e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7ba1e-112">Property value</span></span>

<span data-ttu-id="7ba1e-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7ba1e-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7ba1e-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ba1e-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7ba1e-115">參考</span><span class="sxs-lookup"><span data-stu-id="7ba1e-115">Reference</span></span>

[<span data-ttu-id="7ba1e-116">JET_SETCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="7ba1e-116">JET_SETCOLUMN class</span></span>](./jet-setcolumn-class.md)

[<span data-ttu-id="7ba1e-117">JET_SETCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="7ba1e-117">JET_SETCOLUMN members</span></span>](./jet-setcolumn-members.md)

[<span data-ttu-id="7ba1e-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7ba1e-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
