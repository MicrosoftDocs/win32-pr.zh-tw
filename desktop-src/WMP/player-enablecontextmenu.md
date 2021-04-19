---
title: EnableCoNtextMenu
description: EnableCoNtextMenu 屬性會指定或抓取值，指出是否要啟用操作功能表，這會在按下滑鼠右鍵時顯示。
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- EnableCoNtextMenu Windows Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988667"
---
# <a name="playerenablecontextmenu"></a>EnableCoNtextMenu

**EnableCoNtextMenu** 屬性會指定或抓取值，指出是否要啟用操作功能表，這會在按下滑鼠右鍵時顯示。

## <a name="syntax"></a>Syntax

*玩家*。**enableCoNtextMenu**

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入布林值。



| 值 | 描述                       |
|-------|-----------------------------------|
| true  | 預設值。 啟用內容功能表。 |
| false | 請勿啟用內容功能表。   |



 

## <a name="remarks"></a>備註

在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

**Windows Media Player 10** 行動裝置版：不支援這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





