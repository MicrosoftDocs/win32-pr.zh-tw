---
title: LibraryLocationID
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |LibraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- LibraryLocationID Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65119db42e8a4d6a06414f1c7790fb8716c0f9423391ed0a58f74a6913cb3b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649128"
---
# <a name="externallibrarylocationid"></a>LibraryLocationID

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**LibraryLocationID** 屬性會抓取目前顯示在播放程式視圖中的特定媒體專案識別碼。

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="remarks"></a>備註

這個屬性與 [libraryLocationType](external-librarylocationtype.md) 屬性搭配使用。 例如，假設 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 等於3。 這表示 Windows Media Player 中的目前視圖顯示識別碼為3的專輯。 如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱[位置和選取的專案](location-and-selected-item.md)。

Windows Media Player 中的特定視圖會與特定媒體專案相關聯。 例如，如果目前的視圖代表個別的專輯，則 **libraryLocationType** 等於 CPAlbumID，而 **libraryLocationID** 是專輯的識別碼。 其他的視圖則不會與任何特定媒體專案相關聯。 例如，如果目前的 view 代表所有專輯， **libraryLocationType** 等於 AllCPAlbumIDs，但沒有可指派給 **libraryLocationID** 的有意義的值。 在 **libraryLocationID** 屬性沒有任何有意義的值的情況下，它等於空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**LibraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**位置和選取的專案**](location-and-selected-item.md)
</dt> </dl>

 

 





