---
description: 深入瞭解： ColumnValue。 Size 屬性
title: ColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101207
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.ColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20893eba6516b53045463ce664cdb77ae7e9b768
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026348"
---
# <a name="columnvaluesize-property"></a><span data-ttu-id="416db-103">ColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="416db-103">ColumnValue.Size property</span></span>

<span data-ttu-id="416db-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="416db-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="416db-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="416db-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="416db-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="416db-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="416db-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="416db-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="416db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="416db-108">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected abstract int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="416db-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="416db-109">Property value</span></span>

<span data-ttu-id="416db-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="416db-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="416db-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="416db-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="416db-112">參考</span><span class="sxs-lookup"><span data-stu-id="416db-112">Reference</span></span>

[<span data-ttu-id="416db-113">ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="416db-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="416db-114">ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="416db-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="416db-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="416db-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
