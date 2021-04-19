---
title: ClosedCaption.SAMILang
description: SAMILang 屬性會指定或抓取隱藏式輔助字幕所顯示的語言。
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- ClosedCaption. SAMILang Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977664"
---
# <a name="closedcaptionsamilang"></a>ClosedCaption.SAMILang

**SAMILang** 屬性會指定或抓取隱藏式輔助字幕所顯示的語言。

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **字串**。

## <a name="remarks"></a>備註

薩米文檔案可以包含一或多個語言的文字。 隱藏式字幕的可用語言會定義于薩米文檔案的 <STYLE> 和 </STYLE> 標記之間。 語言識別項是使用唯一的英數位元字串所指定，該字串前面會加上句點 (。 ) 。 針對語言指定的名稱可以是任何字串。 例如，下列程式可用來定義美式英文：


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



如果未指定薩米文語言，預設會使用薩米文檔案中定義的第一種語言。

您使用 *ClosedCaption* 傳遞的值。**SAMILang** 必須符合語言規範中的 **Name** 屬性。

**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的，而且一律會傳回空字串。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *ClosedCaption*。在 HTML SELECT 元素中 **SAMILang** ，以指定隱藏式輔助字幕語言。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption 物件**](closedcaption-object.md)
</dt> </dl>

 

 





