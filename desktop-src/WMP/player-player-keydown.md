---
title: Player. KeyDown 事件
description: 按下按鍵時，就會發生 KeyDown 事件。 |Player. KeyDown 事件
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- KeyDown 事件 Windows Media Player
- KeyDown 事件 Windows Media Player、Player 類別
- Player 類別 Windows Media Player，KeyDown 事件
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a067e0125bea6bcabec591d6c1f3ec6fc5a2ee1b0d649a02009690c89d68952e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134771"
---
# <a name="playerkeydown-event"></a>Player. KeyDown 事件

按下按鍵時，就會發生 **KeyDown** 事件。

## <a name="syntax"></a>語法


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*nKeyCode* 
</dt> <dd>

 (**int**) 指定按下哪個實體索引鍵的 **數目**。 如需了解可能的值，請參閱＜備註＞一節。

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Number** (**int**) 指定具有最少有效位數的位位（對應至 SHIFT 鍵 (BIT 0) 、CTRL 鍵 (位 1) ，以及 ALT 鍵 (位 2) ）。 這些位會分別對應至值1、2和4。 Shift 引數表示這些索引鍵的狀態。 您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

*NKeyCode* 引數會指定實體索引鍵。 下表顯示標準鍵盤上主要索引鍵的可能值。

主要索引鍵的值。



| Key                     | 值   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| CAPS LOCK               | 20      |
| 向左或向右移動 ()    | 16      |
| CTRL (左或右)     | 17      |
| ALT (左或右)      | 18      |
| SPACE                   | 32      |
| 退格鍵               | 8       |
| ENTER                   | 13      |
| Windows 標誌鍵，左方  | 91      |
| Windows 標誌鍵，right | 92      |
| 應用程式金鑰         | 93      |



 

數位板索引鍵的值。



| Key               | 值  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM LOCK          | 144    |
| 除以 (/)         | 111    |
| 將 (乘以 \*)      | 106    |
| 減去 (-)       | 109    |
| 新增 (+)            | 107    |
|  (輸入) 的分隔符號 | 108    |
| DECIMAL (。 )        | 110    |



 

導覽鍵的值。



| Key         | 值 |
|-------------|-------|
| INSERT      | 45    |
| DELETE      | 46    |
| HOME        | 36    |
| END         | 35    |
| PAGE UP     | 33    |
| PAGE DOWN   | 34    |
| 向上鍵    | 38    |
| DOWN ARROW  | 40    |
| 向左鍵  | 37    |
| 向右鍵 | 39    |



 

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

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

 

 





