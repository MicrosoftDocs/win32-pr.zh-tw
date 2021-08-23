---
title: IsRemote
description: isRemote 屬性會抓取值，指出 Windows Media Player 控制項是否在遠端模式中執行。
ms.assetid: bfeab968-affb-4d5d-b88b-5caf50d34cee
keywords:
- IsRemote Windows Media Player
topic_type:
- apiref
api_name:
- Player.isRemote
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afa0caf615563f4829f1a337f31521b1fb7dafd5ef6e2722f1d50c01dda1ba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616688"
---
# <a name="playerisremote"></a>IsRemote

**isRemote** 屬性會抓取值，指出 Windows Media Player 控制項是否在遠端模式中執行。

## <a name="syntax"></a>Syntax

*玩家* 。**isRemote**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **布林值**。



| 值 | 描述                                   |
|-------|-----------------------------------------------|
| true  | 播放機控制項以遠端模式執行。 |
| false | 播放機控制項是在原生模式中執行。  |



 

## <a name="remarks"></a>備註

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回 false。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





