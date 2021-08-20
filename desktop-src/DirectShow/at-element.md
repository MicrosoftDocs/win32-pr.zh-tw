---
description: At 元素會在特定時間定義 param 專案的值，相對於包含參數的轉換或效果的開頭。
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at 元素
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824388"
---
# <a name="at-element"></a>at 元素

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

專案 `at` 會在特定時間定義 [**param**](param-element.md) 專案的值，相對於包含參數的轉換或效果的開頭。 `at`元素會在指定的時間，讓參數跳到新值。 若要讓新值的進展順利進行，請使用 [**線性**](linear-element.md) 元素。

## <a name="attributes"></a>屬性

[**時間**](time-attribute.md)、 [**值**](value-attribute.md)

## <a name="parentchild-information"></a>父系/子系資訊



| 標籤 | 值 |
|----------|--------------------------------|
| 父代   | [**參數**](param-element.md) |
| Children | 無                           |



 

## <a name="examples"></a>範例


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XTL 元素](xtl-elements.md)
</dt> </dl>

 

 



