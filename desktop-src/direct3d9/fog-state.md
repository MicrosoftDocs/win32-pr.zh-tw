---
description: 霧化效果可讓3D 場景更具逼真。
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: " (Direct3D 9) 的霧化狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84004b8f261f9a6dc4c9b800ba5baa1f9a3c3e528db2b94e86286c3752414729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564238"
---
# <a name="fog-state-direct3d-9"></a> (Direct3D 9) 的霧化狀態

霧化效果可讓3D 場景更具逼真。 您可以使用不超過模擬霧化的霧化效果。 它們也可以減少具有距離的場景清晰度。 這會反映真實世界中發生的狀況;當物件從使用者變得更遠時，其詳細資料就比較不相異。

如需在應用程式中使用霧化的詳細資訊，請參閱 [ (Direct3D 9) 的霧化 ](fog.md)。

C + + 應用程式會透過裝置呈現狀態控制霧化。 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)列舉型別包含的狀態可控制是否使用圖元 (資料表) 或頂點模糊、其色彩、系統套用的霧化公式，以及公式的參數。

您可以藉由將 D3DRS \_ FOGENABLE 轉譯狀態設為 **TRUE** 來啟用霧化。 您可以使用 D3DRS FOGCOLOR 轉譯狀態將霧化色彩設定為任何色彩值 \_ ; 會忽略霧化色彩的 Alpha 元件。

D3DRS \_ FOGTABLEMODE 和 D3DRS \_ FOGVERTEXMODE 轉譯狀態會控制適用于霧化計算的霧化公式，並間接控制要套用的霧化類型。 這兩種轉譯狀態都可以設定為 [**D3DFOGMODE**](./d3dfogmode.md) 列舉型別的成員。 將 [轉譯狀態] 設定為 D3DFOG [無] 會 \_ 分別停用圖元或頂點霧化。 如果這兩種轉譯狀態都設為有效的模式，則系統只會套用圖元霧化效果。

D3DRS \_ FOGSTART 和 D3DRS \_ FOGEND 轉譯狀態會控制 D3DFOG 線性模式的霧化公式參數 \_ 。 D3DRS \_ FOGDENSITY 轉譯狀態會控制指數霧化模式中的霧化密度。

如需詳細資訊，請參閱 [ (Direct3D 9) 的霧化參數 ](fog-parameters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
