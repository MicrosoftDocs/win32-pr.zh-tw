---
title: " (Direct3D 11) 的專用介面"
description: ID3DX11EffectVariable 有許多方法可將介面轉換成您需要的特定介面類別型。
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126072"
---
# <a name="specializing-interfaces-direct3d-11"></a> (Direct3D 11) 的專用介面

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) 有許多方法可將介面轉換成您需要的特定介面類別型。 這些方法的格式為 *AsType* ，並且包含每種效果變數類型的方法 (例如 AsBlend、AsConstantBuffer 等。) 

例如，假設您有兩個全域變數的效果：時間和世界轉換。


```
float    g_fTime;
float4x4 g_mWorld;
```



以下是取得這些變數的範例：


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



藉由將介面特製化，您就可以將程式碼縮減為單一呼叫。


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md) 的介面也有這些方法，但其設計目的是要傳回不正確物件;只有來自 **ID3DX11EffectVariable** 的呼叫會傳回有效的物件。 應用程式可以藉由呼叫 [**ID3DX11EffectVariable：： IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件，以查看它是否有效。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 11) 的效果 ](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




