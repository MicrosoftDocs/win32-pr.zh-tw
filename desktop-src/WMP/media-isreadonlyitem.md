---
title: IsReadOnlyItem 方法
description: IsReadOnlyItem 方法會傳回值，指出是否可以編輯媒體專案的指定屬性。
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- isReadOnlyItem 方法 Windows Media Player
- isReadOnlyItem 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isReadOnlyItem 方法
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997437"
---
# <a name="mediaisreadonlyitem-method"></a>IsReadOnlyItem 方法

**IsReadOnlyItem** 方法會傳回值，指出是否可以編輯媒體專案的指定屬性。

## <a name="syntax"></a>語法


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

表示要測試之屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林值**。

## <a name="remarks"></a>備註

如果屬性是唯讀的，則無法使用 **setItemInfo** 方法來設定它。 請注意，使用不同版本的 Windows Media Player 時，這個方法可能會針對特定屬性傳回不同的值。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**Windows Media Player 10** 行動裝置版：這個屬性一律會傳回 **true**。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**isReadOnlyItem** ，以目前媒體專案的相關資訊填入名為 RWTEXT 的 HTML TEXTAREA 元素。 程式碼會輸出目前媒體專案的每個屬性，以及指出屬性為唯讀還是讀取/寫入的文字。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**SetItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





