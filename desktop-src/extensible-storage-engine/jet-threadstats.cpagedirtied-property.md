---
description: 深入瞭解： JET_THREADSTATS cPageDirtied 屬性
title: 'JET_THREADSTATS. cPageDirtied 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cPageDirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagedirtied(v=EXCHG.10)
ms:contentKeyID: 39512428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageDirtied
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d1f628ce821a6e35c231ccf4b469b5b1c1ff60c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510927"
---
# <a name="jet_threadstatscpagedirtied-property"></a><span data-ttu-id="b0741-103">JET_THREADSTATS cPageDirtied 屬性</span><span class="sxs-lookup"><span data-stu-id="b0741-103">JET_THREADSTATS.cPageDirtied property</span></span>

<span data-ttu-id="b0741-104">取得目前線程上的資料庫引擎已修改的資料庫頁面總數（沒有不成文變更）。</span><span class="sxs-lookup"><span data-stu-id="b0741-104">Gets the total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="b0741-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="b0741-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b0741-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b0741-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0741-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0741-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageDirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageDirtied
```

``` csharp
public int cPageDirtied { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="b0741-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="b0741-108">Property value</span></span>

<span data-ttu-id="b0741-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b0741-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0741-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0741-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0741-111">參考</span><span class="sxs-lookup"><span data-stu-id="b0741-111">Reference</span></span>

[<span data-ttu-id="b0741-112">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="b0741-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="b0741-113">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="b0741-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="b0741-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="b0741-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
