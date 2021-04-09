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
# <a name="animationoptions"></a>AnimationOptions

可讓您設定動畫選項。

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

其中：

-   openclosed-使用0表示封閉的動畫，或使用1表示開啟的動畫。 依預設，會關閉動畫。
-   positionquality-設定任何指定位置索引鍵的位置品質。 針對曲線位置使用0，或針對線性位置使用1。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



