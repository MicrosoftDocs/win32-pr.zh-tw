---
description: 深入瞭解： JET_COLUMNCREATE cbMax 屬性
title: JET_COLUMNCREATE cbMax 屬性
TOCTitle: 'cbMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.cbmax(v=EXCHG.10)
ms:contentKeyID: 55103390
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.set_cbMax
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.get_cbMax
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef30df9fd43bb9aa5b9ecb3eadf2f21ac4a8a4f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194308"
---
# <a name="jet_columncreatecbmax-property"></a><span data-ttu-id="ef046-103">JET_COLUMNCREATE cbMax 屬性</span><span class="sxs-lookup"><span data-stu-id="ef046-103">JET_COLUMNCREATE.cbMax property</span></span>

<span data-ttu-id="ef046-104">取得或設定資料行的最大長度。</span><span class="sxs-lookup"><span data-stu-id="ef046-104">Gets or sets the maximum length of the column.</span></span> <span data-ttu-id="ef046-105">只有 [Text](./jet-coltyp-enumeration.md)、 [LongText](./jet-coltyp-enumeration.md)、 [Binary](./jet-coltyp-enumeration.md) 和 [LongBinary](./jet-coltyp-enumeration.md)類型的資料行才有意義。</span><span class="sxs-lookup"><span data-stu-id="ef046-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md), [LongText](./jet-coltyp-enumeration.md), [Binary](./jet-coltyp-enumeration.md) and [LongBinary](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="ef046-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef046-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef046-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ef046-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef046-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef046-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbMax As Integer
    Get
    Set
'Usage
Dim instance As JET_COLUMNCREATE
Dim value As Integer

value = instance.cbMax

instance.cbMax = value
```

``` csharp
public int cbMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ef046-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ef046-109">Property value</span></span>

<span data-ttu-id="ef046-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ef046-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef046-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef046-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef046-112">參考</span><span class="sxs-lookup"><span data-stu-id="ef046-112">Reference</span></span>

[<span data-ttu-id="ef046-113">JET_COLUMNCREATE 類別</span><span class="sxs-lookup"><span data-stu-id="ef046-113">JET_COLUMNCREATE class</span></span>](./jet-columncreate-class.md)

[<span data-ttu-id="ef046-114">JET_COLUMNCREATE 成員</span><span class="sxs-lookup"><span data-stu-id="ef046-114">JET_COLUMNCREATE members</span></span>](./jet-columncreate-members.md)

[<span data-ttu-id="ef046-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ef046-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
