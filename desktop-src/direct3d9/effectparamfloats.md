---
description: 定義效果浮點數。 此範本會取代 EffectFloats 範本。
ms.assetid: 7b41d0dc-209f-4ade-a7ed-aa54f421e520
title: EffectParamFloats
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0954ce7679691920c2e104277d12a48f7a34ddf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025673"
---
# <a name="effectparamfloats"></a>EffectParamFloats

定義效果浮點數。 此範本會取代 [**EffectFloats**](effectfloats.md) 範本。

``` syntax
template EffectParamFloats
{
    < 3014B9A0-62F5-478c-9B86-E4AC9F4E418B >
    STRING ParamName;
    DWORD nFloats;
    array float Floats[nFloats];
} 
```

其中：

-   ParamName：浮點數陣列的名稱。
-   nFloats-陣列中的浮點值數目。
-   \[ \] 浮點數 nFloats-浮點值的陣列。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



