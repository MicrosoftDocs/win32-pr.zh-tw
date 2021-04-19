---
title: 設定。靜音
description: '[靜音] 屬性會指定並抓取值，指出音訊是否為靜音。'
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- 設定。靜音 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989582"
---
# <a name="settingsmute"></a>設定。靜音

[ **靜音** ] 屬性會指定並抓取值，指出音訊是否為靜音。

## <a name="syntax"></a>Syntax

播放的設定。靜音

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **布林值**。



| 值 | 描述                  |
|-------|------------------------------|
| true  | 音訊已靜音。              |
| false | 預設值。 音訊未靜音。 |



 

## <a name="examples"></a>範例

下列範例會建立一個 HTML CHECKBOX 元素，讓使用者可以將音訊靜音並取消靜音。 使用 ID = "Player" 建立 **player** 物件。


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





