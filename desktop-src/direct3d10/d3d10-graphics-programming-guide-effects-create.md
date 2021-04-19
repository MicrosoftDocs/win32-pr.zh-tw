---
description: 效果是藉由將它載入效果架構來建立。
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: " (Direct3D 10 建立效果) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984149"
---
# <a name="create-an-effect-direct3d-10"></a> (Direct3D 10 建立效果) 

效果是藉由將它載入效果架構來建立。 如果從未編譯過此效果，則會在建立時進行編譯。 您可以藉由呼叫 [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)來建立已載入記憶體的效果。 下列程式碼範例會使用 [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) 來建立檔案的效果。


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



讀取效果需要與編譯效果相同的參數，以及裝置和集區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯 (Direct3D 10) 的效果 ](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



