---
description: ICE21 會驗證元件資料表中的每個元件都屬於某項功能。 它會使用 FeatureComponents 資料表來檢查此對應。
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529028"
---
# <a name="ice21"></a>ICE21

ICE21 會驗證 [元件資料表](component-table.md) 中的每個元件都屬於某項功能。 它會使用 [FeatureComponents 資料表](featurecomponents-table.md) 來檢查此對應。

## <a name="result"></a>結果

如果安裝套件包含不屬於某項功能的元件，ICE21 會張貼錯誤訊息。

## <a name="example"></a>範例

在下列範例中，ICE21 會張貼一則錯誤訊息，指出元件 Comp1 未對應到任何功能。

[元件資料表](component-table.md) (部分) 



| 元件 |
|-----------|
| Comp1     |
| Comp2     |



 

[FeatureComponents 資料表](featurecomponents-table.md) (部分) 



| 功能  | 元件 |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



