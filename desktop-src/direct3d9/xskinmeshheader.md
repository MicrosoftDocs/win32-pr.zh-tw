---
description: 此範本只會在包含匯出外觀資訊的網格中，以每個網狀架構為基礎來具現化。 此範本的目的是要提供已匯出之外觀資訊性質的相關資訊。
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796852"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

此範本只會在包含匯出外觀資訊的網格中，以每個網狀架構為基礎來具現化。 此範本的目的是要提供已匯出之外觀資訊性質的相關資訊。

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

其中：

-   nMaxSkinWeightsPerVertex-影響網格中頂點的最大轉換數目。
-   nMaxSkinWeightsPerFace-影響任何臉部之三個頂點的唯一轉換數目上限。
-   nBones-影響此網格中頂點的骨骼數目。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



