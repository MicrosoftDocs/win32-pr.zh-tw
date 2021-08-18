---
description: 定義可套用至完整網格或網格個別臉部的基本材質色彩。 功率是材質的反射指數。
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798965"
---
# <a name="material"></a>Material

定義可套用至完整網格或網格個別臉部的基本材質色彩。 功率是材質的反射指數。

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

其中：

-   faceColor-臉部色彩。 ColorRGBA 範本。 請參閱 [**ColorRGBA**](colorrgba.md)。
-   電源材質反射色彩指數。
-   specularColor-材質反射色彩。 ColorRGB 範本。 請參閱 [**ColorRGB**](colorrgb.md)。
-   emissiveColor-材質放射色彩。 ColorRGB 範本。 請參閱 [**ColorRGB**](colorrgb.md)。

> [!Note]  
> 環境色彩需要 Alpha 元件。

 

[**TextureFilename**](texturefilename.md) 是選擇性的資料物件。 如果這個物件不存在，就會 uNtextured 臉部。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



