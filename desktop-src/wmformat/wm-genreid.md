---
title: WM/GenreID
description: WM/GenreID 屬性包含與 ID3v2 中 TCON 標記內容相容的內容類型識別碼。
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- WM/GenreID windows Media 格式
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9355a16196d386d4ec3f2a98588eced2981f8e62a3df96a9c0d094551a10a733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930438"
---
# <a name="wmgenreid"></a>WM/GenreID

**WM/GenreID** 屬性包含與 ID3V2 中 TCON 標記內容相容的內容類型識別碼。 這應該會在括弧中包含內容類型識別碼，並選擇性地接著進一步描述內容類型。 如需詳細資訊，請參閱 ID3v2 規格。

## <a name="global-constant"></a>全域常數

g \_ wszWMGenreID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

用來指定類型的慣用屬性為 [**WM/**](wm-genre.md)內容類型。 將其用於此屬性的喜好設定。

如果您變更了 MP3 檔中的 **wm/** 內容類型或 **wm/GenreID** ，其他屬性將會變更為 [符合]。

### <a name="example"></a>範例



| 檔案類型 | 範例值   |
|-----------|-----------------|
| 音訊     | " (4) Eurodisco" |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




