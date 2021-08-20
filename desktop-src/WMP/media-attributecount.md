---
title: AttributeCount
description: AttributeCount 屬性會抓取可針對媒體專案查詢及/或設定的屬性數目。
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- AttributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d02e120570140aa7c39a4acc7ce0eb096fffd7bccfc51a6c82d53a7ab5f3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117934339"
---
# <a name="mediaattributecount"></a>AttributeCount

**AttributeCount** 屬性會抓取可針對媒體專案查詢及/或設定的屬性數目。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**attributeCount**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**attributeCount** ，判斷目前媒體專案中可用的屬性數目。 程式碼會使用該值來列印 HTML 文字區域中的屬性名稱和值清單，名稱為 myText。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
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

[**GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





