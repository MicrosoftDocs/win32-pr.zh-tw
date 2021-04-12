---
description: 包裝紋理位址模式（由 \_ D3DTEXTUREADDRESS 列舉型別的 D3DTADDRESS wrap 成員識別）讓 Direct3D 在每個整數連接點上重複紋理。
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: '將材質位址模式換行 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187407"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>將材質位址模式換行 (Direct3D 9) 

包裝紋理位址模式（由 \_ [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) 列舉型別的 D3DTADDRESS wrap 成員識別）讓 Direct3D 在每個整數連接點上重複紋理。 例如：假設您的應用程式建立了一個正方形的原始物件，並且指定其四個頂點座標分別為 (0.0, 0.0)、(0.0, 3.0)、(3.0, 3.0)，及 (3.0, 0.0)。 將材質定址模式設定為 D3DTADDRESS，會在 \_ 兩個方向中，將材質套用三次，如下圖所示。

![在 u 及 v 方向覆蓋臉部紋理之圖例](images/wrap.png)

此材質位址模式的效果與鏡像模式的效果類似，但不同。 如需詳細資訊，請參閱 [ (Direct3D 9) 的鏡像材質位址模式 ](mirror-texture-address-mode.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質定址模式](texture-addressing-modes.md)
</dt> </dl>

 

 
