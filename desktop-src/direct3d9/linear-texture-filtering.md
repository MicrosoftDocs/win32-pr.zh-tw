---
description: Direct3D 使用一種稱為雙線性篩選的線性材質篩選形式。
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: " (Direct3D 9) 的線性材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5177af653c74383ef87468dbb43167fa2962cd093410a6a63f85da2233e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628528"
---
# <a name="linear-texture-filtering-direct3d-9"></a> (Direct3D 9) 的線性材質篩選

Direct3D 使用一種稱為雙線性篩選的線性材質篩選形式。 如同 [最接近的點取樣 (Direct3D 9) ](nearest-point-sampling.md)，雙線性紋理篩選會先計算材質位址，這通常不是整數位址。 雙線性篩選接著會尋找其整數位址最接近計算位址的材質。 此外，Direct3D 轉譯模組會計算材質的加權平均值，其位於下方、下方、位於最接近樣本點的左邊、右邊。

藉由叫用 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法，選取雙線性紋理篩選。 將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。 \_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。 \_在第三個參數中傳遞 D3DTEXF 線性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質篩選](texture-filtering.md)
</dt> </dl>

 

 
