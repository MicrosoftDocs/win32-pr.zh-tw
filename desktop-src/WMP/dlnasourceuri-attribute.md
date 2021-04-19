---
title: DLNASourceURI 屬性
description: DLNASourceURI 屬性是專案 (URI) 的通用資源識別碼。
ms.assetid: 323c897b-9b76-44f7-9313-c51595589583
keywords:
- DLNASourceURI 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- DLNASourceURI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ebe21a39a67dec9356c5dd5360efb48f4ef029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982580"
---
# <a name="dlnasourceuri-attribute"></a>DLNASourceURI 屬性

**DLNASourceURI** 屬性是專案 (URI) 的通用資源識別碼。

## <a name="applies-to"></a>套用至

-   [**音訊專案**](audio-item-attributes.md)
-   [**其他專案**](other-item-attributes.md)
-   [**相片專案**](photo-item-attributes.md)
-   [**播放清單專案**](playlist-attributes-ref.md)
-   [**影片專案**](video-item-attributes.md)

## <a name="remarks"></a>備註

如果專案是在目前使用者的本機文件庫中，則這個屬性、 [**SourceURL**](sourceurl-attribute.md) 屬性以及 [**IWMPMedia：： get \_ SourceURL**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_sourceurl) 所傳回的值全都相同。

如果專案不在目前使用者的本機文件庫中，但屬於遠端程式庫，此屬性就是 playsingle：//*xxx* 格式的識別碼。

您可以將 playsingle URI 傳遞至 [**IWMPCore3：： newMedia**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore3-newmedia) 方法，以取得可讓您查看媒體專案中繼資料的 [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) 介面，並可能會編輯媒體專案的星級評等。 不過請注意，playsingle URI 必須是 Windows Media Player 已經探索到的內容目錄服務 (CD) 。 **NewMedia** 方法不會起始 UPnP 探索並搜尋 cd。

只有在遠端程式庫支援編輯作業時，您才可以編輯遠端媒體櫃中媒體專案的星星評等。 在執行 Windows 7 的電腦上主控的遠端程式庫支援編輯作業。 在執行 windows 7 之前 Windows 作業系統的電腦上裝載的遠端程式庫不支援編輯作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





