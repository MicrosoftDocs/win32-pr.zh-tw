---
description: 效果是藉由將它載入效果架構來建立。
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: " (Direct3D 10 建立效果) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75014688c62e6f8f0463c430b0b17aafd28e0ad3764d00b8a357a6613565d87d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567058"
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

 

 



