---
title: GetMarkerTime 方法
description: GetMarkerTime 方法會抓取位於指定索引處之標記的時間。
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- getMarkerTime 方法 Windows Media Player
- getMarkerTime 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getMarkerTime 方法
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000942"
---
# <a name="mediagetmarkertime-method"></a>GetMarkerTime 方法

**GetMarkerTime** 方法會抓取位於指定索引處之標記的時間。

## <a name="syntax"></a>語法


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*markerNum* \[在\]
</dt> <dd>

指定標記索引的 **數位** (**long**) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位** (**雙精度**) 指定從剪輯開頭開始的標記位置（以秒為單位）。

## <a name="remarks"></a>備註

如果指定的標記不存在，這個方法會傳回 **Null** 。

某些數位媒體專案不包含標記。 使用 **markerCount** 來找出目前剪輯中有多少標記。

標記索引編號從1開始。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**getMarkerTime** ，以每個標記的位置填入名為 MTIMES 的 HTML TEXTAREA 元素。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
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

[**GetMarkerName**](media-getmarkername.md)
</dt> <dt>

[**MarkerCount**](media-markercount.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





