---
title: RaytracingAccelerationStructure
description: 可以在 HLSL 中宣告並傳遞至 TraceRay 的資源類型，以表示使用 BuildRaytracingAccelerationStructure 建立的最上層加速資源。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106986433"
---
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="eec2d-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="eec2d-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="eec2d-104">可以在 HLSL 中宣告並傳遞至 [**TraceRay**](traceray-function.md) 的資源類型，以表示使用 **BuildRaytracingAccelerationStructure** 建立的最上層加速資源。</span><span class="sxs-lookup"><span data-stu-id="eec2d-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="eec2d-105">它會系結為描述中繼資料表或根描述項 SRV 中的原始緩衝區 SRV。</span><span class="sxs-lookup"><span data-stu-id="eec2d-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="eec2d-106">HLSL 中的宣告如下所示：</span><span class="sxs-lookup"><span data-stu-id="eec2d-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="eec2d-107">此範例顯示加速結構的無限制大小陣列，這表示來自描述元堆積，因為無法編制根目錄描述元的索引。</span><span class="sxs-lookup"><span data-stu-id="eec2d-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="eec2d-108">**RaytracingAccelerationStructure** 是不透明的資源，沒有任何可供著色器使用的方法。</span><span class="sxs-lookup"><span data-stu-id="eec2d-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




