---
description: 深入瞭解： ColumnValue. ValueAsObject 屬性
title: ColumnValue. ValueAsObject 屬性
TOCTitle: 'ValueAsObject property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.valueasobject(v=EXCHG.10)
ms:contentKeyID: 55101198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.get_ValueAsObject
- Microsoft.Isam.Esent.Interop.ColumnValue.ValueAsObject
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1cc7d96f9b8584e81da5cfa66073b19989b0a476
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974330"
---
# <a name="columnvaluevalueasobject-property"></a><span data-ttu-id="77995-103">ColumnValue. ValueAsObject 屬性</span><span class="sxs-lookup"><span data-stu-id="77995-103">ColumnValue.ValueAsObject property</span></span>

<span data-ttu-id="77995-104">取得資料行的最後一個設定或抓取值。</span><span class="sxs-lookup"><span data-stu-id="77995-104">Gets the last set or retrieved value of the column.</span></span> <span data-ttu-id="77995-105">此值會以泛型物件的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="77995-105">The value is returned as a generic object.</span></span>

<span data-ttu-id="77995-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="77995-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="77995-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="77995-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="77995-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="77995-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property ValueAsObject As Object
    Get
'Usage
Dim instance As ColumnValue
Dim value As Object

value = instance.ValueAsObject
```

``` csharp
public abstract Object ValueAsObject { get; }
```

#### <a name="property-value"></a><span data-ttu-id="77995-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="77995-109">Property value</span></span>

<span data-ttu-id="77995-110">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="77995-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  

## <a name="see-also"></a><span data-ttu-id="77995-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77995-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="77995-112">參考</span><span class="sxs-lookup"><span data-stu-id="77995-112">Reference</span></span>

[<span data-ttu-id="77995-113">ColumnValue 類別</span><span class="sxs-lookup"><span data-stu-id="77995-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="77995-114">ColumnValue 成員</span><span class="sxs-lookup"><span data-stu-id="77995-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="77995-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="77995-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
