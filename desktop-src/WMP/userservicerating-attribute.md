---
title: UserServiceRating 屬性
description: UserServiceRating 屬性已保留供日後使用。
ms.assetid: e6113474-725d-4eb1-9c05-cff7749f2010
keywords:
- UserServiceRating 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- UserServiceRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690a090aaa9d07ee850caee004242272368129f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992370"
---
# <a name="userservicerating-attribute"></a>UserServiceRating 屬性

**UserServiceRating** 屬性已保留供日後使用。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

使用者評等是以整數值表示，如下表所述。 指定值時，請使用 [寫入值] 資料行中的其中一個值。 在抓取值時，您可以使用 [讀取值] 資料行中的範圍來決定星星數目。



| 分級  | 寫入值 | 讀取值 |
|---------|---------------|----------------|
| 評分 | 0             | 0              |
| 1 顆星  | 1             | 1 到 12        |
| 2 顆星 | 25            | 13到37       |
| 3 顆星 | 50            | 38至62       |
| 4 顆星 | 75            | 63至86       |
| 5 顆星 | 99            | 87至99       |



 

這個屬性只會儲存在程式庫中。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





