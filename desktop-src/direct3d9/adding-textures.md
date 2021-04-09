---
description: 若要加入材質，請使用檔案格式的階層式本質，並將選擇性的 TextureFilename 資料物件加入至材質資料物件。
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: '將材質新增 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee0090b5990c2093a41efbd15eb998401ce2607
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110276"
---
# <a name="adding-textures-direct3d-9"></a><span data-ttu-id="85f2e-103">將材質新增 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="85f2e-103">Adding Textures (Direct3D 9)</span></span>

<span data-ttu-id="85f2e-104">若要加入材質，請使用檔案格式的階層式本質，並將選擇性的 [**TextureFilename**](texturefilename.md) 資料物件加入至 [**材質**](material.md) 資料物件。</span><span class="sxs-lookup"><span data-stu-id="85f2e-104">To add textures, use the hierarchical nature of the file format and add an optional [**TextureFilename**](texturefilename.md) data object to the [**Material**](material.md) data objects.</span></span> <span data-ttu-id="85f2e-105">**材質** 物件現在如下所示：</span><span class="sxs-lookup"><span data-stu-id="85f2e-105">The **Material** objects now read as follows:</span></span>


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a><span data-ttu-id="85f2e-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="85f2e-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85f2e-107">X 檔案 (舊版) </span><span class="sxs-lookup"><span data-stu-id="85f2e-107">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



