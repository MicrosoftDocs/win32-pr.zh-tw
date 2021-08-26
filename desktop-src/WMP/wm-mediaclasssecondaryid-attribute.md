---
title: WM/MediaClassSecondaryID 屬性
description: WM/MediaClassSecondaryID 屬性是指定次要媒體類別的 GUID，這是主要媒體類別的子類別。
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- WM/MediaClassSecondaryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9582fc3db713b8db945ec17534f1dc9c951402eea88489285526d6a3cfbdf147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000988"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>WM/MediaClassSecondaryID 屬性

**WM/MediaClassSecondaryID** 屬性是指定次要媒體類別的 GUID，這是主要媒體類別的子類別。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)
-   [其他專案](other-item-attributes.md)
-   [相片專案](photo-item-attributes.md)
-   [播放清單](playlist-attributes-ref.md)
-   [單選項目](radio-item-attributes.md)
-   [影片專案](video-item-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在文件庫和數位媒體檔案中。

下表列出支援的 Guid 及其描述。



| GUID                                 | 描述                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | 媒體物件代表靜態播放清單。 |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | 媒體物件代表自動播放清單。  |



 

**MediaClassSecondaryID** 是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMMediaClassSecondaryID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | 只有 Windows Media Player 10 或更新版本才支援相片專案。只有 Windows Media Player 9 系列支援 Windows Media Player 9 系列和更新版本中的所有其他專案<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





