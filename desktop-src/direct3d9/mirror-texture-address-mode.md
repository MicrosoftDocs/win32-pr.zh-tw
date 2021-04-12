---
description: 鏡像材質位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS 鏡像成員所識別）會導致 Direct3D 鏡像每個整數界限的材質。
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: " (Direct3D 9) 的鏡像材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385663"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a> (Direct3D 9) 的鏡像材質位址模式

鏡像材質位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS 鏡像成員所識別）會導致 Direct3D 鏡像每個整數界限的材質。 例如：假設您的應用程式建立了一個正方形的原始物件，並且指定其四個頂點座標分別為 (0.0, 0.0)、(0.0, 3.0)、(3.0, 3.0)，及 (3.0, 0.0)。 將材質定址模式設定為 D3DTADDRESS \_ 鏡像會導致紋理在 u 和 v 方向套用三次。 每一欄與每一列套用的紋理，都是前一欄或前一列紋理的鏡映影像，如下圖例所示。

![3x3 格線中鏡映影像的圖例](images/mirror.png)

此材質位址模式的效果類似于換行模式的結果，但不同于。 如需詳細資訊，請參閱 [Wrap (Direct3D 9) 的材質位址模式 ](wrap-texture-address-mode.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質定址模式](texture-addressing-modes.md)
</dt> </dl>

 

 
