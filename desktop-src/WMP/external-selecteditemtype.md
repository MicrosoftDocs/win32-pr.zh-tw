---
title: SelectedItemType
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |SelectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- SelectedItemType Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977151"
---
# <a name="externalselecteditemtype"></a>SelectedItemType

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**SelectedItemType** 屬性會抓取 Windows Media Player 中目前選取之媒體專案的類型。

## <a name="syntax"></a>Syntax

selectedItemType () 

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串** ，其中包含其中一個連結 [庫位置常數](library-location-constants.md)。

## <a name="remarks"></a>備註

這個屬性會與 **selectedItemID** 屬性搭配使用。 例如，如果 **selectedItemType** 等於 CPTrackID，則 **selectedItemID** 是所選播放軌的識別碼。如需 Windows Media Player 如何讓線上商店內容的觀點有詳細的詳細資訊，請參閱 [位置和選取的專案](location-and-selected-item.md)。

Windows Media Player 中的特定視圖會有選取的特定媒體專案。 例如，假設目前的 view 代表專輯。 專輯是曲目的容器，因此 **selectedItemType** 等於 CPTrackID，而 **selectedItemID** 是所選播放軌的識別碼。其他視圖則沒有選取的媒體專案。 例如，如果使用者按一下 [樹狀檢視] 控制項中的線上商店根節點，Windows Media Player 會顯示線上商店所提供的 [探索] 頁面。 播放程式不會在播放程式使用者介面中顯示任何媒體專案的容器。 在此情況下， **selectedItemType** 等於 unknownlocation.xsd，而 **selectedItemID** 等於空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**SelectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**位置和選取的專案**](location-and-selected-item.md)
</dt> </dl>

 

 





