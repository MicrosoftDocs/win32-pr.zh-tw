---
description: ICE22 會使用 FeatureComponents 資料表來驗證 PublishComponent 資料表中所參考的功能和元件的對應。
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987654"
---
# <a name="ice22"></a>ICE22

ICE22 會使用 [FeatureComponents 資料表](featurecomponents-table.md) 來驗證 [PublishComponent 資料表](publishcomponent-table.md)中所參考的功能和元件的對應。

## <a name="result"></a>結果

如果功能和元件在 [PublishComponent 資料表](publishcomponent-table.md)中的對應不正確，ICE22 會張貼錯誤訊息。

## <a name="example"></a>範例

在下列範例中，ICE22 會張貼沒有 {00000003-0004-0000-0000-624474732465} 功能和元件資料行之正確對應的錯誤 \_ \_ 。

[PublishComponent 資料表](publishcomponent-table.md) (部分) 



| ComponentId                            | 功能\_ | 元件\_ |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | Feat1     | Comp1       |
| {00000003-0004-0000-0000-624474732465} | Feat1     | Comp2       |



 

[FeatureComponents 資料表](featurecomponents-table.md) (部分) 



| 功能\_ | 元件\_ |
|-----------|-------------|
| Feat1     | Comp1       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



