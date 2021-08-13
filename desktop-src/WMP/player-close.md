---
title: Player. close 方法
description: close 方法會釋放 Windows Media Player 資源。
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- close 方法 Windows Media Player
- close 方法 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，close 方法
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29e68aed11b095dff80c8c91c88410f98b9a236bbcadcbff75da0fc0de392fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467878"
---
# <a name="playerclose-method"></a>Player. close 方法

**close** 方法會釋放 Windows Media Player 資源。

## <a name="syntax"></a>語法


```JScript
Player.close()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會關閉目前的數位媒體檔案，而不是 Windows Media Player 本身。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 元素，當按下時，會在 Windows Media Player 中停止播放，並釋放使用中的資源。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
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

 

 





