---
title: MarkerCount
description: MarkerCount 屬性會抓取媒體專案中的標記數目。
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- MarkerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987171"
---
# <a name="mediamarkercount"></a>MarkerCount

**MarkerCount** 屬性會抓取媒體專案中的標記數目。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**markerCount**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 指定檔案中的標記數目。

## <a name="remarks"></a>備註

如果檔案沒有標記，或媒體專案與 *播放* 程式不同，則這個屬性會傳回零。**currentMedia**。

標記數位從1開始。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**markerCount** ，以取得目前媒體專案中的標記數目。 該值接著會用來做為迴圈結構的上限，這會逐一查看標記清單來取出每個標記名稱。 名為 MNAMES 的 HTML TEXTAREA 元素會顯示目前媒體專案中的標記名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

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

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





