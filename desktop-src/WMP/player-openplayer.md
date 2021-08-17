---
title: OpenPlayer 方法
description: openPlayer 方法會使用指定的 URL 開啟 Windows Media Player。 |OpenPlayer 方法
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- openPlayer 方法 Windows Media Player
- openPlayer 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，openPlayer 方法
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42245ec29f7d7caeac17f116d1f592f74f10ba95716d5d16734ecd21bbcbb60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747566"
---
# <a name="playeropenplayer-method"></a>OpenPlayer 方法

**openPlayer** 方法會使用指定的 URL 開啟 Windows Media Player。

## <a name="syntax"></a>語法


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* \[在\]
</dt> <dd>

代表要播放之媒體專案之 URL 的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會啟動 Windows Media Player，並將指定的 URL 設定為目前的媒體專案。 如果播放程式之前是在面板模式中關閉，則會使用使用者最後選擇的面板來開啟。 否則，播放會以完整模式開啟。

如果從內嵌于遠端模式 Windows 的 Media PlayerActiveX 控制項呼叫這個方法，其行為就會與 *PlayerApplication* 相同。**switchToPlayerApplication** 方法。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlayerApplication.switchToPlayerApplication**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





