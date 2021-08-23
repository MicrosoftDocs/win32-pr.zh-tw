---
title: LibraryLocationType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |LibraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- LibraryLocationType Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736198"
---
# <a name="externallibrarylocationtype"></a>LibraryLocationType

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**LibraryLocationType** 屬性會抓取連結 [庫位置常數](library-location-constants.md)，指出 Windows Media Player 中目前視圖的型別。

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，其中包含其中一個程式庫位置常數。

## <a name="remarks"></a>備註

這個屬性與 [libraryLocationID](external-librarylocationid.md) 屬性搭配使用。 例如，假設 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 等於3。 這表示 Windows Media Player 中的目前視圖顯示識別碼為3的專輯。 如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱[位置和選取的專案](location-and-selected-item.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**LibraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**位置和選取的專案**](location-and-selected-item.md)
</dt> </dl>

 

 





