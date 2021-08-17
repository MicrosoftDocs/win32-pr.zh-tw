---
description: 您可以使用此注釋，將外部檔案的內容定義為效果參數的初始化值。
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: 參數初始化注釋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798657"
---
# <a name="parameter-initialization-annotation"></a>參數初始化注釋

您可以使用此注釋，將外部檔案的內容定義為效果參數的初始化值。 例如：


```
string SasResourceAddress = "Value";
```



其中，值是可能包含絕對或相對路徑的 ASCII 文字字串。 相對路徑是相對於包含效果檔案的目錄。

以下是範例：


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



預設值為空字串。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX 標準注釋和語義參考](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



