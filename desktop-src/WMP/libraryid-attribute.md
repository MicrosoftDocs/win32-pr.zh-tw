---
title: LibraryID 屬性
description: LibraryID 屬性是專案所屬程式庫的識別碼。
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- LibraryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989802"
---
# <a name="libraryid-attribute"></a>LibraryID 屬性

**LibraryID** 屬性是專案所屬程式庫的識別碼。

## <a name="applies-to"></a>套用至

-   [**音訊專案**](audio-item-attributes.md)
-   [**相片專案**](photo-item-attributes.md)
-   [**播放清單專案**](playlist-attributes-ref.md)
-   [**影片專案**](video-item-attributes.md)

## <a name="remarks"></a>備註

媒體專案可能屬於目前使用者的本機文件庫，或可能屬於家用網路或網際網路上的另一位使用者所提供的程式庫。

這個屬性的值與 [**IWMPLibrary2：： getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) 方法所傳回的值相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------|
| 版本<br/> | Windows Media Player 12<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性參考**](attribute-reference.md)
</dt> </dl>

 

 





