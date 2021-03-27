---
title: " (Direct3D 11) 的專用介面"
description: ID3DX11EffectVariable 有許多方法可將介面轉換成您需要的特定介面類別型。
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674247"
---
# <a name="specializing-interfaces-direct3d-11"></a><span data-ttu-id="13c24-103"> (Direct3D 11) 的專用介面</span><span class="sxs-lookup"><span data-stu-id="13c24-103">Specializing Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="13c24-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) 有許多方法可將介面轉換成您需要的特定介面類別型。</span><span class="sxs-lookup"><span data-stu-id="13c24-104">[**ID3DX11EffectVariable**](id3dx11effectvariable.md) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="13c24-105">這些方法的格式為 *AsType* ，並且包含每種效果變數類型的方法 (例如 AsBlend、AsConstantBuffer 等。) </span><span class="sxs-lookup"><span data-stu-id="13c24-105">The methods are of the form *AsType* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="13c24-106">例如，假設您有兩個全域變數的效果：時間和世界轉換。</span><span class="sxs-lookup"><span data-stu-id="13c24-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="13c24-107">以下是取得這些變數的範例：</span><span class="sxs-lookup"><span data-stu-id="13c24-107">Here is an example that gets these variables:</span></span>


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="13c24-108">藉由將介面特製化，您就可以將程式碼縮減為單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="13c24-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="13c24-109">繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 的介面也有這些方法，但其設計目的是要傳回不正確物件;只有來自 **ID3DX11EffectVariable** 的呼叫會傳回有效的物件。</span><span class="sxs-lookup"><span data-stu-id="13c24-109">Interfaces that inherit from [**ID3DX11EffectVariable**](id3dx11effectvariable.md) also have these methods, but they have been designed to return invalid objects; only calls from **ID3DX11EffectVariable** return valid objects.</span></span> <span data-ttu-id="13c24-110">應用程式可以藉由呼叫 [**ID3DX11EffectVariable：： IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件，以查看它是否有效。</span><span class="sxs-lookup"><span data-stu-id="13c24-110">Applications can test the returned object to see if it is valid by calling [**ID3DX11EffectVariable::IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13c24-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="13c24-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13c24-112"> (Direct3D 11) 的效果 </span><span class="sxs-lookup"><span data-stu-id="13c24-112">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




