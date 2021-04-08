---
title: 限制
description: 限制
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- Windows 上的 OpenGL，限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672683"
---
# <a name="limitations"></a>限制

泛型實有下列限制：

-   列印：

    您只能使用中繼檔將 OpenGL 影像直接列印到印表機。 如需詳細資訊，請參閱 [列印 OpenGL 映射](printing-an-opengl-image.md)。

-   在雙重緩衝的視窗中，無法混合 OpenGL 和 GDI 圖形。

    應用程式可以將 OpenGL 圖形和 GDI 圖形直接繪製成單一緩衝視窗，但不能直接繪製到雙重緩衝視窗。

-   沒有每個視窗的硬體色彩調色板。

    Windows 具有單一系統硬體調色板，適用于整個畫面。 OpenGL 視窗不能有自己的硬體調色板，但可以有自己的邏輯調色板。 若要這樣做，它必須變成可辨識元件的應用程式。 如需詳細資訊，請參閱 [OpenGL 色彩模式和 Windows 調色板管理](opengl-color-modes-and-windows-palette-management.md)。

-   不直接支援剪貼簿、動態資料交換 (DDE) 或 OLE。

    具有 OpenGL 圖形的視窗不直接支援這些 Windows 功能。 不過，有一些因應措施可使用剪貼簿。 如需詳細資訊，請參閱 [將 OpenGL 影像複製到剪貼](copying-an-opengl-image-to-the-clipboard.md)簿。

-   不包含發明者 2.0 c + + 類別庫。

    發明者類別庫建置於 OpenGL 之上，可提供更高層級的程式設計3D 圖形。 它並未包含在目前版本的適用于 Windows 的 OpenGL 中。

-   下列像素格式功能不支援： stereoscopic 影像、Alpha bitplanes 和輔助緩衝區。

    不過，也支援數個附屬緩衝區，包括：樣板緩衝區、累積緩衝區、背景緩衝區 (雙緩衝) 、重迭和基礎平面緩衝區，以及深度 (Z 軸) 緩衝區。

 

 




