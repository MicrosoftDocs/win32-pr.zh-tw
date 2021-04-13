---
title: 操作影像以用於紋理
description: OpenGL 公用程式程式庫 (X.GLU 隊) 提供影像縮放和自動 mipmap 功能，以簡化材質影像的規格。
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- OpenGL 公用程式 (X.GLU 隊) ，影像縮放比例
- X.GLU 隊 (OpenGL 公用程式) ，影像縮放比例
- OpenGL 公用程式 (X.GLU 隊) 、自動 mipmap
- X.GLU 隊 (OpenGL 公用程式) 、自動 mipmap
- OpenGL 公用程式 (X.GLU 隊) 、材質影像
- X.GLU 隊 (OpenGL 公用程式) 、材質影像
- X.GLU 隊程式庫，材質影像
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300632"
---
# <a name="manipulating-images-for-use-in-texturing"></a>操作影像以用於紋理

OpenGL 公用程式程式庫 (X.GLU 隊) 提供影像縮放和自動 mipmap 功能，以簡化材質影像的規格。 [**GluScaleImage**](gluscaleimage.md)函式會將指定的影像調整為接受的材質大小;您可以將產生的影像以材質形式傳遞至 OpenGL。 自動 mipmap 函式（ [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) 和 [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)）會從指定的影像建立 mipmapped 材質影像，並將它們分別傳遞給 [**glTexImage1D**](glteximage1d.md) 和 [**glTexImage2D**](glteximage2d.md)。

 

 




