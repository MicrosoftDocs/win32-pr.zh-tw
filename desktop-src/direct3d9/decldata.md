---
description: 描述頂點宣告。
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: DeclData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5686e3344e4642483490c9bd2892cbc92ade290567107b702cc9c56ff351c71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803233"
---
# <a name="decldata"></a>DeclData

描述頂點宣告。

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

其中：

-   nElements：頂點宣告元素的數目。
-   Elements \[ nElements \] -頂點宣告元素的陣列。
-   nDWords-DWORD 的數目。
-   資料 \[ nDWords \] -dword 的陣列，其中包含每個頂點元素中的資料。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



