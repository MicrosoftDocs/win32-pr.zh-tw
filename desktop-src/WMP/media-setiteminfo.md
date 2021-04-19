---
title: SetItemInfo 方法
description: SetItemInfo 方法會為目前的媒體專案設定指定之屬性的值。
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999422"
---
# <a name="mediasetiteminfo-method"></a>SetItemInfo 方法

**SetItemInfo** 方法會為目前的媒體專案設定指定之屬性的值。

## <a name="syntax"></a>語法


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*屬性* \[在\]
</dt> <dd>

包含屬性名稱的 **字串**。 如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

</dd> <dt>

*值* \[在\]
</dt> <dd>

包含新值的 **字串**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性數目。 然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷可搭配此方法使用的內建屬性名稱。

使用這個方法之前，請使用 **isReadOnlyItem** 方法來判斷是否可以設定特定屬性。

若要使用此方法，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

**注意**

如果您在應用程式中內嵌 Windows Media Player 控制項，您所變更的檔案屬性將不會寫入數位媒體檔案，直到使用者執行 Windows Media Player 為止。 如果您在以 c + + 撰寫的遠端應用程式中使用控制項，則在進行變更之後，將會立即將您變更的檔案屬性寫入數位媒體檔案。 無論是哪一種情況，您的程式碼都可以透過程式庫立即取得變更。

**Windows Media Player 10** 行動裝置版：這個方法不會實作為。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**setItemInfo** ，以變更目前媒體專案的 [內容類型] 屬性值。 名為 GeNtext.c 就會的 HTML 文字輸入元素可讓使用者輸入文字字串，然後用它來變更屬性資訊。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

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

[**GetItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**IsReadOnlyItem**](media-isreadonlyitem.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





