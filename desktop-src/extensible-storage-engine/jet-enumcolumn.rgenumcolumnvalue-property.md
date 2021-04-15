---
description: 深入瞭解： JET_ENUMCOLUMN rgEnumColumnValue 屬性
title: JET_ENUMCOLUMN rgEnumColumnValue 屬性
TOCTitle: 'rgEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.rgenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103505
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.rgEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_rgEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d0e131723ae9fb8e1f68193c96d5ed2671a74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510939"
---
# <a name="jet_enumcolumnrgenumcolumnvalue-property"></a><span data-ttu-id="aabc7-103">JET_ENUMCOLUMN rgEnumColumnValue 屬性</span><span class="sxs-lookup"><span data-stu-id="aabc7-103">JET_ENUMCOLUMN.rgEnumColumnValue property</span></span>

<span data-ttu-id="aabc7-104">取得資料行的列舉資料行值。</span><span class="sxs-lookup"><span data-stu-id="aabc7-104">Gets the enumerated column values for the column.</span></span> <span data-ttu-id="aabc7-105">只有在未[ColumnSingleValue](./jet-wrn-enumeration.md) [err](./jet-enumcolumn.err-property.md)時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="aabc7-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is not [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="aabc7-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aabc7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aabc7-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="aabc7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aabc7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aabc7-108">Syntax</span></span>

``` vb
'Declaration
Public Property rgEnumColumnValue As JET_ENUMCOLUMNVALUE()
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As JET_ENUMCOLUMNVALUE()

value = instance.rgEnumColumnValue
```

``` csharp
public JET_ENUMCOLUMNVALUE[] rgEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="aabc7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="aabc7-109">Property value</span></span>

<span data-ttu-id="aabc7-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="aabc7-110">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="aabc7-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aabc7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aabc7-112">參考</span><span class="sxs-lookup"><span data-stu-id="aabc7-112">Reference</span></span>

[<span data-ttu-id="aabc7-113">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="aabc7-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="aabc7-114">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="aabc7-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="aabc7-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="aabc7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
