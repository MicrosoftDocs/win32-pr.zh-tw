---
description: 深入瞭解： Int32ColumnValue。 Size 屬性
title: Int32ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55103332
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.Size
- Microsoft.Isam.Esent.Interop.Int32ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10710a8705dfaf63959c1287cae7195841a2f039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318664"
---
# <a name="int32columnvaluesize-property"></a><span data-ttu-id="f208c-103">Int32ColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="f208c-103">Int32ColumnValue.Size property</span></span>

<span data-ttu-id="f208c-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="f208c-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="f208c-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="f208c-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="f208c-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f208c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f208c-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f208c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f208c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f208c-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="f208c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f208c-109">Property value</span></span>

<span data-ttu-id="f208c-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f208c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f208c-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f208c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f208c-112">參考</span><span class="sxs-lookup"><span data-stu-id="f208c-112">Reference</span></span>

[<span data-ttu-id="f208c-113">Int32ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="f208c-113">Int32ColumnValue class</span></span>](./int32columnvalue-class.md)

[<span data-ttu-id="f208c-114">Int32ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="f208c-114">Int32ColumnValue members</span></span>](./int32columnvalue-members.md)

[<span data-ttu-id="f208c-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f208c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
