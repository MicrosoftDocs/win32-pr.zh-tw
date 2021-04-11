---
title: " ifdef"
description: '\ Ifdef 指示詞會藉由檢查指定的名稱來控制資源檔的條件式編譯。'
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372224"
---
# <a name="ifdef"></a>\#ifdef

**\# Ifdef** 指示詞會藉由檢查指定的名稱來控制資源檔的條件式編譯。 如果已使用 **\# define** 指示詞或使用 **/d** 命令列選項搭配資源編譯器來定義名稱， **\# ifdef** 會指示編譯器在 **\# ifdef** 指示詞後面緊接著語句繼續。 如果未定義名稱， **\# ifdef** 會指示編譯器略過所有語句，直到下一個 **\# endif** 指示詞為止。

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*名字*
</dt> <dd>

指示詞要檢查的名稱。

</dd> </dl>

## <a name="example"></a>範例

此範例只會在定義 Debug 時編譯 [**BITMAP**](bitmap-resource.md) 語句：

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器指示詞](preprocessor-directives.md)
</dt> </dl>

 

 




