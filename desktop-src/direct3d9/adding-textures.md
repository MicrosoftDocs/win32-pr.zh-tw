---
description: 若要加入材質，請使用檔案格式的階層式本質，並將選擇性的 TextureFilename 資料物件加入至材質資料物件。
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: '將材質新增 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b60ea80702ffc339fe753dec3ad9b72170b03bc8f23598e545e17bc71209d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045236"
---
# <a name="adding-textures-direct3d-9"></a>將材質新增 (Direct3D 9) 

若要加入材質，請使用檔案格式的階層式本質，並將選擇性的 [**TextureFilename**](texturefilename.md) 資料物件加入至 [**材質**](material.md) 資料物件。 **材質** 物件現在如下所示：


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[X 檔案 (舊版) ](x-files--legacy-.md)
</dt> </dl>

 

 



