---
description: 深入瞭解： JET_ENUMCOLUMN cbData 屬性
title: JET_ENUMCOLUMN cbData 屬性
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b38d6c8433cc9792ebdd7e04e72027c6e1477e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112965"
---
# <a name="jet_enumcolumncbdata-property"></a><span data-ttu-id="f1a7c-103">JET_ENUMCOLUMN cbData 屬性</span><span class="sxs-lookup"><span data-stu-id="f1a7c-103">JET_ENUMCOLUMN.cbData property</span></span>

<span data-ttu-id="f1a7c-104">取得為數據行列舉之值的大小。</span><span class="sxs-lookup"><span data-stu-id="f1a7c-104">Gets the size of the value that was enumerated for the column.</span></span> <span data-ttu-id="f1a7c-105">只有當 [err](./jet-enumcolumn.err-property.md) 等於 [ColumnSingleValue](./jet-wrn-enumeration.md)時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="f1a7c-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is equal to [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span>

<span data-ttu-id="f1a7c-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f1a7c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f1a7c-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f1a7c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1a7c-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cbData
```

``` csharp
public int cbData { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f1a7c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f1a7c-109">Property value</span></span>

<span data-ttu-id="f1a7c-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f1a7c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f1a7c-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1a7c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1a7c-112">參考</span><span class="sxs-lookup"><span data-stu-id="f1a7c-112">Reference</span></span>

[<span data-ttu-id="f1a7c-113">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="f1a7c-113">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="f1a7c-114">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="f1a7c-114">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="f1a7c-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f1a7c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
