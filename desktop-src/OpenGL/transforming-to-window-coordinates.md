---
title: 轉換成視窗座標
description: 在剪切座標轉換成視窗座標之前，會將它們除以 w 的值，以產生正規化的裝置座標。
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- OpenGL 處理管線，轉換成視窗座標
- 轉換成視窗座標 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa74b42457349b14e151099a3c4238e855ad0001e1b8f9416808a1279b82345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887988"
---
# <a name="transforming-to-window-coordinates"></a>轉換成視窗座標

在剪切座標轉換成視窗座標之前，會將它們除以 *w* 的值，以產生正規化的裝置座標。 套用至這些正規化座標的「視口」轉換會產生視窗座標。 您可以使用 [**glDepthRange**](gldepthrange.md) 和 [**glViewport**](glviewport.md)來控制顯示影像的螢幕視窗區域，以決定顯示影像的區域。

 

 




