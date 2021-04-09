---
title: " define"
description: '\ 定義指示詞會將指定的值指派給指定的名稱。 所有後續出現的名稱都會以值取代。'
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674167"
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

 

 




