---
title: ClosedCaption.SAMIFileName
description: SAMIFileName 屬性會指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- ClosedCaption. SAMIFileName Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984012"
---
# <a name="closedcaptionsamifilename"></a>ClosedCaption.SAMIFileName

**SAMIFileName** 屬性會指定或抓取包含隱藏式輔助字幕所需資訊的檔案名。

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

已同步處理的可存取媒體交換 (薩米) 檔案必須使用 smi-s 或薩米文的副檔名。

如果您未指定 **SAMIFileName** 的值，此屬性會抓取包含與目前媒體專案相關聯之檔案名或 URL 的字串。 當您使用 *薩米* 文 URL 參數指定薩米文的檔案時，或當薩米文的檔案與數位媒體檔案名 (（副檔名) 除外）時，就可能會發生此關聯。 如果目前的媒體沒有相關聯的薩米文檔案，這個屬性會 )  ( 的空字串。

一旦您指定 **SAMIFileName** 的值，該值就會持續，直到您指定新值為止 (或直到使用 *薩米* 文 URL 參數) 開啟新的媒體專案為止。 因此，在播放每個新媒體專案之前，您必須為這個屬性指定新的值。 如此一來，當下一個媒體專案 (或 *播放* 程式開啟時， **SAMIFileName** 的新值就會生效。**close** 稱為) 。 為 **SAMIFileName** 指定新的值對目前的媒體沒有任何作用。

若要使 Windows Media Player 使用與特定媒體專案相關聯的薩米文檔案傳回，請在播放下一個媒體專案之前，指定 **SAMIFileName** 等於空字串 ( "" ) 的值。

**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。

## <a name="examples"></a>範例

下列三個 JScript 範例使用 *ClosedCaption*。**SAMIFileName** 指定隱藏式輔助字幕文字檔的名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> <dt>

[**Player. 關閉**](player-close.md)
</dt> </dl>

 

 





