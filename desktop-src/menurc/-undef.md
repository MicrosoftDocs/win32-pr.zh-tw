---
title: " undef"
description: '\ Undef 指示詞會移除指定之名稱的目前定義。 所有後續出現的名稱都不需要取代即可進行處理。'
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adf208ecca3f130aefc99de8d2926028f25bcd46be46d42e4cbf92e708fa0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473058"
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

 

 




