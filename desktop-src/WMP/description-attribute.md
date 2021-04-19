---
title: 'Description 屬性 (WMP SDK) '
description: Description 屬性是內容的描述。
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Description 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994214"
---
# <a name="description-attribute"></a>Description 屬性

**Description** 屬性是內容的描述。

## <a name="applies-to"></a>套用至

-   [音樂檔案](music-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性會儲存在音樂檔案中，而不是儲存在文件庫中。

這個屬性可以有多個值。 若要取得多重值屬性的所有值，您必須使用 *媒體*。**getItemInfoByType** 方法，而不 *是 getItemInfo* 方法。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMDescription。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





