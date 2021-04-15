---
title: EXSTYLE 語句
description: 定義對話方塊的延伸視窗樣式。 在資源定義中，EXSTYLE 語句會在資源定義主體開頭之前加上選擇性的語句。
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- EXSTYLE 語句功能表和其他資源
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463044"
---
# <a name="exstyle-statement"></a>EXSTYLE 語句

定義對話方塊的延伸視窗樣式。 在資源定義中， **EXSTYLE** 語句會在資源定義主體開頭之前加上選擇性的語句。

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*擴充樣式*
</dt> <dd>

對話方塊或控制項的擴充視窗樣式。 如需延伸視窗樣式的清單，請參閱 [**擴充的視窗樣式**](/windows/desktop/winmsg/extended-window-styles)。

</dd> </dl>

## <a name="remarks"></a>備註

對於控制項，擴充樣式是在控制項資源定義語句的 *style* 選項之後指定。 如需詳細資訊，請參閱個別控制項的資源定義語句。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**控制**](control-control.md)
</dt> <dt>

[**對話 框**](dialog-resource.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**彈出**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[使用者定義的資源](user-defined-resource.md)
</dt> </dl>

 

 