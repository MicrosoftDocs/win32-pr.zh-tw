---
title: WM/WMContentID 屬性
description: WM/WMContentID 屬性是識別專案內容的 GUID。
ms.assetid: 1e741286-cdd8-4c2f-8fef-5d91d81d6387
keywords:
- WM/WMContentID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f31a42a650d382597e2495d80541d667e229dde09a8181605d83cef65e39945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053756"
---
# <a name="wmwmcontentid-attribute"></a>WM/WMContentID 屬性

**WM/WMContentID** 屬性是識別專案內容的 GUID。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [CD 曲目](cd-track-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。

**WMContentID** 是此屬性的別名。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMContentID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





