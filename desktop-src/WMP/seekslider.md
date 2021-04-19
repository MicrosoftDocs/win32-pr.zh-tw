---
title: SEEKSLIDER
description: 這是具有下列預設值的預先定義滑杆。 |SEEKSLIDER
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SEEKSLIDER Windows Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978630"
---
# <a name="seekslider"></a>SEEKSLIDER

這是具有下列預設值的預先定義 **滑杆** 。

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a>備註

這會建立 **滑動** 軸控制項，將媒體檔案搜尋至任何位置。 工具提示已當地語系化。 此 **滑杆** 的所有屬性都可以藉由明確指定來覆寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> </dl>

 

 





