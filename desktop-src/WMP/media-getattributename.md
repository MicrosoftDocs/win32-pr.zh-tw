---
title: GetAttributeName 方法
description: GetAttributeName 方法會抓取對應于指定索引之屬性的名稱。
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- getAttributeName 方法 Windows Media Player
- getAttributeName 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getAttributeName 方法
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b9a288830283b3711c6e4eb652be968979628af48d2ce5b718150b9018568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123428"
---
# <a name="mediagetattributename-method"></a>GetAttributeName 方法

**GetAttributeName** 方法會抓取對應于指定索引之屬性的名稱。

## <a name="syntax"></a>語法


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

包含屬性索引的 (**長**) **數目**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回指定屬性名稱的 **字串** 。

## <a name="remarks"></a>備註

傳回的屬性名稱可以與 **getItemInfo** 搭配使用，以抓取特定命名屬性的值。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**getAttributeName** 使用目前媒體專案的每個屬性的索引和名稱，填滿名為 MYTEXT 的 HTML 文字區域。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
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

[**AttributeCount**](media-attributecount.md)
</dt> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





