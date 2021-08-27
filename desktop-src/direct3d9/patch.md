---
description: 定義 B&\# 233; zier 控制項修補程式。 陣列會定義修補程式的控制點。
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f57ac0cec68a1e8d1651c0e6ad2aabde6f1f6b949b085aa0dc35bd6e02c82a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118623"
---
# <a name="patch"></a>Patch

定義貝塞爾控制項修補程式。 陣列會定義修補程式的控制點。

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

其中：

-   nControlIndices-控制點索引的數目。
-   陣列 DWORD controlIndices \[ nControlIndices \] -控制點索引的陣列。

修補程式的類型是由控制點的數目所定義，如下表所示。



| 控制點數目 | 類型                              |
|--------------------------|-----------------------------------|
| 10                       | 三次貝塞爾三角形 patch     |
| 15                       | Quartic 貝塞爾三角形 patch   |
| 16                       | 三次方貝塞爾四個矩形修補程式 |



 

控制點的順序會以螺旋線模式提供，如下圖所示，適用于三角形和矩形的修補程式。

三角修補程式使用下列模式。

![三角化修補程式模式的圖表](images/tripatch.png)

矩形修補程式使用下列模式。

![矩形修補程式模式的圖表](images/quadpatch.png)

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



