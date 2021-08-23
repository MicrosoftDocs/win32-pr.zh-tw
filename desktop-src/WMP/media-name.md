---
title: Media.name
description: Name 屬性會指定或抓取媒體專案的名稱。
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616854"
---
# <a name="medianame"></a>Media.name

**Name** 屬性會指定或抓取媒體專案的名稱。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**名稱**

## <a name="possible-values"></a>可能的值

這個屬性是包含媒體專案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 若要指定此屬性的值，需要有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

使用這個方法來指定媒體專案的名稱之前，請使用 **isReadOnlyItem** 來判斷是否可以設定名稱。

**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。要變更目前媒體專案名稱的 **名稱**。 名為 NameText 的 HTML 文字輸入元素可讓使用者輸入新名稱的文字字串。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
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

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





