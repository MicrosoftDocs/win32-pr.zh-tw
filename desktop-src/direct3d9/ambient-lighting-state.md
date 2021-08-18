---
description: 環境光源的周圍是從所有方向 radiates 的光源。 如需 Direct3D 如何使用環境光線的詳細資訊，請參閱 (Direct3D 9) 的數學運算。
ms.assetid: c5aa493e-09b8-433c-a21c-e39af795b3c9
title: '環境光源狀態 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc32a6ec654bd30627c853bc00c90e94b6008e769fb3aa708e963a9430e0dc85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952688"
---
# <a name="ambient-lighting-state-direct3d-9"></a>環境光源狀態 (Direct3D 9) 

環境光源的周圍是從所有方向 radiates 的光源。 如需 Direct3D 如何使用環境光線的詳細資訊，請參閱 [ (Direct3D 9) 的數學 ](mathematics-of-lighting.md)運算。

C + + 應用程式藉由叫用 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，並將列舉值 D3DRS \_ 環境傳遞為第一個參數，來設定環境光源的色彩。 第二個參數是色彩值。 預設值為零。


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the ambient light.

d3dDevice->SetRenderState(D3DRS_AMBIENT, 0x00202020);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
