---
title: IsAvailable
description: IsAvailable 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。 |IsAvailable
ms.assetid: d2bfaa67-eac9-4fc4-9424-636ddb4b35d6
keywords:
- IsAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Controls.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502343b7654241a00e9efb33acc6f5de842c6fb6bad650f24839a5fe7febf9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135741"
---
# <a name="controlsisavailable"></a>IsAvailable

**IsAvailable** 屬性會指出是否可以使用指定的資訊類型，或可以執行指定的動作。

``` syntax
player.controls.isAvailable(
        name
        )
```

## <a name="parameters"></a>參數

*name*

包含下列其中一個值的 **字串**。



| String          | 描述                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | 判斷使用者是否可以設定 **currentItem** 屬性。                                                                                                 |
| currentMarker   | 決定使用者是否可以搜尋特定標記。                                                                                                        |
| currentPosition | 決定使用者是否可以搜尋檔案中的特定位置。 有些檔案不支援搜尋。                                                       |
| fastForward     | 判斷檔案是否支援快速轉送以及是否可叫用該功能。 許多檔案類型 (或即時資料流) 不支援 fastForward。 |
| fastReverse     | 判斷檔案是否支援 fastReverse，以及是否可叫用該功能。 許多檔案類型 (或即時資料流) 不支援 fastReverse。     |
| 下一步            | 決定使用者是否可以搜尋播放清單中的下一個專案。                                                                                             |
| pause           | 判斷 **pause** 方法是否可用。                                                                                                             |
| 玩遊戲            | 判斷 **播放** 方法是否可用。                                                                                                              |
| previous        | 決定使用者是否可以搜尋播放清單中的上一個專案。                                                                                         |
| 步驟            | 判斷 **步驟** 方法在播放期間是否可用。                                                                                              |
| stop            | 判斷 **停止** 方法是否可用。                                                                                                              |



 

## <a name="return-values"></a>傳回值

這個方法會傳回 **布林** 值。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 元素，以搜尋目前媒體專案的開始位置。 JScript 的程式碼會使用 **isAvailable** 來驗證檔案是否支援搜尋作業。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "START"  NAME = "START"  VALUE = "Seek To Zero"

    /* If supported, seek to position zero. */
    onClick = "if (Player.controls.isAvailable('CurrentPosition'))
        Player.controls.currentPosition = 0;
">
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> </dl>

 

 





