---
description: 深入瞭解： JET_ENUMCOLUMN pvData 屬性
title: JET_ENUMCOLUMN pvData 屬性
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469032"
---
# <a name="jet_enumcolumnpvdata-property"></a><span data-ttu-id="a6864-103">JET_ENUMCOLUMN pvData 屬性</span><span class="sxs-lookup"><span data-stu-id="a6864-103">JET_ENUMCOLUMN.pvData property</span></span>

<span data-ttu-id="a6864-104">取得為數據行列舉的值。</span><span class="sxs-lookup"><span data-stu-id="a6864-104">Gets the value that was enumerated for the column.</span></span> <span data-ttu-id="a6864-105">只有當 [err](./jet-enumcolumn.err-property.md) 等於 [ColumnSingleValue](./jet-wrn-enumeration.md)時，才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="a6864-105">This member is only used if [err](./jet-enumcolumn.err-property.md) is equal to [ColumnSingleValue](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="a6864-106">這會指向傳遞給[JetEnumerateColumns (JET_SESID、JET_TABLEID、Int32、 \[ \] 、int32、 \[ \] 、JET_PFNREALLOC、IntPtr、int32、EnumerateColumnsGrbit) ](./api.jetenumeratecolumns-method.md)的[JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)配置器回呼所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="a6864-106">This points to memory allocated with the [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) allocator callback passed to [JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md).</span></span> <span data-ttu-id="a6864-107">請記得在完成時釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="a6864-107">Remember to release the memory when finished.</span></span>

<span data-ttu-id="a6864-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6864-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a6864-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a6864-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6864-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6864-110">Syntax</span></span>

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="a6864-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="a6864-111">Property value</span></span>

<span data-ttu-id="a6864-112">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="a6864-112">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a6864-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6864-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6864-114">參考</span><span class="sxs-lookup"><span data-stu-id="a6864-114">Reference</span></span>

[<span data-ttu-id="a6864-115">JET_ENUMCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="a6864-115">JET_ENUMCOLUMN class</span></span>](./jet-enumcolumn-class.md)

[<span data-ttu-id="a6864-116">JET_ENUMCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="a6864-116">JET_ENUMCOLUMN members</span></span>](./jet-enumcolumn-members.md)

[<span data-ttu-id="a6864-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a6864-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
