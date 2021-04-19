---
title: OpenPlayer 方法
description: OpenPlayer 方法會使用指定的 URL 開啟 Windows Media Player。 |OpenPlayer 方法
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
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989566"
---
# <a name="playeropenplayer-method"></a>OpenPlayer 方法

**OpenPlayer** 方法會使用指定的 URL 開啟 Windows Media Player。

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

如果從內嵌于遠端模式的 Windows Media PlayerActiveX 控制項呼叫這個方法，其行為就會與 *PlayerApplication* 相同。**switchToPlayerApplication** 方法。

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

 

 





