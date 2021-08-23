---
title: MetadataPicture 物件
description: MetadataPicture 物件會提供一種方式來取出 WM/圖片中繼資料屬性的值。 這個屬性會對應至包含在數位媒體檔案中的專輯封面，而不是透過網際網路下載的專輯封面。
ms.assetid: c0d6f43d-1a88-4ac2-a7b3-c502f4d57afb
keywords:
- MetadataPicture 物件 Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 261ed17a156e1b5563b52744490e2ed014803eb9f1e75c182f44d5bd228b11c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996208"
---
# <a name="metadatapicture-object"></a>MetadataPicture 物件

**MetadataPicture** 物件會提供一種方式來取出 [**WM/圖片**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)中繼資料屬性的值。 這個屬性會對應至包含在數位媒體檔案中的專輯封面，而不是透過網際網路下載的專輯封面。

**MetadataPicture** 物件支援下列屬性。



| 屬性                                           | 描述                                       |
|----------------------------------------------------|---------------------------------------------------|
| [**描述**](metadatapicture-description.md) | 捕獲中繼資料影像的描述。    |
| [**mimeType**](metadatapicture-mimetype.md)       | 捕獲中繼資料影像的 MIME 類型。    |
| [**pictureType**](metadatapicture-picturetype.md) | 捕獲中繼資料影像的圖片類型。 |
| [**URL**](metadatapicture-url.md)                 | 僅供內部使用。                                |



 

**MetadataPicture** 物件是透過下列方法來存取。



| Object                        | 方法                                               |
|-------------------------------|------------------------------------------------------|
| [**媒體**](media-object.md) | [**getItemInfoByType**](media-getiteminfobytype.md) |



 

為了方便說明， `player.currentMedia.getItemInfoByType(name, language, index)` 在參考語法區段中使用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 