---
description: 深入瞭解： SystemParameters. StartFlushThreshold 屬性
title: SystemParameters. StartFlushThreshold 屬性
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320164"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="edfba-103">SystemParameters. StartFlushThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="edfba-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="edfba-104">取得或設定資料庫頁面快取開始從快取收回頁面的閾值，以騰出空間給未快取的頁面。</span><span class="sxs-lookup"><span data-stu-id="edfba-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="edfba-105">當快取中的頁面緩衝區數目降到低於此閾值時，就會啟動背景進程來補充該可用緩衝區集區。</span><span class="sxs-lookup"><span data-stu-id="edfba-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="edfba-106">此臨界值一律相對於 JET_paramCacheSizeMax 所設定的最大快取大小。</span><span class="sxs-lookup"><span data-stu-id="edfba-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="edfba-107">此臨界值也必須小於 JET_paramStopFlushThreshold 所設定的停止閾值。</span><span class="sxs-lookup"><span data-stu-id="edfba-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="edfba-108">開始閾值的距離高度將決定資料庫頁面快取在應用程式需要之前產生可用緩衝區所必須擁有的回應時間。</span><span class="sxs-lookup"><span data-stu-id="edfba-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="edfba-109">高啟動臨界值可讓背景進程更有時間回應。</span><span class="sxs-lookup"><span data-stu-id="edfba-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="edfba-110">不過，高啟動閾值表示較高的停止閾值，而且會減少資料庫頁面快取的有效大小。</span><span class="sxs-lookup"><span data-stu-id="edfba-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="edfba-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="edfba-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="edfba-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="edfba-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="edfba-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="edfba-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="edfba-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="edfba-114">Property value</span></span>

<span data-ttu-id="edfba-115">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="edfba-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="edfba-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edfba-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="edfba-117">參考</span><span class="sxs-lookup"><span data-stu-id="edfba-117">Reference</span></span>

[<span data-ttu-id="edfba-118">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="edfba-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="edfba-119">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="edfba-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="edfba-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="edfba-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
