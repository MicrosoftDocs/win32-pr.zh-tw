---
description: 深入瞭解： JET_SPACEHINTS ulGrowth 屬性
title: JET_SPACEHINTS ulGrowth 屬性
TOCTitle: 'ulGrowth property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.ulgrowth(v=EXCHG.10)
ms:contentKeyID: 55103929
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.set_ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.get_ulGrowth
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 946975a1777778871ecb8ae66c8e567e7c2ffcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689559"
---
# <a name="jet_spacehintsulgrowth-property"></a><span data-ttu-id="1b247-103">JET_SPACEHINTS ulGrowth 屬性</span><span class="sxs-lookup"><span data-stu-id="1b247-103">JET_SPACEHINTS.ulGrowth property</span></span>

<span data-ttu-id="1b247-104">取得或設定上一次成長或初始大小 (可能四捨五入為最接近原生 JET 配置大小) 的成長百分比。</span><span class="sxs-lookup"><span data-stu-id="1b247-104">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="1b247-105">有效的值為0，而 \[ 100 50000) 。</span><span class="sxs-lookup"><span data-stu-id="1b247-105">Valid values are 0, and \[100, 50000).</span></span>

<span data-ttu-id="1b247-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b247-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1b247-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1b247-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b247-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b247-108">Syntax</span></span>

``` vb
'Declaration
Public Property ulGrowth As Integer
    Get
    Set
'Usage
Dim instance As JET_SPACEHINTS
Dim value As Integer

value = instance.ulGrowth

instance.ulGrowth = value
```

``` csharp
public int ulGrowth { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1b247-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1b247-109">Property value</span></span>

<span data-ttu-id="1b247-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1b247-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b247-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b247-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b247-112">參考</span><span class="sxs-lookup"><span data-stu-id="1b247-112">Reference</span></span>

[<span data-ttu-id="1b247-113">JET_SPACEHINTS 類別</span><span class="sxs-lookup"><span data-stu-id="1b247-113">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="1b247-114">JET_SPACEHINTS 成員</span><span class="sxs-lookup"><span data-stu-id="1b247-114">JET_SPACEHINTS members</span></span>](./jet-spacehints-members.md)

[<span data-ttu-id="1b247-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1b247-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
