---
description: 深入瞭解： SystemParameters. StopFlushThreshold 屬性
title: SystemParameters. StopFlushThreshold 屬性
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320163"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="7e5a7-103">SystemParameters. StopFlushThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="7e5a7-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="7e5a7-104">取得或設定資料庫頁面快取結束從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="7e5a7-105">當快取中的頁面緩衝區數目超過此臨界值時，就會停止已開始補充該可用緩衝區集區的背景進程。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="7e5a7-106">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="7e5a7-107">此臨界值也必須大於 JET_paramStartFlushThreshold 所設定的 [開始] 閾值。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="7e5a7-108">開始閾值和停止臨界值之間的距離，會影響背景進程清除資料庫頁面的效率。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="7e5a7-109">較大的間距將可讓您更有可能合併對相鄰頁面的寫入。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="7e5a7-110">不過，高停止閾值將會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="7e5a7-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a7-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e5a7-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7e5a7-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5a7-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e5a7-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7e5a7-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="7e5a7-114">Property value</span></span>

<span data-ttu-id="7e5a7-115">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7e5a7-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e5a7-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e5a7-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e5a7-117">參考</span><span class="sxs-lookup"><span data-stu-id="7e5a7-117">Reference</span></span>

[<span data-ttu-id="7e5a7-118">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="7e5a7-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="7e5a7-119">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="7e5a7-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="7e5a7-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7e5a7-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
