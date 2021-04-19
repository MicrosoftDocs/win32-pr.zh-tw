---
title: GetItemInfoByAtom 方法
description: GetItemInfoByAtom 方法會使用指定的索引編號來抓取屬性的值。
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- getItemInfoByAtom 方法 Windows Media Player
- getItemInfoByAtom 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfoByAtom 方法
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997740"
---
# <a name="mediagetiteminfobyatom-method"></a>GetItemInfoByAtom 方法

**GetItemInfoByAtom** 方法會使用指定的索引編號來抓取屬性的值。

## <a name="syntax"></a>語法


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**Long**) 指定指定屬性位於可用屬性集合內的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，表示指定之屬性的值。 針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。

## <a name="remarks"></a>備註

這個方法可以用來使用屬性索引編號來取得特定數位媒體專案的中繼資料。 **AttributeCount** 屬性可以用來判斷媒體專案可用的屬性數目。

**MediaCollection** 物件的 **getMediaAtom** 方法也可以用來取得特定屬性的索引。 這項技術通常比使用大型播放清單時的 **getItemInfo** 或 **getItemInfoByType** 方法更有效率。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**AttributeCount**](media-attributecount.md)
</dt> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**SetItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**讀取屬性值**](reading-attribute-values.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





