---
description: DirectDraw 獨佔模式
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: DirectDraw 獨佔模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09199e04a221299676c21fbc2876af4b8149943a743101d34893d5563ed42482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016177"
---
# <a name="directdraw-exclusive-mode"></a>DirectDraw 獨佔模式

> [!Note]  
> 本主題僅適用于 VMR-7。 在 VMR-9 中，您可以藉由提供專屬的獨佔模式配置器-展示者來啟用獨佔模式。 如果您使用 [**IVMRSurfaceAllocatorNotify9：： AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) 方法，這會相當簡單。 VMR9Allocator 範例會示範如何執行自訂配置器-展示者。

 

在 DirectDraw 獨佔模式中，應用程式會獨佔控制圖形硬體。 這對於遊戲等應用程式或可能是全螢幕的影片應用程式很有用。 一般來說，VMR 會建立 DirectDraw 物件，並將合作層級設定為 [一般]。 不過，若要在 DirectDraw 獨佔模式中執行 VMR，應用程式本身必須建立 DirectDraw 物件和主要介面，然後呼叫 **SetCooperativeLevel** 以指定獨佔模式。

VMR 具有特殊的配置器提供者，可讓它在 DirectDraw 獨佔模式中執行。 若要將 VMR 設定為使用此配置器-展示者：

1.  使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter)方法建立篩選 Graph，並將 VMR 新增至其中。 如需程式碼範例，請參閱 [VMR 無視窗模式](vmr-windowless-mode.md)。
2.  建立專屬模式配置器-展示者：
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  設定新的配置器-展示者：
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  將新的配置器呈現者插入 VMR 中。
5.  以一般方式建立篩選圖形的其餘部分。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[作業的 VMR 模式](vmr-modes-of-operation.md)
</dt> </dl>

 

 



