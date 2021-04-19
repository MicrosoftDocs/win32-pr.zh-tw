---
description: ID3D10EffectVariable 介面有許多方法可將介面轉換成您需要的特定介面類別型。
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: " (Direct3D 10) 的專用介面"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999837"
---
# <a name="specializing-interfaces-direct3d-10"></a><span data-ttu-id="7186f-103"> (Direct3D 10) 的專用介面</span><span class="sxs-lookup"><span data-stu-id="7186f-103">Specializing Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="7186f-104">[**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 有許多方法可將介面轉換成您需要的特定介面類別型。</span><span class="sxs-lookup"><span data-stu-id="7186f-104">[**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) has a number of methods for casting the interface into the particular type of interface you need.</span></span> <span data-ttu-id="7186f-105">方法的形式為 *類型* ，並包含每種效果變數 (的方法，例如 AsBlend、AsConstantBuffer 等。) </span><span class="sxs-lookup"><span data-stu-id="7186f-105">The methods are of the form As *Type* and include a method for each type of effect variable (such as AsBlend, AsConstantBuffer etc..)</span></span>

<span data-ttu-id="7186f-106">例如，假設您有兩個全域變數的效果：時間和世界轉換。</span><span class="sxs-lookup"><span data-stu-id="7186f-106">For example, suppose you have an effect with two global variables: time and a world transform.</span></span>


```
float    g_fTime;
float4x4 g_mWorld;
```



<span data-ttu-id="7186f-107">以下是可取得這些變數的 [SimpleSample10 範例](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) 範例 (：</span><span class="sxs-lookup"><span data-stu-id="7186f-107">Here is an example (from [SimpleSample10 Sample](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) that gets these variables:</span></span>


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



<span data-ttu-id="7186f-108">藉由將介面特製化，您就可以將程式碼縮減為單一呼叫。</span><span class="sxs-lookup"><span data-stu-id="7186f-108">By specializing the interfaces, you could reduce the code to a single call.</span></span>


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



<span data-ttu-id="7186f-109">繼承自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 的介面也有這些方法，但其設計目的是要傳回不正確物件;只有來自 **ID3D10EffectVariable 介面** 的呼叫會傳回有效的物件。</span><span class="sxs-lookup"><span data-stu-id="7186f-109">Interfaces that inherit from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) also have these methods, but they have been designed to return invalid objects; only calls from **ID3D10EffectVariable Interface** return valid objects.</span></span> <span data-ttu-id="7186f-110">應用程式可以藉由呼叫 [**ID3D10EffectVariable：： IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid)來測試傳回的物件，以查看它是否有效。</span><span class="sxs-lookup"><span data-stu-id="7186f-110">Applications can test the returned object to see if it is valid by calling [**ID3D10EffectVariable::IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7186f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="7186f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7186f-112">影響</span><span class="sxs-lookup"><span data-stu-id="7186f-112">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



