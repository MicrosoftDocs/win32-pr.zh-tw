---
title: WM/Year 屬性
description: WM/Year 屬性是發佈內容的年份。
ms.assetid: b64e37f1-6f12-43a6-8a66-7d61b470853c
keywords:
- WM/Year 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Year
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0b76fbf54a53a7ae09728fe34d75fff5c232de9ecfa13a77edaa97cd37e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900188"
---
# <a name="wmyear-attribute"></a>WM/Year 屬性

**WM/Year** 屬性是發佈內容的年份。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用 Windows 媒體檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在數位媒體檔案中。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

這個屬性不應該當做查詢準則的一部分使用。 它是衍生自另一個屬性，而且無法在媒體集合中直接查詢。

這個屬性的 Windows 媒體格式 SDK 常數是 g \_ wszWMYear。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列 Windows Media Player 10 或更新版本不支援此屬性<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





