---
title: MediaCollection. getAttributeStringCollection 方法
description: GetAttributeStringCollection 方法會抓取 StringCollection 物件，代表指定之媒體類型內指定之屬性的所有值集。
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- getAttributeStringCollection 方法 Windows Media Player
- getAttributeStringCollection 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getAttributeStringCollection 方法
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27b7c6dbef585763ecfda1abdc7beadfa3d883476033424ff868a3d56c4bb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996298"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>MediaCollection. getAttributeStringCollection 方法

**GetAttributeStringCollection** 方法會抓取 **StringCollection** 物件，代表指定之媒體類型內指定之屬性的所有值集。

## <a name="syntax"></a>語法


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

指定屬性的 **字串**。

</dd> <dt>

*媒體媒體* \[在\]
</dt> <dd>

代表媒體類型的 **字串**。 包含下列其中一個值：「音訊」、「影片」、「播放清單」或「其他」。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **StringCollection** 物件。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱[屬性參考](attribute-reference.md)一節。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *MediaCollection*。**getAttributeStringCollection** 顯示的值清單，會對應至媒體集合中音訊專案的特定屬性。 以 ID = "Attribute" 建立的 HTML SELECT 元素，可讓使用者選取屬性，例如演出者、內容類型或專輯。 以 ID = "AttributeVals" 建立的 HTML TEXTAREA 元素會顯示結果。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**StringCollection 物件**](stringcollection-object.md)
</dt> </dl>

 

 





