---
title: 產生材質座標
description: 您可以使用 glTexGen \ 來將 OpenGL 產生為其他頂點資料的函式，而不是明確提供材質座標。
ms.assetid: 5c9ce163-6107-46a3-8c8d-fc87d2f8cf9a
keywords:
- OpenGL 處理管線，材質座標
- 材質座標 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d3f5b807f25aee2783ff8dab3a4930a9c797ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183728"
---
# <a name="generating-texture-coordinates"></a><span data-ttu-id="d71c3-105">產生材質座標</span><span class="sxs-lookup"><span data-stu-id="d71c3-105">Generating Texture Coordinates</span></span>

<span data-ttu-id="d71c3-106">您可以使用[glTexGen \* ](gltexgen-functions.md)，讓 OpenGL 將它們產生為其他頂點資料的函式，而不是明確提供材質座標。</span><span class="sxs-lookup"><span data-stu-id="d71c3-106">Rather than explicitly supplying texture coordinates, you can have OpenGL generate them as a function of other vertex data using [glTexGen\*](gltexgen-functions.md).</span></span> <span data-ttu-id="d71c3-107">在指定或產生材質座標之後，材質矩陣會轉換它們。</span><span class="sxs-lookup"><span data-stu-id="d71c3-107">After the texture coordinates have been specified or generated, they are transformed by the texture matrix.</span></span> <span data-ttu-id="d71c3-108">此矩陣是使用用於矩陣轉換的相同函式來控制 (請參閱 [矩陣轉換](matrix-transformations.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d71c3-108">This matrix is controlled with the same functions that are used for matrix transformations (see [Matrix Transformations](matrix-transformations.md)).</span></span>

 

 




