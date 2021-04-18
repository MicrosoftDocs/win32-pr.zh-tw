---
description: 深入瞭解： ColumnValue。 Length 屬性
title: ColumnValue. Length 屬性
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976369"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="67cc0-103">ColumnValue. Length 屬性</span><span class="sxs-lookup"><span data-stu-id="67cc0-103">ColumnValue.Length property</span></span>

<span data-ttu-id="67cc0-104">取得資料行值的位元組長度，如果資料行是 null，則為零，否則會符合固定大小資料行的大小，並代表變數大小資料行的實際值位元組長度， (也就是二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="67cc0-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="67cc0-105">若為字串，就會以假設每個字元的兩個位元組來決定長度。</span><span class="sxs-lookup"><span data-stu-id="67cc0-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="67cc0-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="67cc0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="67cc0-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="67cc0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="67cc0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67cc0-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="67cc0-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="67cc0-109">Property value</span></span>

<span data-ttu-id="67cc0-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="67cc0-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="67cc0-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67cc0-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67cc0-112">參考</span><span class="sxs-lookup"><span data-stu-id="67cc0-112">Reference</span></span>

[<span data-ttu-id="67cc0-113">ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="67cc0-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="67cc0-114">ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="67cc0-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="67cc0-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="67cc0-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
