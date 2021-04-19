---
title: AmbientAttributes.accKeyboardShortcut
description: AccKeyboardShortcut 屬性會指定或抓取任何元素的鍵盤快速鍵描述。
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes. accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982985"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

**AccKeyboardShortcut** 屬性會指定或抓取任何元素的鍵盤快速鍵描述。

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **字串** ，其預設值為 "" (空白字串) 。 若為 **BUTTON** 元素，此屬性的預設值為 "空格鍵或 Enter"。 若為 **滑杆** 元素，預設值為「向右/向上箭號，可增加、向左/向下箭號以減少」。

## <a name="remarks"></a>備註

這個屬性會用於協助工具用途。 它允許讀取器程式大聲讀出任何專案的鍵盤快速鍵描述。 這個屬性不會設定快捷方式。 腳本處理常式必須執行該工作。

這個屬性也適用于按鈕群組控制項內的按鈕元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





