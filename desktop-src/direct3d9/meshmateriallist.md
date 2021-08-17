---
description: 用於網格物件中，以指定要將哪些材質套用至哪些臉部。 NMaterials 成員會指定有多少材質存在，而材質則會指定要套用的材質。
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798784"
---
# <a name="meshmateriallist"></a>MeshMaterialList

用於網格物件中，以指定要將哪些材質套用至哪些臉部。 NMaterials 成員會指定有多少材質存在，而材質則會指定要套用的材質。

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

其中：

-   nMaterials-DWORD。 材質數目。
-   nFaceIndexes-DWORD。 索引的數目。
-   faceIndexes \[ nFaceIndexes \] -包含臉部索引的 dword 陣列。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



