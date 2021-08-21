---
title: AlternateSourceURL 屬性
description: AlternateSourceURL 屬性是媒體專案的統一資源定位器，可做為 DLNASourceURI 和 SourceURL 屬性的替代專案。
ms.assetid: 2be88d9b-4fd8-4e70-9a4d-114a2bf8b23c
keywords:
- AlternateSourceURL 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- AlternateSourceURL Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765c7a3945224e82a0112c0f4dd7249e4340ec13e0d78adbd59039d25f234aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055236"
---
# <a name="alternatesourceurl-attribute"></a>AlternateSourceURL 屬性

**AlternateSourceURL** 屬性是媒體專案的統一資源定位器，可做為 [**DLNASourceURI**](dlnasourceuri-attribute.md)和 [**SourceURL**](sourceurl-attribute.md)屬性的替代專案。

## <a name="applies-to"></a>套用至

-   [**音訊專案**](audio-item-attributes.md)
-   [**相片專案**](photo-item-attributes.md)
-   [**播放清單專案**](playlist-attributes-ref.md)
-   [**影片專案**](video-item-attributes.md)

## <a name="remarks"></a>備註

目前使用者的本機文件庫中的媒體專案無法使用這個屬性。 它僅適用于屬於遠端媒體櫃的媒體專案;也就是，由家用網路上的另一位使用者所提供的程式庫。 若要判斷媒體櫃是否為遠端，請呼叫 [**IWMPLibrary：： get \_ 類型**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





