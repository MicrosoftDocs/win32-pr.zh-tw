---
description: 深入瞭解： JET_THREADSTATS cPageRedirtied 屬性
title: 'JET_THREADSTATS. cPageRedirtied 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cPageRedirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageredirtied(v=EXCHG.10)
ms:contentKeyID: 39515312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRedirtied
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0ed97a93958ba52231439dc6c2125db982296ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985484"
---
# <a name="jet_threadstatscpageredirtied-property"></a><span data-ttu-id="55d9c-103">JET_THREADSTATS cPageRedirtied 屬性</span><span class="sxs-lookup"><span data-stu-id="55d9c-103">JET_THREADSTATS.cPageRedirtied property</span></span>

<span data-ttu-id="55d9c-104">取得目前線程上的資料庫引擎已修改的資料庫頁面總數（具有不成文變更）。</span><span class="sxs-lookup"><span data-stu-id="55d9c-104">Gets the total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="55d9c-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="55d9c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="55d9c-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="55d9c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55d9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="55d9c-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageRedirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRedirtied
```

``` csharp
public int cPageRedirtied { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="55d9c-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="55d9c-108">Property value</span></span>

<span data-ttu-id="55d9c-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55d9c-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="55d9c-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55d9c-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55d9c-111">參考</span><span class="sxs-lookup"><span data-stu-id="55d9c-111">Reference</span></span>

[<span data-ttu-id="55d9c-112">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="55d9c-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="55d9c-113">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="55d9c-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="55d9c-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="55d9c-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
