---
description: 深入瞭解： GuidColumnValue。 Size 屬性
title: GuidColumnValue. Size 屬性
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.guidcolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55107387
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.GuidColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.GuidColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b973638ac8caa4848ed5ecc65468c363ebd2f866
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996638"
---
# <a name="guidcolumnvaluesize-property"></a><span data-ttu-id="2b9b6-103">GuidColumnValue. Size 屬性</span><span class="sxs-lookup"><span data-stu-id="2b9b6-103">GuidColumnValue.Size property</span></span>

<span data-ttu-id="2b9b6-104">取得資料行中值的大小。</span><span class="sxs-lookup"><span data-stu-id="2b9b6-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="2b9b6-105">這會針對可變大小的資料行傳回0， (即二進位和字串) 。</span><span class="sxs-lookup"><span data-stu-id="2b9b6-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="2b9b6-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b9b6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2b9b6-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2b9b6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b9b6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b9b6-108">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="2b9b6-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="2b9b6-109">Property value</span></span>

<span data-ttu-id="2b9b6-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2b9b6-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b9b6-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b9b6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b9b6-112">參考</span><span class="sxs-lookup"><span data-stu-id="2b9b6-112">Reference</span></span>

[<span data-ttu-id="2b9b6-113">GuidColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="2b9b6-113">GuidColumnValue class</span></span>](./guidcolumnvalue-class.md)

[<span data-ttu-id="2b9b6-114">GuidColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="2b9b6-114">GuidColumnValue members</span></span>](./guidcolumnvalue-members.md)

[<span data-ttu-id="2b9b6-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2b9b6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
