---
description: 您也可以在材質中提供 Alpha。 若要啟用材質 Alpha，請設定擴散材質轉譯狀態，讓執行時間使用材質擴散色彩元件，而不是頂點擴散色彩元件。
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: " (Direct3D 9 的材質 Alpha) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07ac2c28b497167f7bd742ecd8176b82b61e8f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108393"
---
# <a name="material-alpha-direct3d-9"></a> (Direct3D 9 的材質 Alpha) 

您也可以在材質中提供 Alpha。 若要啟用材質 Alpha，請設定擴散材質轉譯狀態，讓執行時間使用材質擴散色彩元件，而不是頂點擴散色彩元件。


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL );
```



使用 Alpha 值初始化材質，並在繪製前設定材質。


```
D3DMATERIAL9 mtrl;
mtrl.Diffuse = mtrl.Ambient = mtrl.Specular = mtrl.Emissive = 
    D3DCOLORVALUE(255,0,0,0.5f)

m_pd3dDevice->SetMaterial(&mtrl);     
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Alpha 混色](alpha-blending.md)
</dt> </dl>

 

 



