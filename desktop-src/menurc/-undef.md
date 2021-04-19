---
title: " undef"
description: '\ Undef 指示詞會移除指定之名稱的目前定義。 所有後續出現的名稱都不需要取代即可進行處理。'
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106995550"
---
# <a name="undef"></a>\#undef

**\# Undef** 指示詞會移除指定之名稱的目前定義。 所有後續出現的名稱都不需要取代即可進行處理。

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

要移除的名稱。 此值是字母、數位和標點符號的任意組合，適用于 C/c + + 預處理器。

</dd> </dl>

## <a name="example"></a>範例

此範例會移除名稱為非零和 USERCLASS 的定義：

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




