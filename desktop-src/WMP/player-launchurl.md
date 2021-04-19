---
title: LaunchURL 方法
description: LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。 |LaunchURL 方法
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- launchURL 方法 Windows Media Player
- launchURL 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，launchURL 方法
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990550"
---
# <a name="playerlaunchurl-method"></a>LaunchURL 方法

**LaunchURL** 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。

## <a name="syntax"></a>語法


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* \[在\]
</dt> <dd>

表示要啟動之 URL 的 **字串** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法只會使用 HTTP 或 HTTPS 通訊協定來開啟網頁。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 元素，當按一下此專案時，會在新的瀏覽器視窗中顯示 Microsoft 網站。 **播放** 程式元素是以 ID = "Player" 建立。


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
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

 

 





