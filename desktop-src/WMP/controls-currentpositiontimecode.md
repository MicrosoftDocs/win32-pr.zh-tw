---
title: CurrentPositionTimecode
description: CurrentPositionTimecode 屬性會使用時間碼格式來指定或抓取目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。
ms.assetid: 98d79756-c6cf-4dbc-936a-58229452451c
keywords:
- CurrentPositionTimecode Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentPositionTimecode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd0dcdf4c5337cf8dc447452ce9667c261a9c7ea4b11f98753a294bca20c6af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736538"
---
# <a name="controlscurrentpositiontimecode"></a>CurrentPositionTimecode

**CurrentPositionTimecode** 屬性會使用時間碼格式來指定或抓取目前媒體專案中的目前位置。 這個屬性目前支援 SMPTE 時間代碼。

``` syntax
player.controls.currentPositionTimecode
      
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

SMPTE 時間程式碼提供一種標準方式來識別個別的影片畫面，這對同步播放很有用。 如果數位媒體檔案支援 SMPTE 時間代碼，Windows Media Player 可以取出目前時間代碼位置資訊，或搜尋特定時間碼 **字串** 所識別的影片畫面。

SMPTE 時間代碼會依時數、分鐘數、秒數和框架數來識別特定的畫面格，以將其與特定的參考框架（指定為時間0）隔開。 通常，時間為零的框架是檔案的開頭，而特定的 SMPTE 時間代碼值代表自檔案開始以來經過的時間。

時間代碼 **字串** 的格式 \[ *範圍* 為 \] *hh*：*mm*：*ss*。*ff* 的 \[ *範圍* \] 代表範圍， *hh* 代表小時， *mm* 代表分鐘， *ss* 代表秒，而 *ff* 代表畫面格。 使用 **currentPositionTimecode** 指定值時，您必須使用零做為預留位置來包含全部八位數。

\[*範圍* \] 規範會對應至 Windows 媒體格式 **WMT 時間 \_ 碼 \_ 延伸模組 \_ 資料** 結構的 **wRange** 成員。 如需時間碼範圍的詳細資訊，請參閱 Windows 媒體格式 SDK。

只有包含 SMPTE 時間程式碼資訊的檔案才支援指定和取出 **currentPositionTimecode** 。

## <a name="examples"></a>範例

下列程式碼範例會將 **currentPositionTimecode** 指定為1小時、零分鐘、30秒和5個框架。 使用 ID = "Player" 建立 **player** 物件。


```
// Seek to a frame using SMPTE time code.
Player.controls.currentPositionTimecode = "[00000]01:00:30.05";

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> </dl>

 

 





