---
title: 設定. defaultFrame
description: DefaultFrame 屬性會指定或抓取用來顯示 ScriptCommand 事件中所接收之 URL 的框架名稱。
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- 設定. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984060"
---
# <a name="settingsdefaultframe"></a>設定. defaultFrame

**DefaultFrame** 屬性會指定或抓取用來顯示 **ScriptCommand** 事件中所接收之 URL 的框架名稱。

## <a name="syntax"></a>Syntax

defaultFrame

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串** ，對應至目標框架元素的 **name** 屬性值。

## <a name="remarks"></a>備註

如果在 **ScriptCommand** 事件本身指定了目標框架，則會忽略這個屬性。

使用 JAVA applet Netscape Navigator 時，會忽略這個屬性。 在 [導覽器] 中，每個收到的 URL 指令碼命令都會在新的瀏覽器視窗中顯示 URL，不論 *設定* 的值為何。**defaultFrame**。

**Windows Media Player 10** 行動裝置版：此屬性是唯讀的，而且一律會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ScriptCommand 事件**](player-player-scriptcommand.md)
</dt> <dt>

[**Settings 物件**](settings-object.md)
</dt> <dt>

[**使用 Windows Media Player 搭配 Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





