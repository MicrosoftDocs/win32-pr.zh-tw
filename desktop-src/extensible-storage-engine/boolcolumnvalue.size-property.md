---
description: 深入瞭解： BoolColumnValue。 Size 屬性
title: BoolColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55100904
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.BoolColumnValue.Size
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95458e02780b1a0a96c46c857dc168be3125a816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992182"
---
# <a name="boolcolumnvaluesize-property"></a><span data-ttu-id="a20f5-103">BoolColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="a20f5-103">BoolColumnValue.Size property</span></span>

<span data-ttu-id="a20f5-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="a20f5-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="a20f5-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="a20f5-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="a20f5-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a20f5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a20f5-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a20f5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a20f5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a20f5-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="a20f5-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="a20f5-109">Property value</span></span>

<span data-ttu-id="a20f5-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a20f5-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a20f5-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a20f5-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a20f5-112">參考</span><span class="sxs-lookup"><span data-stu-id="a20f5-112">Reference</span></span>

[<span data-ttu-id="a20f5-113">BoolColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="a20f5-113">BoolColumnValue class</span></span>](./boolcolumnvalue-class.md)

[<span data-ttu-id="a20f5-114">BoolColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="a20f5-114">BoolColumnValue members</span></span>](./boolcolumnvalue-members.md)

[<span data-ttu-id="a20f5-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a20f5-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
