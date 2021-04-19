---
title: GetItemInfoByType 方法
description: GetItemInfoByType 方法會抓取對應到指定屬性名稱、語言和索引的屬性值。
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- getItemInfoByType 方法 Windows Media Player
- getItemInfoByType 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfoByType 方法
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984846"
---
# <a name="mediagetiteminfobytype-method"></a>GetItemInfoByType 方法

**GetItemInfoByType** 方法會抓取對應到指定屬性名稱、語言和索引的屬性值。

## <a name="syntax"></a>語法


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

</dd> <dt>

*語言* \[在\]
</dt> <dd>

表示語言的 **字串**。 如果值設定為 null 或 "" (空字串) 會使用目前的地區設定字串。 否則，此值必須是有效的 RFC 1766 語言字串，例如 "en-us"。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

**Number** (**Long**) ，其中包含要從屬性中取出之值的以零為起始的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **數位**、 **字串**、 **MetadataPicture** 物件或 **MetadataText** 物件，如下表所示。



| 屬性                   | 傳回值                   |
|-----------------------------|--------------------------------|
| **SyncState**               | **數位** (不 **帶正負** 號的 long)  |
| **WM/歌詞 \_ 內容** | **MetadataText** 物件        |
| **WM/圖片**              | **MetadataPicture** 物件     |
| **WM/UserWebURL**           | **MetadataText** 物件        |
| 所有其他屬性        | **String**                     |



 

若為其基礎值為 **布林** 值的屬性，這個方法會傳回字串 "true" 或 "false"。

## <a name="remarks"></a>備註

這個方法會抓取個別數位媒體專案的中繼資料，或屬於播放清單一部分的媒體專案。

這個方法支援具有多個值的屬性和具有複雜值的屬性。 **GetItemInfo** 方法不支援具有多個值的屬性和具有複雜值的屬性。

**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性名稱數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷每個可用屬性的名稱。 您可以將個別的屬性名稱傳遞給 **getItemInfoByType** 的 *name* 參數。

**GetAttributeCountByType** 方法會傳回對應至指定 **媒體** 物件之特定屬性名稱的屬性數目。 然後，您可以將索引編號傳遞給 **getItemInfoByType** 的 *index* 參數。 例如，當數位媒體專案分類為多個內容（例如）時，這非常有用。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

這個方法可能會造成錯誤。 當您呼叫這個方法時，應該包含錯誤處理常式代碼。 例如，在 JScript 中，您可以使用 [try ...] 來執行錯誤處理。 **抓住。。。finally** 結構。

**Windows Media Player 10** 行動裝置版：不支援這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**AttributeCount**](media-attributecount.md)
</dt> <dt>

[**GetAttributeCountByType**](media-getattributecountbytype.md)
</dt> <dt>

[**GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**SetItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MetadataPicture 物件**](metadatapicture-object.md)
</dt> <dt>

[**MetadataText 物件**](metadatatext-object.md)
</dt> <dt>

[**讀取屬性值**](reading-attribute-values.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





