---
description: 可讓您設定動畫選項。
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111013"
---
# <a name="animationoptions"></a><span data-ttu-id="a1794-103">AnimationOptions</span><span class="sxs-lookup"><span data-stu-id="a1794-103">AnimationOptions</span></span>

<span data-ttu-id="a1794-104">可讓您設定動畫選項。</span><span class="sxs-lookup"><span data-stu-id="a1794-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="a1794-105">其中：</span><span class="sxs-lookup"><span data-stu-id="a1794-105">Where:</span></span>

-   <span data-ttu-id="a1794-106">openclosed-使用0表示封閉的動畫，或使用1表示開啟的動畫。</span><span class="sxs-lookup"><span data-stu-id="a1794-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="a1794-107">依預設，會關閉動畫。</span><span class="sxs-lookup"><span data-stu-id="a1794-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="a1794-108">positionquality-設定任何指定位置索引鍵的位置品質。</span><span class="sxs-lookup"><span data-stu-id="a1794-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="a1794-109">針對曲線位置使用0，或針對線性位置使用1。</span><span class="sxs-lookup"><span data-stu-id="a1794-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1794-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1794-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1794-111">範本</span><span class="sxs-lookup"><span data-stu-id="a1794-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



