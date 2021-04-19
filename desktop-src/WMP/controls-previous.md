---
title: Controls。 previous 方法
description: 先前的方法會將目前的專案設定為播放清單中的上一個專案。
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- 上一個方法 Windows Media Player
- 上一個方法 Windows Media Player，Controls 類別
- 控制項類別 Windows Media Player、上一個方法
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981306"
---
# <a name="controlsprevious-method"></a>Controls。 previous 方法

**先前** 的方法會將目前的專案設定為播放清單中的上一個專案。

## <a name="syntax"></a>語法


```JScript
Controls.previous()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果播放清單是在叫用 **先前** 的第一個專案時，播放清單中的最後一個專案會成為目前的專案。

## <a name="examples"></a>範例

下列範例會建立 HTML BUTTON 專案，使用 [ **上一步** ] 移至目前播放清單中的上一個專案。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
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

[**控制項。下一步**](controls-next.md)
</dt> <dt>

[**控制項。停止**](controls-stop.md)
</dt> </dl>

 

 





