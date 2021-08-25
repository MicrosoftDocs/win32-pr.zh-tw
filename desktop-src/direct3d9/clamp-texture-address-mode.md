---
description: 由 D3DTEXTUREADDRESS 列舉型別之 D3DTADDRESS 的夾具成員所識別的夾具材質位址模式， \_ 會導致 Direct3D 將您的材質座標帶到 \[ 0.0 1.0 的 \] 範圍。
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: " (Direct3D 9) 的夾具材質位址模式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751351"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a> (Direct3D 9) 的夾具材質位址模式

由 D3DTEXTUREADDRESS 列舉型別之 D3DTADDRESS 的夾具成員所識別的夾具材質位址模式， \_ 會導致 Direct3D 將您的材質座標帶到[](./d3dtextureaddress.md) \[ 0.0 1.0 的 \] 範圍。 也就是說，它會套用紋理一次，然後 smears 邊緣圖元的色彩。 例如，假設您的應用程式會建立一個平方根，並將 (0.0、0.0) 、 (0.0、3.0) 、 (3.0、3.0) 和 (3.0、0.0) 的材質座標指派給基本頂點。 將材質定址模式設定為 D3DTADDRESS \_ 的夾具會導致紋理套用一次。 在欄頂端及列末端的像素色彩會分別延伸至原始物件的頂端及右端。

以下圖例為一個鉗位紋理。

![紋理及鉗位紋理的圖例](images/clamp.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質定址模式](texture-addressing-modes.md)
</dt> </dl>

 

 
