---
description: 深入瞭解： JET_ENUMCOLUMN cEnumColumnValue 屬性
title: JET_ENUMCOLUMN cEnumColumnValue 屬性
TOCTitle: 'cEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103498
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee9649f7c546dee155dfcda35ece32dfe346c689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689615"
---
# <a name="jet_enumcolumncenumcolumnvalue-property"></a><span data-ttu-id="17362-103">JET_ENUMCOLUMN cEnumColumnValue 屬性</span><span class="sxs-lookup"><span data-stu-id="17362-103">JET_ENUMCOLUMN.cEnumColumnValue property</span></span>

<span data-ttu-id="17362-104">取得針對資料行列舉的資料行值數目。</span><span class="sxs-lookup"><span data-stu-id="17362-104">Gets the number of column values enumerated for the column.</span></span> <span data-ttu-id="17362-105">只有在未[ColumnSingleValue](./jet-wrn-enumeration.md) [err](./jet-enumcolumn.err-property.md)時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="17362-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is not [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="17362-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17362-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="17362-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="17362-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17362-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17362-108">Syntax</span></span>

``` vb
'Declaration
Public Property cEnumColumnValue As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cEnumColumnValue
```

``` csharp
public int cEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="17362-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="17362-109">Property value</span></span>

<span data-ttu-id="17362-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="17362-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="17362-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17362-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17362-112">參考</span><span class="sxs-lookup"><span data-stu-id="17362-112">Reference</span></span>

[<span data-ttu-id="17362-113">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="17362-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="17362-114">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="17362-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="17362-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="17362-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
