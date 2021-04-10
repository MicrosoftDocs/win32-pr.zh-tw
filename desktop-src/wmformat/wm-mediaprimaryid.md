---
title: WM/MediaClassPrimaryID
description: WM/MediaClassPrimaryID 屬性包含主要媒體類別的 GUID。
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- WM/MediaClassPrimaryID windows Media 格式
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841463"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

**WM/MediaClassPrimaryID** 屬性包含主要媒體類別的 GUID。

## <a name="global-constant"></a>全域常數

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ GUID**

## <a name="remarks"></a>備註

這個屬性應該設定為下表中的其中一個值。



| 主要類別 GUID                     | Description                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | 用於音樂檔案。 請勿用於非音樂的音訊。 |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | 使用於影片檔案。                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | 用於非音樂的音訊檔案。                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | 針對非音訊或影片的檔案使用。               |



 

當您指定主要類別識別碼時，您也應該設定次要類別識別碼，以明確說明檔案中的內容類型。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




