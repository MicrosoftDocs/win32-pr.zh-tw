---
title: 'IWMPMetadataPicture (VB 和 C ) 介面 (Wmp. h) '
description: 提供屬性，以取得以 WM/Picturemetadata 屬性工作表示之數位媒體檔案中包含之影像的相關資訊。
ms.assetid: f8260882-dfb8-4ff0-954c-5060cb7a6995
keywords:
- IWMPMetadataPicture (VB 和 C ) 介面 Windows Media Player
- IWMPMetadataPicture (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMetadataPicture (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b73a48b2ea93d696f2b8780edec90dfcf0522e2353c508e31d96dd7a404d0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996488"
---
# <a name="iwmpmetadatapicture-vb-and-c-interface"></a>IWMPMetadataPicture (VB 和 c # ) 介面

提供屬性，以取得以 [**WM/圖片**](/windows/desktop/wmformat/wmpicture)中繼資料屬性工作表示之數位媒體檔案中包含之影像的相關資訊。 這個屬性會對應至數位媒體檔案中包含的專輯封面影像，而不是透過網際網路下載的專輯封面。

**IWMPMetadataPicture** 介面會公開下列屬性。



| 屬性                                                                                   | 描述                                                               |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**描述**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-description--vb-and-c.md) | 取得中繼資料屬性所代表之影像的描述。  |
| [**mimeType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-mimetype--vb-and-c.md)       | 取得中繼資料屬性所代表之影像的 MIME 類型。    |
| [**pictureType**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-picturetype--vb-and-c.md) | 取得中繼資料屬性所代表之影像的圖片類型。 |
| [**URL**](wmplibiwmpmetadatapicture-iwmpmetadatapicture-url--vb-and-c.md)                 | 僅供內部使用。                                                        |



 

取得 **IWMPMetadataPicture** 介面，方法是將屬性名稱 [**WM/圖片**](/windows/desktop/wmformat/wmpicture) 傳入下列方法，並轉換傳回的物件。



| 介面                                  | 屬性                                                                             |
|--------------------------------------------|--------------------------------------------------------------------------------------|
| [**IWMPMedia3**](iwmpmedia3--vb-and-c.md) | [**getItemInfoByType**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md) |



 

## <a name="members"></a>成員

**IWMPMetadataPicture (VB 和 c # )** 介面不會定義任何成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .net 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

