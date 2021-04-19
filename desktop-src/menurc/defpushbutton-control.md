---
title: DEFPUSHBUTTON 控制項
description: 定義預設的按鈕控制項。
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- DEFPUSHBUTTON 控制項功能表和其他資源
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965625"
---
# <a name="defpushbutton-control"></a>DEFPUSHBUTTON 控制項

定義預設的按鈕控制項。 控制項是具有粗體外框的小矩形，代表使用者的預設回應。 指定的文字會顯示在按鈕內。 控制項會在使用者按一下按鈕時，以一般方式反白顯示按鈕，並將訊息傳送至其父視窗。

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

要置於控制項矩形區域中的文字。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這個值可以是下列樣式的組合： **BS \_ DEFPUSHBUTTON**、 **WS \_ TABSTOP**、 **ws \_ GROUP** 和 **ws \_ DISABLED**。

如果您未指定樣式，則預設樣式為 `BS_DEFPUSHBUTTON | WS_TABSTOP` 。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

這個範例會定義一個標示為 [取消] 的預設按鈕控制項：

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[推播按鈕](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**按鈕**](pushbutton-control.md)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




