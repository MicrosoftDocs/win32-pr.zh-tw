---
description: 用來定義換行中每個臉部的材質拓撲。 NFaceWrapValues 成員的值應等於網格中的臉部數目。
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509782"
---
# <a name="meshfacewraps"></a><span data-ttu-id="00211-104">MeshFaceWraps</span><span class="sxs-lookup"><span data-stu-id="00211-104">MeshFaceWraps</span></span>

<span data-ttu-id="00211-105">用來定義換行中每個臉部的材質拓撲。</span><span class="sxs-lookup"><span data-stu-id="00211-105">Used to define the texture topology of each face in a wrap.</span></span> <span data-ttu-id="00211-106">NFaceWrapValues 成員的值應等於網格中的臉部數目。</span><span class="sxs-lookup"><span data-stu-id="00211-106">The value of the nFaceWrapValues member should be equal to the number of faces in a mesh.</span></span>

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

<span data-ttu-id="00211-107">此範本已不再使用。</span><span class="sxs-lookup"><span data-stu-id="00211-107">This template is no longer used.</span></span>

## <a name="see-also"></a><span data-ttu-id="00211-108">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00211-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00211-109">範本</span><span class="sxs-lookup"><span data-stu-id="00211-109">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



