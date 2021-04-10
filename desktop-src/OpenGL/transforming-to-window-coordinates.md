---
title: 轉換成視窗座標
description: 在剪切座標轉換成視窗座標之前，會將它們除以 w 的值，以產生正規化的裝置座標。
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- OpenGL 處理管線，轉換成視窗座標
- 轉換成視窗座標 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675483"
---
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="68906-105">轉換成視窗座標</span><span class="sxs-lookup"><span data-stu-id="68906-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="68906-106">在剪切座標轉換成視窗座標之前，會將它們除以 *w* 的值，以產生正規化的裝置座標。</span><span class="sxs-lookup"><span data-stu-id="68906-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="68906-107">套用至這些正規化座標的「視口」轉換會產生視窗座標。</span><span class="sxs-lookup"><span data-stu-id="68906-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="68906-108">您可以使用 [**glDepthRange**](gldepthrange.md) 和 [**glViewport**](glviewport.md)來控制顯示影像的螢幕視窗區域，以決定顯示影像的區域。</span><span class="sxs-lookup"><span data-stu-id="68906-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




