---
title: " define"
description: '\ 定義指示詞會將指定的值指派給指定的名稱。 所有後續出現的名稱都會以值取代。'
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826048"
---
# <a name="define"></a>\#定義

**\# Define** 指示詞會將指定的值指派給指定的名稱。 所有後續出現的名稱都會以值取代。

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

要定義的名稱。 此值是字母、數位和標點符號的任意組合，適用于 C/c + + 預處理器。

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*價值*
</dt> <dd>

整數、字元字串或文字行。

</dd> </dl>

## <a name="example"></a>範例

這個範例會將值指派給名稱非零和 USERCLASS：

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




