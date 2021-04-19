---
title: 光線承載結構
description: 在 TraceRay 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "106991387"
---
# <a name="ray-payload-structure"></a><span data-ttu-id="ca4db-103">光線承載結構</span><span class="sxs-lookup"><span data-stu-id="ca4db-103">Ray payload structure</span></span> 

<span data-ttu-id="ca4db-104">在 [**TraceRay**](traceray-function.md) 呼叫中提供作為 inout 引數的使用者定義結構，以及可存取光線承載之著色器類型中的 inout 參數，其中包括 [任何命中](any-hit-shader.md)、 [最接近的點擊](closest-hit-shader.md)和 [遺漏](miss-shader.md) 著色器。</span><span class="sxs-lookup"><span data-stu-id="ca4db-104">A user-defined structure that is provided as an inout argument in a [**TraceRay**](traceray-function.md) call, and as an inout parameter in the shader types that may access the ray payload, which include [any hit](any-hit-shader.md), [closest hit](closest-hit-shader.md), and [miss](miss-shader.md) shaders.</span></span> <span data-ttu-id="ca4db-105">存取光線承載的任何著色器都必須使用與原始 **TraceRay** 呼叫所提供的相同結構。</span><span class="sxs-lookup"><span data-stu-id="ca4db-105">Any shaders that access the ray payload must use the same structure as the one provided at the originating **TraceRay** call.</span></span>  <span data-ttu-id="ca4db-106">即使其中一個著色器根本不參考光線承載，仍必須指定相符的裝載做為原始 **TraceRay** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="ca4db-106">Even if one of these shaders doesn’t reference the ray payload at all, it still must specify the matching payload as the originating **TraceRay** call.</span></span>

