---
title: FastForward 方法
description: FastForward 方法會以正向方向啟動媒體專案的快速播放。 |FastForward 方法
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- fastForward 方法 Windows Media Player
- fastForward 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，fastForward 方法
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341814"
---
# <a name="controlsfastforward-method"></a>FastForward 方法

**FastForward** 方法會以正向方向啟動媒體專案的快速播放。

## <a name="syntax"></a>語法


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**FastForward** 方法會以正常速度的五倍來播放剪輯。 叫用 **fastForward** 會變更 *設定*。**rate** 屬性為5.0。 如果之後變更了 **速率**，或呼叫了 **播放** 或 **停止**，Windows Media Player 將會停止快速轉送。

**FastForward** 方法不適用於即時廣播和特定媒體類型。 若要判斷您是否可以在剪輯中向前快轉，請呼叫 **isAvailable** ( "FastForward" ) 。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，以使用 **fastForward** 來啟動媒體專案的快速播放。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**IsAvailable**](controls-isavailable.md)
</dt> <dt>

[**控制項. play**](controls-play.md)
</dt> <dt>

[**控制項。停止**](controls-stop.md)
</dt> <dt>

[**設定。速率**](settings-rate.md)
</dt> </dl>

 

 





