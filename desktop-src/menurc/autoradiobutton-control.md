---
title: AUTORADIOBUTTON 控制項
description: 定義自動選項按鈕控制項。 此控制項會自動與相同群組中的其他 AUTORADIOBUTTON 控制項執行互斥。 選擇按鈕時，應用程式會在按下 BN 時收到通知 \_ 。
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- AUTORADIOBUTTON 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678435"
---
# <a name="autoradiobutton-control"></a>AUTORADIOBUTTON 控制項

定義自動選項按鈕控制項。 此控制項會自動與相同群組中的其他 **AUTORADIOBUTTON** 控制項執行互斥。 選擇按鈕時，應用程式會在按下 **BN 時 \_** 收到通知。

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

將顯示在選項按鈕旁的文字。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

自動選項按鈕的樣式，可以是按鈕類別樣式和下列樣式的組合： **ws \_ TABSTOP**、 **ws \_ DISABLED** 和 **ws \_ GROUP**。

如果您未指定樣式，則預設樣式為 `BS_AUTORADIOBUTTON | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control-control.md)
</dt> <dt>

[選項按鈕](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




