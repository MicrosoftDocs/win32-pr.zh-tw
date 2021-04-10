---
description: 深入瞭解： JET_COLUMNBASE cbMax 屬性
title: JET_COLUMNBASE cbMax 屬性
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103464
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d539df352119d24e1c8ddf7df816b8715f659417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027506"
---
# <a name="jet_columnbasecbmax-property"></a><span data-ttu-id="9567f-103">JET_COLUMNBASE cbMax 屬性</span><span class="sxs-lookup"><span data-stu-id="9567f-103">JET_COLUMNBASE.cbMax property</span></span>

<span data-ttu-id="9567f-104">取得資料行的最大長度。</span><span class="sxs-lookup"><span data-stu-id="9567f-104">Gets the maximum length of the column.</span></span> <span data-ttu-id="9567f-105">只有 [Text](./jet-coltyp-enumeration.md)、 [LongText](./jet-coltyp-enumeration.md)、 [Binary](./jet-coltyp-enumeration.md) 和 [LongBinary](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="9567f-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="9567f-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9567f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9567f-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9567f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9567f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9567f-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As Integer

value = instance.cbMax
```

``` csharp
public int cbMax { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="9567f-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9567f-109">Property value</span></span>

<span data-ttu-id="9567f-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9567f-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9567f-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9567f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9567f-112">參考</span><span class="sxs-lookup"><span data-stu-id="9567f-112">Reference</span></span>

[<span data-ttu-id="9567f-113">JET_COLUMNBASE 類別</span><span class="sxs-lookup"><span data-stu-id="9567f-113">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="9567f-114">JET_COLUMNBASE 成員</span><span class="sxs-lookup"><span data-stu-id="9567f-114">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="9567f-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9567f-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
