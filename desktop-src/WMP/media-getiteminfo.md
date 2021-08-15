---
title: GetItemInfo 方法
description: GetItemInfo 方法會抓取目前媒體專案的指定屬性值。
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab885a8505f3637d21f4a406e5a7c324ee6b9ec90e5ad0434a385e321072ccaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135151"
---
# <a name="mediagetiteminfo-method"></a>GetItemInfo 方法

**GetItemInfo** 方法會抓取目前媒體專案的指定屬性值。

## <a name="syntax"></a>語法


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **字串** ，表示指定之屬性的值。 針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。

## <a name="remarks"></a>備註

這個方法會抓取個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案。

**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性名稱數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。 可以將個別的屬性名稱傳遞給 **getItemInfo**。

若要使用具有複雜值的多個值和屬性來取得屬性，請使用 **getItemInfoByType** 方法。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

為了透過 upnp 共用 Windows 媒體程式庫，Windows Media Player 會建立內容目錄服務， (透過 upnp 公開的 cd) 。 其他裝置則可以流覽和流覽程式庫。

在 Windows 7 中，應用程式可以使用 Windows Media Player [**TrackingID**](trackingid-attribute.md)和 [**媒體**](mediatype-attribute.md)型屬性來為 cd 中的每個專案建立物件識別碼。 請注意，在未來的 Windows 版本中，此結構可能會變更。 應用程式會在 **getItemInfo** 的呼叫中，傳遞 *name* 參數中的每個屬性字串。 **getItemInfo** 會傳回傳回值中每個屬性的值。 然後，應用程式會使用下列語法來建立每個物件識別碼：

*TrackingID*。0。*MediaTypeID*

此語法具有下列意義：

-   *TrackingID* 是儲存在媒體專案的 Windows Media Player [**TrackingID**](trackingid-attribute.md)屬性中的字串。
-   *MediaTypeID* 取決於 [ [**媒體**](mediatype-attribute.md) ] 屬性的值，如下表所示：

    | 媒體屬性                      | MediaTypeID |
    |------------------------------------------|-------------|
    | [音訊專案](audio-item-attributes.md) | 4           |
    | [相片專案](photo-item-attributes.md) | B           |
    | [影片專案](video-item-attributes.md) | 8           |

    

     

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

[**GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**GetItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**SetItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**讀取屬性值**](reading-attribute-values.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





