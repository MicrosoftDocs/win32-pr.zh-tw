---
description: 深入瞭解： JET_RETRIEVECOLUMN itagSequence 屬性
title: JET_RETRIEVECOLUMN itagSequence 屬性
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103882
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f2885d5bf467d282ef97172323a8de44980ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851020"
---
# <a name="jet_retrievecolumnitagsequence-property"></a><span data-ttu-id="44ee3-103">JET_RETRIEVECOLUMN itagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="44ee3-103">JET_RETRIEVECOLUMN.itagSequence property</span></span>

<span data-ttu-id="44ee3-104">取得或設定包含在多值資料行中之值的序號。</span><span class="sxs-lookup"><span data-stu-id="44ee3-104">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="44ee3-105">如果 itagSequence 為0，則會傳回多重值資料行的實例數目，而不是任何資料行資料。</span><span class="sxs-lookup"><span data-stu-id="44ee3-105">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span>

<span data-ttu-id="44ee3-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44ee3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44ee3-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="44ee3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44ee3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44ee3-108">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="44ee3-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="44ee3-109">Property value</span></span>

<span data-ttu-id="44ee3-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="44ee3-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="44ee3-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44ee3-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44ee3-112">參考</span><span class="sxs-lookup"><span data-stu-id="44ee3-112">Reference</span></span>

[<span data-ttu-id="44ee3-113">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="44ee3-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="44ee3-114">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="44ee3-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="44ee3-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="44ee3-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
