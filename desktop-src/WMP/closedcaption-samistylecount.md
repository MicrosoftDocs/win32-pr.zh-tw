---
title: ClosedCaption.SAMIStyleCount
description: SAMIStyleCount 屬性會抓取目前的薩米文檔案所支援的樣式數目。
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- ClosedCaption. SAMIStyleCount Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999103"
---
# <a name="closedcaptionsamistylecount"></a>ClosedCaption.SAMIStyleCount

**SAMIStyleCount** 屬性會抓取目前的薩米文檔案所支援的樣式數目。

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

在 (*播放機* 開啟數位媒體檔案之前，無法使用此方法。**openState** 等於13個) 。

**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





