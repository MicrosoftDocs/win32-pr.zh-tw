---
title: Player. URL
description: URL 屬性會指定或抓取要播放之媒體專案的名稱。
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Player. URL Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999197"
---
# <a name="playerurl"></a>Player. URL

**URL** 屬性會指定或抓取要播放之媒體專案的名稱。

## <a name="syntax"></a>Syntax

*玩家* 。**URL**

## <a name="possible-values"></a>可能的值

這個屬性是沒有預設值的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

這個屬性只能設定為安全性區域中的 URL，該 URL 的安全性區域與呼叫的程式或網頁的安全性區域相同或較不嚴格。

如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則從防火牆後方開啟媒體專案的應用程式將會有較佳的效能。

請勿從事件處理常式程式碼呼叫此方法。 呼叫 *Player*。來自事件處理常式的 **URL** 可能會產生非預期的結果。

## <a name="examples"></a>範例

下列範例會建立 HTML 文字輸入專案和 HTML 按鈕 input 元素。 TEXT 元素可讓使用者輸入路徑來指定要播放的數位媒體檔案。 BUTTON 元素會執行開啟檔案的 JScript，並啟動 Windows Media Player。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





