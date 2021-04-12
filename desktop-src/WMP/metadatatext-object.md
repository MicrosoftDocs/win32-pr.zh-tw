---
title: MetadataText 物件
description: MetadataText 物件提供一種方式，來取得複雜文字中繼資料屬性的中繼資料。
ms.assetid: cf8e4524-6fc5-4534-9542-6bdc7d34bca4
keywords:
- MetadataText 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MetadataText Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b043a9050d03ca562159aa5be0c113084ac152fb
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2019
ms.locfileid: "104373455"
---
# <a name="metadatatext-object"></a>MetadataText 物件

**MetadataText** 物件提供一種方式，來取得複雜文字中繼資料屬性的中繼資料。

**MetadataText** 物件支援下列屬性。



| 屬性                                    | 描述                                   |
|---------------------------------------------|-----------------------------------------------|
| [description](metadatatext-description.md) | 捕獲中繼資料文字的描述。 |
| [text](metadatatext-text.md)               | 捕獲中繼資料文字。                  |



 

**MetadataText** 物件是透過下列方法來存取。



| Object                    | 方法                                           |
|---------------------------|--------------------------------------------------|
| [媒體](media-object.md) | [getItemInfoByType](media-getiteminfobytype.md) |



 

例如， *播放* 程式的用途。*currentMedia*。**getItemInfoByType** (*name*、 *language*、 *index*) 用於參考語法區段中。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




