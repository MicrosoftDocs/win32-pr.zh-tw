---
title: 選擇 RGBA 和 Color-Index 模式
description: 一般情況下，請使用您的 OpenGL 應用程式的 RGBA 模式;除了陰影、光源、色彩對應、霧化、消除鋸齒和混合等效果的色彩索引模式之外，還提供更多的彈性。
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- Windows 上的 OpenGL、RGBA 模式
- Windows 上的 OpenGL、色彩索引模式
- RGBA 模式 OpenGL
- 色彩索引模式 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673148"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>選擇 RGBA 和 Color-Index 模式

一般情況下，請使用您的 OpenGL 應用程式的 RGBA 模式;除了陰影、光源、色彩對應、霧化、消除鋸齒和混合等效果的色彩索引模式之外，還提供更多的彈性。

在下列情況下，請考慮使用色彩索引模式：

-   如果您的可用 bitplanes 數目有限，色彩索引模式可能會產生比 RGBA 模式更不粗略的陰影。
-   如果您不在意使用「真實」色彩，例如，在地形對應中使用數種色彩來指定相對提升。
-   當您要移植的現有應用程式會大量使用色彩索引模式時。
-   當您想要在應用程式中使用色彩對應動畫和效果時。  (不可能發生在真色彩裝置上。 ) 

 

 




