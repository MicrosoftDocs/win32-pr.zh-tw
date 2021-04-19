---
description: 深入瞭解： JET_ERRINFOBASIC rgCategoricalHierarchy 屬性
title: RgCategoricalHierarchy 屬性 (Windows8) 的 JET_ERRINFOBASIC。
TOCTitle: 'rgCategoricalHierarchy property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.rgcategoricalhierarchy(v=EXCHG.10)
ms:contentKeyID: 55104314
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37034ca35427c9470d69f5e90dd43a4640601574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974308"
---
# <a name="jet_errinfobasicrgcategoricalhierarchy-property"></a><span data-ttu-id="d11a8-103">JET_ERRINFOBASIC rgCategoricalHierarchy 屬性</span><span class="sxs-lookup"><span data-stu-id="d11a8-103">JET_ERRINFOBASIC.rgCategoricalHierarchy property</span></span>

<span data-ttu-id="d11a8-104">取得或設定錯誤的階層。</span><span class="sxs-lookup"><span data-stu-id="d11a8-104">Gets or sets the hierarchy of errors.</span></span> <span data-ttu-id="d11a8-105">位置0是階層中最高的層級，而其餘的則是 JET_errcatUnknown。</span><span class="sxs-lookup"><span data-stu-id="d11a8-105">Position 0 is the highest level in the hierarchy, and the rest are JET_errcatUnknown.</span></span>

<span data-ttu-id="d11a8-106">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d11a8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d11a8-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d11a8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d11a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d11a8-108">Syntax</span></span>

``` vb
'Declaration
Public Property rgCategoricalHierarchy As JET_ERRCAT()
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_ERRCAT()

value = instance.rgCategoricalHierarchy

instance.rgCategoricalHierarchy = value
```

``` csharp
public JET_ERRCAT[] rgCategoricalHierarchy { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d11a8-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d11a8-109">Property value</span></span>

<span data-ttu-id="d11a8-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="d11a8-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="d11a8-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d11a8-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d11a8-112">參考</span><span class="sxs-lookup"><span data-stu-id="d11a8-112">Reference</span></span>

[<span data-ttu-id="d11a8-113">JET_ERRINFOBASIC 類別</span><span class="sxs-lookup"><span data-stu-id="d11a8-113">JET_ERRINFOBASIC class</span></span>](./jet-errinfobasic-class.md)

[<span data-ttu-id="d11a8-114">JET_ERRINFOBASIC 成員</span><span class="sxs-lookup"><span data-stu-id="d11a8-114">JET_ERRINFOBASIC members</span></span>](./jet-errinfobasic-members.md)

[<span data-ttu-id="d11a8-115">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="d11a8-115">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
