---
description: 您也可以在材質中提供 Alpha。 若要啟用材質 Alpha，請設定擴散材質轉譯狀態，讓執行時間使用材質擴散色彩元件，而不是頂點擴散色彩元件。
ms.assetid: fd477d8f-d838-4a08-a8c6-38678798e0b0
title: " (Direct3D 9 的材質 Alpha) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a70ed4a3f5bcaf38f4ace079af5b2e1804af0e24340e5004898c9ed26707d40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798975"
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

 

 



