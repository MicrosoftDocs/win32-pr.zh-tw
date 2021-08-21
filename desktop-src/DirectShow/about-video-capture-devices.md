---
description: 關於影片捕獲裝置
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: 關於影片捕獲裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160181"
---
# <a name="about-video-capture-devices"></a>關於影片捕獲裝置

大部分新的影片捕獲裝置都會使用 Windows Driver Model (WDM) 驅動程式。 在 WDM 架構中，Microsoft 提供一組與硬體無關的驅動程式，稱為類別驅動程式，硬體廠商則提供硬體特定的 minidrivers。 迷你驅動程式會實作用於裝置的任何函式;針對大部分的函式，迷你驅動程式會呼叫 Microsoft class 驅動程式。

在 DirectShow 篩選圖形中，任何 wdm 捕獲裝置都會顯示為[wdm 影片捕獲](wdm-video-capture-filter.md)篩選器。 WDM 影片捕獲篩選器會根據驅動程式的特性來設定本身。 它會顯示在驅動程式所提供的名稱底下，在圖形中的任何位置都不會看到名為「WDM 影片捕獲篩選器」的篩選。

某些較舊的捕獲裝置仍會使用影片進行 Windows (VFW) 驅動程式。 雖然這些驅動程式現在已過時，但 DirectShow 透過[VFW Capture](vfw-capture-filter.md)篩選器來支援這些驅動程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow 中的影片捕獲](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



