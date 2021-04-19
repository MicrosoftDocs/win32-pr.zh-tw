---
title: DurationString
description: DurationString 屬性會抓取字串值，指出目前媒體專案的持續時間（以 HH MM SS 格式表示）。
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- DurationString Windows Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983154"
---
# <a name="mediadurationstring"></a>DurationString

**DurationString** 屬性會抓取 **字串** 值，以 HH： MM： SS 格式指出目前媒體專案的持續時間。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**durationString**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

如果這個屬性與 media 專案一起使用，而不是 *播放* 程式中指定的媒體專案。**currentMedia**，它可能不包含有效的值。 如果媒體專案的長度不到一小時，則會省略傳回值的 HH：部分。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**durationString** ，以格式化的文字顯示目前媒體專案的持續時間。 名為 Mediainfo.xml 的 HTML DIV 元素會顯示持續時間資訊。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**Media. duration**](media-duration.md)
</dt> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





