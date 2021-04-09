---
description: 深入瞭解： JET_ENUMCOLUMNID rgtagSequence 屬性
title: JET_ENUMCOLUMNID rgtagSequence 屬性
TOCTitle: 'rgtagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.rgtagsequence(v=EXCHG.10)
ms:contentKeyID: 55103529
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_rgtagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.rgtagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d61d69fb9f22a31f07ee2eb0b4116a13761d961
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689607"
---
# <a name="jet_enumcolumnidrgtagsequence-property"></a><span data-ttu-id="10ecb-103">JET_ENUMCOLUMNID rgtagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="10ecb-103">JET_ENUMCOLUMNID.rgtagSequence property</span></span>

<span data-ttu-id="10ecb-104">取得或設定指定資料行的資料行值陣列中，以一個為基底的索引陣列。</span><span class="sxs-lookup"><span data-stu-id="10ecb-104">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="10ecb-105">單一元素是 JET_RETRIEVECOLUMN 中定義的 itagSequence。</span><span class="sxs-lookup"><span data-stu-id="10ecb-105">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="10ecb-106">ItagSequence 0 (零) 表示「略過」。</span><span class="sxs-lookup"><span data-stu-id="10ecb-106">An itagSequence of 0 (zero) means "skip".</span></span> <span data-ttu-id="10ecb-107">1的 itagSequence 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。</span><span class="sxs-lookup"><span data-stu-id="10ecb-107">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

<span data-ttu-id="10ecb-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10ecb-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10ecb-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="10ecb-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10ecb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="10ecb-110">Syntax</span></span>

``` vb
'Declaration
Public Property rgtagSequence As Integer()
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer()

value = instance.rgtagSequence

instance.rgtagSequence = value
```

``` csharp
public int[] rgtagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="10ecb-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="10ecb-111">Property value</span></span>

<span data-ttu-id="10ecb-112">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="10ecb-112">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="10ecb-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10ecb-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10ecb-114">參考</span><span class="sxs-lookup"><span data-stu-id="10ecb-114">Reference</span></span>

[<span data-ttu-id="10ecb-115">JET_ENUMCOLUMNID 類別</span><span class="sxs-lookup"><span data-stu-id="10ecb-115">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="10ecb-116">JET_ENUMCOLUMNID 成員</span><span class="sxs-lookup"><span data-stu-id="10ecb-116">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="10ecb-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="10ecb-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
