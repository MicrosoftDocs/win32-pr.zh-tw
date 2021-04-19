---
description: 深入瞭解： UInt32ColumnValue。 Size 屬性
title: UInt32ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint32columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104179
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.UInt32ColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c80fd3afb34c73d5d054a11f57c42af52be776ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978996"
---
# <a name="uint32columnvaluesize-property"></a><span data-ttu-id="05874-103">UInt32ColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="05874-103">UInt32ColumnValue.Size property</span></span>

<span data-ttu-id="05874-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="05874-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="05874-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="05874-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="05874-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="05874-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="05874-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="05874-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="05874-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="05874-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="05874-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="05874-109">Property value</span></span>

<span data-ttu-id="05874-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="05874-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="05874-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05874-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="05874-112">參考</span><span class="sxs-lookup"><span data-stu-id="05874-112">Reference</span></span>

[<span data-ttu-id="05874-113">UInt32ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="05874-113">UInt32ColumnValue class</span></span>](./uint32columnvalue-class.md)

[<span data-ttu-id="05874-114">UInt32ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="05874-114">UInt32ColumnValue members</span></span>](./uint32columnvalue-members.md)

[<span data-ttu-id="05874-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="05874-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
