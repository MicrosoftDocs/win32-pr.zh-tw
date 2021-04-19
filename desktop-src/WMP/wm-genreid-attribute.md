---
title: WM/GenreID 屬性
description: WM/GenreID 屬性是符合 ID3v2 中 TCON 標記的內容類型識別碼。
ms.assetid: 9b68f9be-1f02-4b14-b052-90657b8800e3
keywords:
- WM/GenreID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d31e54805f778a51f345c84654056391ec4052e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000765"
---
# <a name="wmgenreid-attribute"></a>WM/GenreID 屬性

**WM/GenreID** 屬性是符合 ID3V2 中 TCON 標記的內容類型識別碼。

## <a name="applies-to"></a>套用至

-   [音訊專案](audio-item-attributes.md)
-   [常用的 Windows Media 檔案屬性](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>備註

這個屬性只會儲存在數位媒體檔案中。

ID3 第2版是一種標記慣例，原本是針對 MP3 所設計。 如需詳細資訊，請參閱 [ID3 組織的網站](https://id3.org/)。

這個屬性的 Windows Media Format SDK 常數是 g \_ wszGenreID。

若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列 Windows Media Player 10 或更新版本不支援此屬性<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





