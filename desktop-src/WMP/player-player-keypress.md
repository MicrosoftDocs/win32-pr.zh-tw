---
title: Player. KeyPress 事件
description: 按下並釋放按鍵時，就會發生 KeyPress 事件。 |Player. KeyPress 事件
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- 按鍵事件 Windows Media Player
- KeyPress 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player，按鍵事件
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994634"
---
# <a name="playerkeypress-event"></a>Player. KeyPress 事件

按下並釋放按鍵時，就會發生 **KeyPress** 事件。

## <a name="syntax"></a>語法


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*nKeyAscii* 
</dt> <dd>

**數位** (**int**) 指定字元的標準數值 ANSI 代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

當擊鍵產生任何可列印的鍵盤字元、CTRL 鍵與標準字母中的字元或一些特殊字元的其中一個字元，以及 ENTER 鍵或倒退鍵時，就會發生此事件。

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





