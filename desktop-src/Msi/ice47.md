---
description: ICE47 會檢查功能和 FeatureComponents 資料表，以取得具有1600或更多元件的功能。
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcf1f71af9bb8784c15b159836d329a94e7e6f33b34c31cbba72f9b31349a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381948"
---
# <a name="ice47"></a>ICE47

ICE47 會檢查 [功能](feature-table.md) 和 [FeatureComponents](featurecomponents-table.md) 資料表，以取得具有1600或更多元件的功能。

## <a name="result"></a>結果

如果功能超過每項功能1600個元件的上限，ICE47 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE47 會報告下列警告：

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

[功能表](feature-table.md) (部分) 



| 功能  |
|----------|
| Feature1 |



 

[FeatureComponents 資料表](featurecomponents-table.md) (部分) 



| 動作   | 條件     |
|----------|---------------|
| Feature1 | Component1    |
| Feature1 | Component1600 |



 

若要修正此警告，請嘗試將功能分割成數個功能

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



