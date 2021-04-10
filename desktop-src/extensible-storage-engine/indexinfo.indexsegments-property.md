---
description: 深入瞭解： IndexInfo. IndexSegments 屬性
title: IndexInfo. IndexSegments 屬性
TOCTitle: 'IndexSegments property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexinfo.indexsegments(v=EXCHG.10)
ms:contentKeyID: 55103239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IndexInfo.IndexSegments
- Microsoft.Isam.Esent.Interop.IndexInfo.get_IndexSegments
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d366d3ddd5ba7a33faeb44459830dbaadcc221e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691352"
---
# <a name="indexinfoindexsegments-property"></a><span data-ttu-id="db24c-103">IndexInfo. IndexSegments 屬性</span><span class="sxs-lookup"><span data-stu-id="db24c-103">IndexInfo.IndexSegments property</span></span>

<span data-ttu-id="db24c-104">取得索引的區段。</span><span class="sxs-lookup"><span data-stu-id="db24c-104">Gets the segments of the index.</span></span>

<span data-ttu-id="db24c-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db24c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db24c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="db24c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db24c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="db24c-107">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property IndexSegments As IList(Of IndexSegment)
    Get
'Usage
Dim instance As IndexInfo
Dim value As IList(Of IndexSegment)

value = instance.IndexSegments
```

``` csharp
public IList<IndexSegment> IndexSegments { get; }
```

#### <a name="property-value"></a><span data-ttu-id="db24c-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="db24c-108">Property value</span></span>

<span data-ttu-id="db24c-109">類型： [system.object](/dotnet/api/system.collections.generic.ilist-1) 。\<[IndexSegment](./indexsegment-class.md)\></span><span class="sxs-lookup"><span data-stu-id="db24c-109">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[IndexSegment](./indexsegment-class.md)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="db24c-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db24c-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db24c-111">參考</span><span class="sxs-lookup"><span data-stu-id="db24c-111">Reference</span></span>

[<span data-ttu-id="db24c-112">IndexInfo 類別</span><span class="sxs-lookup"><span data-stu-id="db24c-112">IndexInfo class</span></span>](./indexinfo-class.md)

[<span data-ttu-id="db24c-113">IndexInfo 成員</span><span class="sxs-lookup"><span data-stu-id="db24c-113">IndexInfo members</span></span>](./indexinfo-members.md)

[<span data-ttu-id="db24c-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="db24c-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
