---
description: 滑鼠游標方法可讓應用程式藉由提供包含影像的介面來指定色彩游標。
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: 使用 (Direct3D 9) 的滑鼠游標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518916"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>使用 (Direct3D 9) 的滑鼠游標

滑鼠游標方法可讓應用程式藉由提供包含影像的介面來指定色彩游標。 如果應用程式的畫面播放速率很慢，系統將確保此資料指標會以顯示速率的一半或更高的頻率更新。 但是，資料指標的更新頻率絕不會比顯示器重新整理速率更頻繁。

滑鼠游標位置會系結至系統游標，並針對目前的顯示模式空間解析度適當地調整，但應用程式可以明確地移動。 這與 WIN32 API 支援的系統滑鼠游標的行為類似。 如需如何在 Direct3D 應用程式中使用滑鼠游標的詳細資訊，請參閱下列參考主題。

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

Direct3D 可確保在呼叫 IDirect3DDevice9 時執行硬體加速 blitting 作業的硬體執行或 Direct3D 執行時間支援滑鼠 [**：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計提示](programming-tips.md)
</dt> </dl>

 

 
