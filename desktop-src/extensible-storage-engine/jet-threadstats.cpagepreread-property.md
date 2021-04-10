---
description: 深入瞭解： JET_THREADSTATS cPagePreread 屬性
title: 'JET_THREADSTATS. cPagePreread 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cPagePreread property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagepreread(v=EXCHG.10)
ms:contentKeyID: 39510638
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPagePreread
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPagePreread
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd004407fcc7474435b8b2e12dc7eff9555b0e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194291"
---
# <a name="jet_threadstatscpagepreread-property"></a><span data-ttu-id="f7da6-103">JET_THREADSTATS cPagePreread 屬性</span><span class="sxs-lookup"><span data-stu-id="f7da6-103">JET_THREADSTATS.cPagePreread property</span></span>

<span data-ttu-id="f7da6-104">取得目前線程上的資料庫引擎從磁片預先提取的資料庫頁面總數。</span><span class="sxs-lookup"><span data-stu-id="f7da6-104">Gets the total number of database pages prefetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="f7da6-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="f7da6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f7da6-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f7da6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7da6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7da6-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPagePreread As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPagePreread
```

``` csharp
public int cPagePreread { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="f7da6-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="f7da6-108">Property value</span></span>

<span data-ttu-id="f7da6-109">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7da6-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7da6-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7da6-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7da6-111">參考</span><span class="sxs-lookup"><span data-stu-id="f7da6-111">Reference</span></span>

[<span data-ttu-id="f7da6-112">JET_THREADSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="f7da6-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="f7da6-113">JET_THREADSTATS 成員</span><span class="sxs-lookup"><span data-stu-id="f7da6-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="f7da6-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="f7da6-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
