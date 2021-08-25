---
description: 霧化混色指的是 [霧化] 和 [物件色彩] 的 [霧化] 因數，以產生出現在場景中的最終色彩，如 (Direct3D 9) 中的霧化公式所述。
ms.assetid: b5b43f12-bbed-4464-aebc-02ad6dab1951
title: " (Direct3D 9) 的霧化混色"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60f3402daf71a3fce14af936334c3d96e928d3469452eafb94d139594bb0b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894018"
---
# <a name="fog-blending-direct3d-9"></a> (Direct3D 9) 的霧化混色

霧化混色指的是 [霧化] 和 [物件色彩] 的 [霧化] 因數，以產生出現在場景中的最終色彩，如 [ (Direct3D 9) 中的霧化公式 ](fog-formulas.md)所述。 D3DRS \_ FOGENABLE 轉譯狀態控制項霧化混色。 將此呈現狀態設為 **TRUE** ，以啟用霧化混合，如下列範例程式碼所示。 預設值為 **FALSE**。


```
// For this example, g_pDevice is a valid pointer
// to an IDirect3DDevice9 interface.
HRESULT hr;
hr = g_pDevice->SetRenderState(
                    D3DRS_FOGENABLE,
                    TRUE);
if FAILED(hr)
    return hr;
```



您必須啟用圖元霧化和頂點霧化的霧化混合。 如需有關使用這些類型的霧化的詳細資訊，請參閱 [ (direct3d 9 的圖元霧化) ](pixel-fog.md) 和 [ (direct3d 9) 的頂點霧化 ](vertex-fog.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 



