---
title: STYLE 語句
description: 定義對話方塊的視窗樣式。 視窗樣式會指定方塊是快顯視窗或子視窗。
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- 樣式語句功能表和其他資源
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375193"
---
# <a name="style-statement"></a>STYLE 語句

定義對話方塊的視窗樣式。 視窗樣式會指定方塊是快顯視窗或子視窗。

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

視窗樣式。 這個參數可以是整數值，也可以是視窗樣式值的組合 (例如 **ws \_ 標題** 和 **WS \_ SYSMENU**) 和對話方塊樣式值 (例如 **DS \_ CENTER**) 。

</dd> </dl>

如需視窗樣式的清單，請參閱 [視窗樣式](/windows/desktop/winmsg/window-styles)。 如需對話方塊樣式的清單，請參閱 [對話方塊範本樣式](../dlgbox/about-dialog-boxes.md)。 如果您使用視窗或對話方塊的樣式值，就必須包含 Windows .h。

 

 