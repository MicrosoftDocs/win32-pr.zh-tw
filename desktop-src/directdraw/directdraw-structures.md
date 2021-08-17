---
title: DirectDraw 結構
description: 此區段包含下列與 DirectDraw 搭配使用之結構的相關資訊
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba62751b619982628575b380ea75eb57661db8737325fee1fb1b042e856ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504340"
---
# <a name="directdraw-structures"></a>DirectDraw 結構

本章節包含下列與 DirectDraw 搭配使用之結構的相關資訊：

-   [**DDBLTBATCH**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**DDBLTFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**DDCOLORCONTROL**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**DDCOLORKEY**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**DDGAMMARAMP**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**DDOVERLAYFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**DDPIXELFORMAT**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**DDSCAPS**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> 使用結構之前，您應該將每個 DirectX 結構的記憶體初始化為0。 此外，對於包含 **dwSize** 成員的所有結構，您應該將成員設定為使用結構之前的結構大小（以位元組為單位）。 下列範例會在通用結構 [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)上執行這些工作：

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




