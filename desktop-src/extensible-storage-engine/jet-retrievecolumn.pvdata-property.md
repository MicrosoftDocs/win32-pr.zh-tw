---
description: 深入瞭解： JET_RETRIEVECOLUMN pvData 屬性
title: JET_RETRIEVECOLUMN pvData 屬性
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0809073dd956cf8166463450160d46761eb86fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511944"
---
# <a name="jet_retrievecolumnpvdata-property"></a><span data-ttu-id="e6a30-103">JET_RETRIEVECOLUMN pvData 屬性</span><span class="sxs-lookup"><span data-stu-id="e6a30-103">JET_RETRIEVECOLUMN.pvData property</span></span>

<span data-ttu-id="e6a30-104">取得或設定將儲存從資料行取出之資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6a30-104">Gets or sets the buffer that will store data that is retrieved from the column.</span></span>

<span data-ttu-id="e6a30-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6a30-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6a30-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e6a30-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a30-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6a30-107">Syntax</span></span>

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e6a30-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="e6a30-108">Property value</span></span>

<span data-ttu-id="e6a30-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="e6a30-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6a30-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6a30-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6a30-111">參考</span><span class="sxs-lookup"><span data-stu-id="e6a30-111">Reference</span></span>

[<span data-ttu-id="e6a30-112">JET_RETRIEVECOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="e6a30-112">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="e6a30-113">JET_RETRIEVECOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="e6a30-113">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="e6a30-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e6a30-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
