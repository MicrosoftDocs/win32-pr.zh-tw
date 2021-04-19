---
title: PlaySound
description: PlaySound 方法會播放指定的音效檔。
ms.assetid: 42675a66-0139-4e74-9abe-1b42017fc6fe
keywords:
- PlaySound Windows Media Player
topic_type:
- apiref
api_name:
- THEME.playSound
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ceb30e5c47632a1358262019124fceae056294d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990638"
---
# <a name="themeplaysound"></a>PlaySound

**PlaySound** 方法會播放指定的音效檔。

``` syntax
        theme.playSound(soundFile)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="soundFile"></span><span id="soundfile"></span><span id="SOUNDFILE"></span>*soundFile*
</dt> <dd>

**字串**，指定要播放的音效檔名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此方法可讓您將音效效果新增至面板，例如，按一下按鈕時。 音效是由作業系統直接播放，而不是 Windows Media Player。 這表示音效無法利用 Windows Media Player 設定和方法來控制，但可以在 Windows Media Player 播放另一個數位媒體檔案時播放。

這個方法僅支援 WAV 檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**主題元素**](theme-element.md)
</dt> </dl>

 

 





