---
description: 深入瞭解： JET_THREADSTATS cPageReferenced 屬性
title: 'JET_THREADSTATS. cPageReferenced 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cPageReferenced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageReferenced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagereferenced(v=EXCHG.10)
ms:contentKeyID: 39510184
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageReferenced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageReferenced
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageReferenced
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageReferenced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beead7c667adc1a4b34ec425d0c2aee7de3aeab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984661"
---
# <a name="jet_threadstatscpagereferenced-property"></a><span data-ttu-id="0cb49-103">JET_THREADSTATS cPageReferenced 屬性</span><span class="sxs-lookup"><span data-stu-id="0cb49-103">JET_THREADSTATS.cPageReferenced property</span></span>

<span data-ttu-id="0cb49-104">取得目前線程上資料庫引擎所造訪的資料庫頁面總數。</span><span class="sxs-lookup"><span data-stu-id="0cb49-104">Gets the total number of database pages visited by the database engine on the current thread.</span></span>

<span data-ttu-id="0cb49-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="0cb49-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0cb49-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0cb49-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb49-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cb49-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageReferenced As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageReferenced
```

``` csharp
public int cPageReferenced { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="0cb49-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="0cb49-108">Property value</span></span>

<span data-ttu-id="0cb49-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0cb49-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0cb49-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cb49-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0cb49-111">參考</span><span class="sxs-lookup"><span data-stu-id="0cb49-111">Reference</span></span>

[<span data-ttu-id="0cb49-112">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="0cb49-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="0cb49-113">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="0cb49-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="0cb49-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="0cb49-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
