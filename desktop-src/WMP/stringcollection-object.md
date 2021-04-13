---
title: StringCollection 物件
description: StringCollection 物件提供操作字串集合的方法。
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- StringCollection 物件 Windows Media Player
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313250"
---
# <a name="stringcollection-object"></a>StringCollection 物件

**StringCollection** 物件提供操作字串集合的方法。

**StringCollection** 物件支援下列屬性。



| 屬性                            | 描述                                             |
|-------------------------------------|---------------------------------------------------------|
| [計數](stringcollection-count.md) | 抓取字串集合中的專案數。 |



 

**StringCollection** 物件支援下列方法。



| 方法                                                                  | 描述                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](stringcollection-getattributecountbytype.md) | 抓取與指定的 **StringCollection** 專案索引、屬性名稱和語言相關聯的屬性數目。 |
| [getItemInfo](stringcollection-getiteminfo.md)                         | 抓取對應于指定之 **StringCollection** 專案索引和名稱的字串。                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | 抓取與指定的 **StringCollection** 專案索引、名稱、語言和屬性索引對應的字串。       |
| [isIdentical](stringcollection-isidentical.md)                         | 抓取值，指出提供的物件是否與目前的物件相同。                                        |
| [item](stringcollection-item.md)                                       | 抓取位於指定索引位置的字串。                                                                                    |



 

**StringCollection** 物件是透過下列方法來存取。



| Object                                        | 方法                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [MediaCollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

例如， *播放* 程式的用途。*mediaCollection*。**getAttributeStringCollection** (*屬性*， *媒體媒體*) 用於參考語法區段。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




