---
description: 若要改善轉譯效能，您可以挑選出 (，或從相機中移除) 的基本物件。
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: " (Direct3D 9) 的挑選狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111009"
---
# <a name="culling-state-direct3d-9"></a> (Direct3D 9) 的挑選狀態

若要改善轉譯效能，您可以挑選出 (，或從相機中移除) 的基本物件。 若是單面基本專案，這會節省轉譯時間，因為看不見背面的臉部。 若要啟用剔除，您需要知道頂點的纏繞順序 (通常會逆時針地) 。 此範例將會移除背面臉部朝前 (的任何基本型別) 的逆時針繞組順序：


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 



