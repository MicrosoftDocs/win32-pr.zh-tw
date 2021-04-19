---
description: 深入瞭解： JET_COLUMNDEF cbMax 屬性
title: JET_COLUMNDEF cbMax 屬性
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103491
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cbMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 486507dc046617ea6689fcf1c5eac4199cfeecd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974167"
---
# <a name="jet_columndefcbmax-property"></a><span data-ttu-id="8cac6-103">JET_COLUMNDEF cbMax 屬性</span><span class="sxs-lookup"><span data-stu-id="8cac6-103">JET_COLUMNDEF.cbMax property</span></span>

<span data-ttu-id="8cac6-104">取得或設定資料行的最大長度。</span><span class="sxs-lookup"><span data-stu-id="8cac6-104">Gets or sets the maximum length of the column.</span></span> <span data-ttu-id="8cac6-105">只有 [Text](./jet-coltyp-enumeration.md)、 [LongText](./jet-coltyp-enumeration.md)、 [Binary](./jet-coltyp-enumeration.md) 和 [LongBinary](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="8cac6-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="8cac6-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8cac6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8cac6-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8cac6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8cac6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cac6-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8cac6-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="8cac6-109">Property value</span></span>

<span data-ttu-id="8cac6-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8cac6-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8cac6-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cac6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cac6-112">參考</span><span class="sxs-lookup"><span data-stu-id="8cac6-112">Reference</span></span>

[<span data-ttu-id="8cac6-113">JET_COLUMNDEF 類別</span><span class="sxs-lookup"><span data-stu-id="8cac6-113">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="8cac6-114">JET_COLUMNDEF 成員</span><span class="sxs-lookup"><span data-stu-id="8cac6-114">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="8cac6-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8cac6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
