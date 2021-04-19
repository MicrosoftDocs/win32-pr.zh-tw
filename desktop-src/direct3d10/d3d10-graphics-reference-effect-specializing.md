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
# <a name="specializing-interfaces-direct3d-10"></a> (Direct3D 10) 的專用介面

[**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 有許多方法可將介面轉換成您需要的特定介面類別型。 方法的形式為 *類型* ，並包含每種效果變數 (的方法，例如 AsBlend、AsConstantBuffer 等。) 

例如，假設您有兩個全域變數的效果：時間和世界轉換。


```
float    g_fTime;
float4x4 g_mWorld;
```



以下是可取得這些變數的 [SimpleSample10 範例](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) 範例 (：


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



藉由將介面特製化，您就可以將程式碼縮減為單一呼叫。


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



繼承自 [**ID3D10EffectVariable 介面**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) 的介面也有這些方法，但其設計目的是要傳回不正確物件;只有來自 **ID3D10EffectVariable 介面** 的呼叫會傳回有效的物件。 應用程式可以藉由呼叫 [**ID3D10EffectVariable：： IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid)來測試傳回的物件，以查看它是否有效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影響](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



