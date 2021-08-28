---
title: GetMarkerName 方法
description: GetMarkerName 方法會在指定的索引處，抓取標記的名稱。
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- getMarkerName 方法 Windows Media Player
- getMarkerName 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getMarkerName 方法
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1ace88a7012ec59bf4dcae32c5c2f51f240dd1e59c58408165392a6fc1e616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123398"
---
# <a name="mediagetmarkername-method"></a>GetMarkerName 方法

**GetMarkerName** 方法會在指定的索引處，抓取標記的名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*markerNum* \[在\]
</dt> <dd>

指定標記索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串**。

## <a name="remarks"></a>備註

如果指定的標記不存在，這個方法會傳回 **Null** 。

某些數位媒體專案不包含標記。 使用 **markerCount** 來找出目前剪輯中有多少標記。

標記索引編號從1開始。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**getMarkerName** ，以目前媒體專案中的標記名稱填入名為 MNAMES 的 HTML TEXTAREA 元素。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
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

[**GetMarkerTime**](media-getmarkertime.md)
</dt> <dt>

[**MarkerCount**](media-markercount.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





