---
description: 深入瞭解： UInt64ColumnValue。 Size 屬性
title: UInt64ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.uint64columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55104194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.Size
- Microsoft.Isam.Esent.Interop.UInt64ColumnValue.get_Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8102b08ce8a48bb23a3618fe5829c354f200ff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849530"
---
# <a name="uint64columnvaluesize-property"></a><span data-ttu-id="0d0ec-103">UInt64ColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="0d0ec-103">UInt64ColumnValue.Size property</span></span>

<span data-ttu-id="0d0ec-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="0d0ec-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="0d0ec-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="0d0ec-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="0d0ec-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d0ec-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d0ec-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0d0ec-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0ec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d0ec-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="0d0ec-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="0d0ec-109">Property value</span></span>

<span data-ttu-id="0d0ec-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0d0ec-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d0ec-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d0ec-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d0ec-112">參考</span><span class="sxs-lookup"><span data-stu-id="0d0ec-112">Reference</span></span>

[<span data-ttu-id="0d0ec-113">UInt64ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="0d0ec-113">UInt64ColumnValue class</span></span>](./uint64columnvalue-class.md)

[<span data-ttu-id="0d0ec-114">UInt64ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="0d0ec-114">UInt64ColumnValue members</span></span>](./uint64columnvalue-members.md)

[<span data-ttu-id="0d0ec-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0d0ec-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
